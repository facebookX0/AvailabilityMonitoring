---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Alerthäufigkeit
{: #avmon_alert_freq}

Die Anzeige 'Alerthäufigkeit' enthält eine Karte mit den zuletzt ausgegebenen Alerts. Die Alerts sind nach Standort gruppiert und werden in der Tabelle 'Alerts' aufgeführt.
{: shortdesc}

## Karte 'Alerthäufigkeit'
{: #avmon_alertmap}

Auf der Karte 'Alerthäufigkeit' werden Informationen zu allen Bereitstellungspunkten (Points of Presence, PoPs) für Ihre Tests auf einen Blick angezeigt.

Mit der Zoomfunktion können Sie einen beliebigen Bereich der Karte vergrößern oder auf die ursprüngliche Größe zurücksetzen. Bewegen Sie den Mauszeiger über die einzelnen Standorte, um den Namen des jeweiligen Standorts und die Anzahl der Alerts mit Warnstatus und kritischem Status an dem betreffenden Standort anzuzeigen. Sie können die Alerts, die auf der Karte angezeigt werden, filtern, indem Sie **Alle**, **Geöffnet** oder **Geschlossen** in der Dropdown-Liste **Alerts** auswählen.

![Karte 'Alerthäufigkeit', in der die Tests an vier Bereitstellungspunkten angezeigt werden](images/alert_freq_map2.png)

### Hoststandort
Das Symbol **Hoststandort** ![Symbol für den Standort des Hosts](images/icn_host_crit_whtbackground30.jpg) gibt den Standort des Servers an, auf dem die Anwendung ausgeführt wird, die Sie überwachen. Die Farbe des Symbols **Hoststandort** gibt den Schweregrad des neuesten Alerts am Standort an: Normal ![Symbol für Hoststandort mit grünem Rand, das angibt, dass am Standort kein Alert auftritt](images/icn_host_normal_whtbckgrnd_30x38.jpg), Warnung ![Symbol für Hoststandort mit gelbem Rand, das angibt, dass am Standort ein Alert auftritt](images/icn_host_warning_whtbackground30.jpg) oder Kritisch ![Symbol für Hoststandort mit rotem Rand, das angibt, dass an diesem Standort ein Alert auftritt](images/icn_host_crit_whtbackground30.jpg). Das animierte Symbol **Hoststandort** gibt an, dass von allen Standorten für Ihre Testinstanzen dieser Standort die meisten Alerts mit der höchsten Prioritätsstufe aufweist.

### Standorte der Bereitstellungspunkte (Points of Presence, PoP)
Symbole des Typs **PoP-Standort** ![Symbol 'PoP-Standort'](images/icn_pop_normal_whtbckgrnd30x30.jpg) geben die Standorte der Bereitstellungspunkte (Points of Presence) für die Tests an. Die Farbe jedes Symbols des Typs **PoP-Standort** gibt den Schweregrad des neuesten Alerts an jedem Standort an: Normal ![Symbol für PoP-Standort mit grünem Rand, das angibt, dass am Standort kein Alert auftritt](images/icn_pop_normal_whtbckgrnd30x30.jpg), Warnung ![Symbol für PoP-Standort mit gelbem Rand, das angibt, dass am Standort ein Alert auftritt](images/icn_pop_warning_whtbckgrnd30x30.jpg) oder Kritisch ![Symbol für PoP-Standort mit rotem Rand, das angibt, dass am Standort ein Alert auftritt](images/icn_pop_crit_whtbckgrnd30x30.jpg). Ein animiertes Symbol für den **PoP-Standort** gibt an, dass von allen Standorten für Ihre Testinstanzen dieser Standort die meisten Alerts mit der höchsten Prioritätsstufe aufweist.

Fügen Sie PoP-Standorte zu Ihrem ausgewählten Test hinzu, indem Sie den Cursor auf ein Symbol des Typs **Inaktiver PoP-Standort** ![Inaktiver PoP-Standort](images/icn_avbl_pop.jpg) bewegen und auf **Test hier einfügen** klicken. Die Seite 'Testbearbeitungsmodus' für Ihren ausgewählten Test wird angezeigt. Sie können im Dropdown-Menü **Test** im Bereich **Antwortzeit** und im Bereich **Verfügbarkeit** einen Test auswählen.

<!--
Private PoP locations are represented by **Private PoP location** icons ![Private PoP location icon that indicates 2 alerts with one or more critical alerts at that location.](images/avmon_private_pop.png).
-->
### Anzahl der Alerts
Das Symbol **Hoststandort** und die Symbole des Typs **PoP-Standort** für den PoP-Standort zeigen die Anzahl der geöffneten, der geschlossenen oder aller Alerts an, die an den einzelnen Standorten generiert werden. Die Symbole 'Kritisch', 'Warnung' und 'Normal' ![Symbole 'Kritisch', 'Warnung' und 'Normal' ](images/fltr_alrts_tbl.jpg) geben die Anzahl der Alerts mit der jeweiligen Priorität für die Standorte an.

### Fehlgeschlagene Tests
Standorte, an denen Tests fehlgeschlagen sind, werden mithilfe des Symbols **Hoststandort** oder des Symbols **PoP-Standort** mit einem defekten Rand ![PoP-Standort mit rotem Rand, der 10 Alerts und mindestens einen fehlgeschlagenen Test an diesem Standort angibt](images/avmon_pop_fail_32x33.png) angegeben.

## Alerttabelle
{: #avmon_alertstable}

Die Alerts für alle Standorte werden in einer Tabelle angezeigt.

![Alerttabelle, in der Alerts für alle PoP-Standorte angezeigt werden](images/alert_table.jpg)

Die Tabelle enthält die folgenden Informationen zu den Alerts:

-   **Priorität** gibt an, ob es sich um einen kritischen Alert oder einen Warnungsalert handelt.
-   **Zeitmarke** gibt den Zeitpunkt der Erstellung des Alerts an.
-   **Beschreibung** gibt eine Zusammenfassung der Leistung der Testinstanz an.
-   **Ausgelöst von** gibt den Namen des Test an, der den Alert ausgelöst hat.
-   **Standort** gibt an, wo das Problem aufgetreten ist.
-   **Status** gibt an, ob der Alert geöffnet oder geschlossen ist.

### Alertdetails anzeigen
Jeder Alert in der Tabelle enthält einen Link zum Dashboard **Aufgliederung**. Verwenden Sie das Dashboard 'Aufgliederung' zur Fehlerbehebung.

### Alerts filtern
Klicken Sie in der Karte auf das Symbol **Hoststandort** oder **PoP-Standort**, um Alerts für einen bestimmten Standort zu filtern. Zum Anzeigen der Alerts für alle Standorte klicken Sie auf eine beliebige Stelle in der Karte, bei der es sich nicht um ein Symbol des Typs **Hoststandort** oder **PoP-Standort** handelt.

Wenn Sie die Alerts in der Tabelle nach Priorität filtern möchten, klicken Sie auf das Symbol **Kritisch**, **Warnung** oder **Normal** ![Die Symbole 'Kritisch', 'Warnung' und 'Normal'](images/fltr_alrts_tbl.jpg). Klicken Sie erneut auf das ausgewählte Symbol, um den Filter aufzuheben und Alerts aller Prioritäten anzuzeigen.

### Alertschwellenwerte ändern
Alerts werden durch die Schwellenwerte ausgelöst, die Sie beim Erstellen eines Tests angeben. In den meisten Fällen werden sie aufgrund von Verfügbarkeitsproblemen oder langsamen Antwortzeiten generiert. Wenn Sie die Schwellenwerteinstellungen ändern möchten, klicken Sie im Bereich 'Synthetische Tests' auf das Symbol **Aktionen** ![Symbol 'Aktionen'](images/actions_icn_white_smll.jpg) für den Test, der den Alert ausgelöst hat; klicken Sie anschließend auf **Bearbeiten**.
