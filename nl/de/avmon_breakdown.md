---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Dashboard 'Aufgliederung'
{: avmon_view_breakdown}

Das Dashboard **Aufgliederung** enthält wichtige statistische Informationen für die Tests. Außerdem finden Sie hier eine Zusammenfassung der Informationen zu Verfügbarkeit und Antwortzeiten, Langzeittrends und Leistungsdaten der Tests der letzten 24 Stunden.
{: shortdesc}

Zum Anzeigen einer detaillierten Aufgliederung eines Tests klicken Sie im Bereich mit den synthetischen Tests auf den entsprechenden Test. Sie können das Dashboard **Aufgliederung** auch öffnen, indem Sie im Bereich 'Alerthäufigkeit' in der Tabelle 'Alert' auf 'Aufgliederung' klicken.

Das Dashboard für die Aufgliederung enthält vier Bereiche:

## Testzusammenfassung
{: #avmon_bdown_summary}

![Bereich 'Testzusammenfassung'](images/avmon_bdown_summ.png)

Der Bereich **Testzusammenfassung** enthält die folgenden Testinformationen für die letzten 24 Stunden:

-   **Aktueller Status** zeigt den Teststatus an.
-   **Testinstanzen** zeigt eine prozentuale Aufgliederung der unterschiedlichen Testinstanzen (normal, Warnung, kritisch) an.
-   **Durchschnittliche Antwortzeit** zeigt die durchschnittliche Antwortzeit des Tests an.
-   **Langzeittrends** zeigt die Langzeittrends der Testleistung für das 50. 95. und 99. Perzentil in Millisekunden an.

## Testinstanzen
{: #avmon_bdown_instances}

![Aufgliederung der Rest-API-Testinstanz in der Tabelle 'Testinstanzen'](images/avmon_bdown_apitest_instance.png)

In der Tabelle **Testinstanzen** werden detaillierte Informationen zu jeder einzelnen Testinstanz, einschließlich Status, Antwortzeit, Standort der Ausführung des Tests, Anzahl der Fehler und Zeitmarke der Testausführung, angezeigt. Wenn Sie eine Testinstanz genauer untersuchen möchten, klicken Sie auf **Erweitern**. Damit werden detaillierte Antwortinformationen zu jedem Schritt der Testinstanz aufgelistet. Sie können die Spalten beliebig sortieren. So finden Sie am schnellsten den Schritt, bei dem es zu einer Verlangsamung oder einem Ausfall kam. Die Anzeige von Fehlern, Testsequenz und Antwortzeit liefert Aufschluss über die vorliegenden Probleme.

Welche Informationen angezeigt werden, hängt vom Typ des überwachten synthetischen Tests ab:

### API
Wenn Sie für eine API-Testinstanz auf **Erweitern** klicken, wird eine allgemeine Zusammenfassung der folgenden Details angezeigt:

-   **Antwort** zeigt die Gesamtantwortzeit für die Testinstanz einschließlich der Zeit für die Weiterleitung an.
-   **Weiterleitung** zeigt die Gesamtzeit für Weiterleitungen für die Testinstanz an.
-   **Größe** zeigt die Größe des Objekts an.
-   **Downloadgeschwindigkeit** zeigt die Geschwindigkeit an, mit der die einzelnen Objekte heruntergeladen werden.
-   **Fehler** zeigt die Anzahl der Fehler an, die bei der Testinstanz aufgetreten sind. Klicken Sie auf das Symbol **Informationen**, um die Fehlerdetails anzuzeigen.

In einer Tabelle werden die einzelnen Schritte im API-Aufruf angezeigt, zusammen mit dem Namen des Schritts, der Abfolge der Schritte und der Antwortzeit für jeden Schritt. Die folgenden Schrittnamen werden angezeigt:

-   **Namenssuche** stellt die Zeit dar, die die Testinstanz benötigte, um den Namen des Objekts aufzulösen.
-   **Verbindung** stellt die Zeit dar, die in der Testinstanz vom Starten des Schritts bis zum erfolgreichen Herstellen einer Verbindung zum fernen Host oder Proxy vergangen ist.
-   **App-Verbindung** stellt die Zeit dar, die in der Testinstanz vom Starten des Schritts bis zum erfolgreichen Herstellen der SSL-Verbindung zum fernen Host vergangen ist.
-   **Transfervorbereitung** stellt die Zeit dar, die in der Testinstanz vom Starten des Schritts bis zum Zeitpunkt unmittelbar vor dem Starten des Dateitransferbefehls vergangen ist.
-   **Transferstart** stellt die Zeit dar, die in der Testinstanz vom Starten des Schritts bis zum Empfang des ersten Bytes vergangen ist.
-   **Transfer** stellt die Zeit dar, die die Testinstanz für den Transfer der Datei benötigte.

### Webseite
![Aufgliederung der Webseitentestinstanz in der Tabelle 'Testinstanzen'](images/avmon_bdown_webpage_instance.png)

Wenn Sie für eine Webseitentestinstanz auf **Erweitern** klicken, wird eine allgemeine Zusammenfassung der folgenden Details angezeigt:

-   **Antwort** gibt die Antwortzeit für die Testinstanz.
-   **Summe der Anforderungen (extern)** zeigt die Gesamtzahl der Anforderungen für die Testinstanz an. Die Anzahl der externen Anforderungen wird in Klammern angegeben.
-   **Seitengröße** zeigt die Größe der Webseite an.
-   **Fehler** zeigt die Anzahl der Fehler an, die bei der Testinstanz aufgetreten sind. Klicken Sie auf das Symbol 'Informationen', um die Fehlerdetails anzuzeigen.

Darüber hinaus wird eine Tabelle angezeigt, die die folgenden Details für jede Anforderung enthält, die der Test sendet:

-   **Typ** zeigt den Typ der Anforderung an, z. B. HTML, CSS, JavaScript oder Abbildung. Externe und interne Anforderungen sind durch Symbole gekennzeichnet.
-   **Dateipfad** beschreibt die Speicherposition des angeforderten Objekts.
-   **Größe** zeigt die Größe des angeforderten Objekts an.
-   **Sequenz** zeigt die Abfolge der Anforderungen an, die der Test sendet.
-   **Zeit** zeigt die Zeit an, die jede Anforderung benötigt.
-   **Statuscode** zeigt den HTTP-Anforderungsstatuscode an.
-   **Status** beschreibt das Ergebnis der Anforderung, z. B. 'abgeschlossen', 'unbekannt' oder 'fehlgeschlagen'.

### Script
![Aufgliederung der Scripttestinstanz in der Tabelle 'Testinstanzen'](images/avmon_bdown_script_instance.png)

Wenn Sie für eine Scripttestinstanz auf **Erweitern** klicken, werden die Antwortzeit, die Anzahl der Scriptschritte und die Anzahl der Fehler angezeigt. Klicken Sie auf das Symbol **Informationen**, um die Fehlerdetails anzuzeigen.

Die folgenden Details für die einzelnen Schritte des Scripts werden in einer Tabelle angezeigt:

-   **Name** zeigt die einzelnen von der Testinstanz aufgerufenen Selenium-Befehle an, z. B. Open, ClickAt oder VerifyBodyText.
-   **Sequenz** zeigt die Abfolge der Scriptschritte vom Anfang bis zum Ende der Testinstanz an.
-   **Zeit** zeigt die Zeit an, die jeder Schritt des Scripts benötigt.
-   **Fehler** zeigt die Anzahl der Fehler an, die bei den einzelnen Schritten des Scripts aufgetreten sind.
-   **Status** beschreibt das Ergebnis des Scriptschritts, z. B. 'abgeschlossen', 'unbekannt' oder 'fehlgeschlagen'.

Sie können einen Drilldown durchführen und Details zu den Anforderungen anzeigen, die von den einzelnen Schritten des Scripts generiert werden.

![Aufgliederung der Details zu einzelnen Schritten für Ihre Scripttestinstanz in der Tabelle 'Testinstanzen'](images/avmon_bdown_script_subtrans.png)

Klicken Sie auf **Erweitern**, um eine Tabelle mit den folgenden Details anzuzeigen:

-   **Typ** zeigt den Typ der Anforderung an, z. B. HTML, CSS, JavaScript oder Abbildung. Externe und interne Anforderungen sind durch Symbole gekennzeichnet.
-   **Dateipfad** beschreibt die Speicherposition des angeforderten Objekts.
-   **Größe** zeigt die Größe des angeforderten Objekts an.
-   **Sequenz** zeigt die Abfolge der Anforderungen an, die der Test sendet.
-   **Zeit** zeigt die Zeit an, die jede Anforderung benötigt.
-   **Statuscode** zeigt den HTTP-Anforderungsstatuscode an.
-   **Status** beschreibt das Ergebnis der Anforderung, z. B. 'abgeschlossen', 'unbekannt' oder 'fehlgeschlagen'.

{{site.data.keyword.prf_hubshort}} kann automatisch einen Screenshot erstellen, wenn das Laden der Webseite oder ein Schritt im Script fehlschlägt. Wenn z. B. einer der Schritte in Ihrem Script eine Webseite öffnet, diese aber nicht geladen wird,
erstellt {{site.data.keyword.prf_hubshort}} automatisch einen Screenshot. Zur Anzeige eines Screenshots der Webseite bzw. des Scripts klicken Sie auf das Symbol **Screenshotfehler** ![Symbol 'Screenshotfehler'](images/scrnsht_err_icn_white.jpg). Dieses Feature ist nur bei der Überwachung von Webseiten und scriptgesteuerten Tests verfügbar. Es funktioniert nicht bei der REST-API-Überwachung.

Sie können auch eine Aufzeichnung des Netzverkehrs einer bestimmten Testinstanz als .har-Datei herunterladen, indem Sie auf das Symbol **Download** ![Downloadsymbol](images/download_icn_white_smll.jpg) klicken. Dieses Feature ist bei der Überwachung von Webseiten und scriptgesteuerten Verhaltenstests verfügbar.

## Antwortzeit und Verfügbarkeit
{: #avmon_bdown_rt_avail}
Im Bereich 'Antwortzeit und Verfügbarkeit' wird eine Grafik die gemessenen Antwortzeiten und der Verfügbarkeit für Instanzen Ihres Tests über einen definierten Zeitraum hinweg angezeigt. Weitere Informationen finden Sie unter [Antwortzeit und Verfügbarkeit](avmon_resptime_avail.html "Im Bereich 'Antwortzeit und Verfügbarkeit' können Sie Antwortzeit, Verfügbarkeitstrends, Alerts und Aktivitäten über einen bestimmten Zeitraum hinweg visualisieren. Durch die Korrelation von Metriken, Alerts und Aktivitäten können Sie problemlos eine bestimmte Anwendungsänderung oder Codebereitstellung isolieren, wenn Sie eine zu lange Antwortzeit feststellen.").

## Aktivität
{: #avmon_bdown_activity}
Der Fensterbereich 'Aktivität' enthält eine Tabelle mit allen Aktivitäten in den letzten 24 Stunden. Weitere Informationen finden Sie unter [Aktivität](avmon_activities.html "'Informationen zu Aktivitäten können Sie im Bereich 'Aktivitäten' anzeigen. Aktivitäten sind Aktionen, die außerhalb von benutzerdefinierten Ereignissen auftreten.").
