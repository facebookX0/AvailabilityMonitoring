---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Blockieren und Filtern mit Whitelist und Blacklist
{: #avmon_filters}

Mit der Whitelist und der Blacklist können Sie festzulegen, an welche Ressourcen Anforderungen gesendet werden und welche Ressourcen mit ihren Metriken und Statusangaben zu den Anwendungstests beitragen sollen. Whitelists und Blacklists sind nur für Tests für Webseiten und scriptgesteuertes Verhalten verfügbar.
{: shortdesc}

Definieren Sie in den Feldern **Whitelist** und **Blacklist** die Ressourcen, auf die während eines Tests zugegriffen werden kann sowie die Ressourcen, die mit ihren Metriken und Statusangaben in die Tests einfließen. Mit 'Whitelist' und 'Blacklist' kann gesteuert werden, welche Abhängigkeiten und Ressourcen zu den Antwortzeiten der getesteten Webanwendungen beitragen, zum Beispiel Metriken anderer Anbieter. Sie können Ihre Whitelist und Blacklist konfigurieren, wenn Sie einen Test für eine Webseite oder scriptgesteuertes Verhalten erstellen.

Sie können die **Whitelist** verwenden, um zulässige Domänen und URLs zu definieren; verwenden Sie anschließend die **Blacklist**, um bestimmte Elemente der zulässigen Standorte zu blockieren.

## Syntax

Verwenden Sie Kommas (,) zum Trennen der Einträge in der Blacklist und Whitelist. Verwenden Sie das Platzhalterzeichen (\*) zum Filtern der Elemente jeder einzelner URL oder Domäne.

## Whitelist

Fügen Sie die URLs oder Domänen, die Sie in die Anforderung und die Metrikberechnungen einfügen möchten, zum Feld 'Whitelist' hinzu. Sie können bis zu 10 Einträge in der Whitelist auflisten. Die Länge eines Eintrags darf 200 Zeichen nicht überschreiten. Alle Domänen und URLs, die nicht mit den Einträgen in der Whitelist übereinstimmen, werden blockiert.

Beispiel:
```
ibm.com, *developerworks*, *.s81c.com/*
```
{: codeblock}

## Blacklist

Fügen Sie die URLs oder Domänen, von denen Sie Anforderung und die Metrikberechnungen blockieren möchten, zum Feld 'Blacklist' hinzu. Sie können bis zu 20 Einträge in der Blacklist auflisten. Die Länge eines Eintrags darf 200 Zeichen nicht überschreiten. 

Beispiel:
```
*.profile.*.cloudfront.net/*.png
```
{: codeblock}

## Verhalten filtern und blockieren

Für einen Test kann sowohl eine Whitelist als auch eine Blacklist verwendet werden. Wenn festgestellt werden muss, welche Standorte zulässig sind oder blockiert werden sollen, genießt die Blacklist immer Vorrang vor der Whitelist. In der folgenden Tabelle wird das Filter- und Blockierverhalten für alles Szenarios mit Whitelist und Blacklist aufgeführt.

<table id="avmon_whitelist_blacklist__table_gyg_vvp_fbb">
<caption>Tabelle 1. Filter- und Blockierverhalten für Whitelist und Blacklist</caption>
<thead>
<tr>
<th>Blacklist</th>
<th>Whitelist</th>
<th>Verhalten</th>
<th>Grund</th>
</tr>
</thead>
<tbody>
<tr>
<td>Leer</td>
<td>Leer</td>
<td>Zugriff zulassen</td>
<td>Es wurden keine Filterregeln eingegeben.</td>
</tr>
<tr>
<td>Leer</td>
<td>URL stimmt nicht mit Listeneintrag überein</td>
<td>Zugriff blockieren</td>
<td>URL befindet sich nicht in der Whitelist.</td>
</tr>
<tr>
<td>Leer</td>
<td>URL stimmt mit Listeneintrag überein</td>
<td>Zugriff zulassen</td>
<td>URL befindet sich in der Whitelist. Kein Blacklist-Eintrag zum Blockieren des Zugriffs.</td>
</tr>
<tr>
<td>URL stimmt nicht mit Listeneintrag überein</td>
<td>Leer</td>
<td>Zugriff zulassen</td>
<td>URL befindet sich nicht in der Blacklist. Kein Whitelist-Eintrag zum Blockieren des Zugriffs.</td>
</tr>
<tr>
<td>URL stimmt mit Listeneintrag überein</td>
<td>Leer</td>
<td>Zugriff blockieren</td>
<td>URL befindet sich in der Blacklist. </td>
</tr>
<tr>
<td>URL stimmt nicht mit Listeneintrag überein</td>
<td>URL stimmt nicht mit Listeneintrag überein</td>
<td>Zugriff blockieren</td>
<td>URL befindet sich nicht in der Whitelist.</td>
</tr>
<tr>
<td>URL stimmt nicht mit Listeneintrag überein</td>
<td>URL stimmt mit Listeneintrag überein</td>
<td>Zugriff zulassen</td>
<td>URL befindet sich in der Whitelist. URL befindet sich nicht in der Blacklist. </td>
</tr>
<tr>
<td>URL stimmt mit Listeneintrag überein</td>
<td>URL stimmt nicht mit Listeneintrag überein</td>
<td>Zugriff blockieren</td>
<td>URL befindet sich nicht in der Whitelist. URL befindet sich in der Blacklist.</td>
</tr>
<tr>
<td>URL stimmt mit Listeneintrag überein</td>
<td>URL stimmt mit Listeneintrag überein</td>
<td>Zugriff blockieren</td>
<td>URL befindet sich in der Blacklist. Der Blacklist-Eintrag hat Vorrang vor dem Whitelist-Eintrag.</td>
</tr>
</tbody>
</table>
