---

copyright:
  years: 2015, 2017
lastupdated: "2017-9-28"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Anwendungsstatus
{: #avmon_health}

Im Teilfenster 'Anwendungsstatus' wird ein Snapshot der Anwendungsleistung basierend auf der Anwendungsverfügbarkeit, der Benutzerzufriedenheit mit der Anwendungsleistung und dem Durchsatz der Anwendung angezeigt.
{: shortdesc}

Wenn von {{site.data.keyword.prf_hubshort}} festgestellt wird, dass ein Datenkollektor für die Anwendung konfiguriert ist, kann das Teilfenster 'Anwendungsstatus' angezeigt werden.

**Einschränkung:** Anfangs ist nur für Node.js-Anwendungen ein Datenkollektor verfügbar. Weitere Informationen zum Konfigurieren eines Node.js-Datenkollektors finden Sie in der [Dokumentation zum Node.js-Datenkollektor](https://www.npmjs.com/package/ibmapm "(Wird in neuer Registerkarte oder neuem Fenster geöffnet)"){: new_window}.

Im Bereich werden drei Metriken angezeigt: **Verfügbarkeit**, **Zufriedenheitsquote** und **Anforderungsvolumen**.
![Teilfenster 'Anwendungsstatus', in dem die Verfügbarkeitsstufe, die Benutzerzufriedenheit und der Transaktionsdurchsatz der App angezeigt werden.](images/avmon_app_health_ui.jpg)
 Die Berechnung der Metrik **Verfügbarkeit** basiert auf simulierten Benutzertransaktionsdaten aus synthetischen Tests. Im Gegensatz dazu basieren die Metriken **Zufriedenheitsquote** und **Anforderungsvolumen** sowohl auf realen als auch simulierten Benutzertransaktionsdaten, die von Datenkollektoren bereitgestellt werden.

Von den numerischen Bezeichnungen wird der neueste Wert für jede Metrik angegeben. Beispiel: Der neueste Wert für **Verfügbarkeit** ist ![Der neueste Wert für die Metrik 'Verfügbarkeit'](images/avmon_app_health_latest.jpg). In einem Kurvendiagramme für eine Zeitreihe wird die Leistung einer Anwendung im zeitlichen Verlauf dargestellt. Sie können den Zeitraum für Verlaufsdiagramme durch die Auswahl der letzten **24 Stunden** oder der letzten **7 Tage** in der Dropdown-Liste für die Zeit festlegen. Wenn Sie den Mauszeiger über die Linie des Diagramms bewegen, wird der Wert für jeden einzelnen Datenpunkt in einem QuickInfo angezeigt, zum Beispiel ![QuickInfo in der Linie eines Verlaufsdiagramms](images/avmon_app_health_hover.jpg). Wenn Sie auf einen Datenpunkt im Kurvendiagramm klicken, wird eine numerische Bezeichnung mit dem Wert für den jeweiligen Datenpunkt angezeigt. Klicken Sie auf einen beliebigen Bereich außerhalb des Kurvendiagramms, um die numerischen Bezeichnung auf die neuesten Werte zurückzusetzen. Wenn Sie den Mauszeiger auf einem Diagramm bewegen oder auf ein Diagramm klicken, werden die beiden anderen Diagramme im Teilfenster **Anwendungsstatus** aktualisiert.

Klicken Sie auf ![Menü zum Anzeigen der Beiträge, das Sie zum Anzeigen der Transaktionen oder Tests erweitern können, die die Grundlage der Metrik bilden.](images/avmon_view_contrib.jpg), um die obersten fünf Transaktionen oder Tests anzuzeigen, die in den aktuellen Status der Anwendung eingeflossen sind.![Bereich 'Anwendungsstatus', in dem Verfügbarkeitsstufe, Benutzerzufriedenheit und Transaktionsdurchsatz der Anwendung angezeigt werden.](images/avmon_app_health_expanded.jpg)

## Verfügbarkeit
{: #avmon_health_availability}
Die **Verfügbarkeit** gibt den Umfang an, in dem die Anwendung betriebsbereit ist. Die Verfügbarkeit ergibt sich aus dem Prozentsatz der synthetischen Testinstanzen, die erfolgreich verlaufen sind. Beispiel: Wenn alle synthetischen Tests im letzten Testintervall erfolgreich verlaufen sind, beträgt der Wert für die Verfügbarkeit der Anwendung 100%.

Sie können in der Registerkarte 'Überwachung' konfigurieren, wie die Verfügbarkeit von {{site.data.keyword.prf_hubshort}} berechnet wird; hierzu wählen Sie Tests aus, die in die Berechnung der Verfügbarkeit einfließen sollen. Weitere Informationen finden Sie unter [Auf Availability Monitoring zugreifen](avmon_tab.html "Auf das Availability Monitoring-Dashboard können Sie über die Registerkarte **Überwachung** zugreifen. Auf der Registerkarte 'Überwachung' für die Cloud Foundry-Anwendung werden Übersichtsinformationen zu Verfügbarkeit und Status der Tests sowie zu den Details und der Verwendung der Servicesubskriptionen angezeigt.").

Von {{site.data.keyword.prf_hubshort}} wird der Prozentsatz der Testinstanzen berechnet, die pro Stunde verfügbar sind. Bewegen Sie den Mauszeiger über die Linie im Diagramm, um den Wert für jedes Stundenintervall während der letzten 24 Stunden oder sieben Tage anzuzeigen.

Die obersten fünf synthetischen Tests, die zur aktuellen Verfügbarkeitsstufe der Anwendung beitragen, werden angezeigt. In der Tabelle werden die folgenden Informationen zu jedem einzelnen Test angezeigt.

-   In den **Tests** werden die Testnamen angezeigt, die Sie zugewiesen haben.
-   In den **Instanzen** wird die Anzahl der Testinstanzen angezeigt, die für jeden einzelnen Test ausgeführt wurden.
-   Die **Fehlerrate** gibt den Prozentsatz der Testinstanzen an, die für jeden einzelnen Test fehlgeschlagen sind.


## Zufriedenheitsquote
{: #avmon_health_satscore}
Die **Zufriedenheitsquote** ist ein Indikator für die Benutzerzufriedenheit mit der Bereitschaft der Anwendung. Sie können einen Zufriedenheitsschwellenwert (**T**) für die Anwendung festlegen. Sie bestimmen, welche Antwortzeit die Benutzeranforderungen erfüllen müssen, damit die Benutzer zufrieden sind.

Die Antwortzeiten der Benutzeranforderungen werden in einen Indexwert zwischen 0,0 und 1,0 umgewandelt, wobei 1,0 für den besten Wert steht, der sich ergibt, wenn alle Benutzer zufrieden sind. Zum Berechnen der Zufriedenheitsquote werden die Benutzerbeispiele wie folgt kategorisiert:

-   Zufrieden - Wenn die Antwortzeit einer Benutzeranforderung kleiner-gleich dem Zufriedenheitsschwellenwert ist, lautet die Klassifizierung 'Zufrieden'.
-   Toleriert - Wenn die Antwortzeit einer Benutzeranforderung zwischen 'Zufrieden' und 'Gescheitert' liegt, wird sie wird als 'Toleriert' klassifiziert.
-   Gescheitert - Für Benutzeranforderungen mit einer Antwortzeit größer als 4**T** oder mit einem Fehler als Ergebnis lautet die Klassifizierung 'Gescheitert'.

Anschließend wird die Zufriedenheitsquote anhand der Formel [zufriedene Benutzeranforderung + (tolerierte Benutzeranforderungen /2)] / [Gesamtzahl der der Benutzeranforderungen] berechnet.

Von {{site.data.keyword.prf_hubshort}} wird die Zufriedenheitsquote auf Basis der Transaktionsdaten für jedes einzelne Intervall berechnet. Bewegen Sie den Mauszeiger über die Linie im Diagramm, um den Wert für jedes Stundenintervall während der letzten 24 Stunden oder sieben Tage anzuzeigen.

In der Tabelle werden die folgenden Informationen zu den obersten fünf Transaktionen angezeigt, die in die aktuelle Zufriedenheitsquote der Anwendung eingeflossen sind:

-   Unter **Transaktionen** wird der Name der Benutzertransaktion angezeigt.
-   Unter **Quote** wird die Zufriedenheitsquote angezeigt, die für die einzelne Transaktion berechnet wird.
-   Unter **Unzufriedenheit** wird der Beitrag der Transaktion zu den aktuellen Benutzerunzufriedenheitsstufen angezeigt. Wenn die Benutzerzufriedenheit nicht optimal ist, können Sie mit dem Prozentsatz **Unzufriedenheit** ermitteln, wie viel jede einzelne Transaktion zur Unzufriedenheitsstufe  beigetragen hat.


## Anforderungsvolumen
{: #avmon_health_reqvol}
Die Metrik 'Anforderungsvolumen' ist das aktuelle Volumen der Benutzertransaktionsinstanzen. Die Metrik gibt den derzeitigen Durchsatz der Anwendung an.

Die durchschnittliche Transaktionsantwortzeit wird auch unter der Bezeichnung angezeigt, zum Beispiel ![Der neueste Wert für die durchschnittliche Antwortzeit](images/avmon_app_health_response.jpg), und die durchschnittlichen Antwortzeitwerte werden im Diagramm dargestellt. Sie können nach Korrelationen zwischen Durchsatzzunahmen und gestiegenen durchschnittliche Antwortzeiten suchen.

Die unaufbereiteten Anforderungsvolumendaten werden aggregiert und im Diagramm auf stündlicher Basis angezeigt. Bewegen Sie den Mauszeiger über die Linie im Diagramm, um den Durchsatz der Anwendung jedes Stundenintervalls während der letzten 24 Stunden oder sieben Tage anzuzeigen.

In der Tabelle werden die folgenden Informationen zu den obersten fünf Transaktionen angezeigt, die am meisten in das aktuelle Anforderungsvolumen einfließen. Wenn die Anwendung einem starken Benutzerdatenverkehr ausgesetzt ist, verwenden Sie **Gesamtprozentsatz**, um zu ermitteln, wie viel jede einzelne Transaktion zum gesamten Datenverkehrsaufkommen beiträgt.

-   Unter **Transaktion** wird der Name der Benutzertransaktion angezeigt.
-   Unter **Umfang** wird die Anzahl der Transaktionsinstanzen für jede einzelne Transaktion angezeigt.
-   Unter **Gesamtprozentsatz** wird der Prozentsatz am gesamten Umfang der Anforderungen angezeigt.
