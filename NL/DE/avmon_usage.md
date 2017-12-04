---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Servicenutzung
{: #avmon_usage}

Sie können die Details zur Nutzung von {{site.data.keyword.prf_hubshort}} auf der Registerkarte **Überwachung** für Ihre App und im Hauptdashboard von {{site.data.keyword.prf_hubshort}} anzeigen.

Um eine Übersicht der Nutzung von {{site.data.keyword.prf_hubshort}} über die Tabelle **Alle Anwendungen** anzuzeigen, klicken Sie zunächst auf den Namen Ihrer App und anschließend auf die Registerkarte **Überwachung** im App-Bereich. Der Prozentsatz für **Nutzung** wird zusammen mit dem von Ihnen verwendeten Plan in Form einer Messanzeige angezeigt.

Um eine Übersicht der Nutzung über das Hauptdashboard von {{site.data.keyword.prf_hubshort}} anzuzeigen, klicken Sie auf das Symbol **Konfigurieren** ![Symbol 'Konfigurieren'](images/config_icn_white_smll.jpg). Wenn Sie den Lite-Plan für {{site.data.keyword.prf_hubshort}} nutzen, wird Nutzung wird zusammen mit der Anzahl der verwendeten Tests als Balkengrafik und als Prozentsatz angezeigt. Wenn Sie den kostenpflichtigen Plan nutzen, wird die Nutzung in Datenpunkten angezeigt. Sie können die Nutzungsdetails für die einzelnen Tests im Bereich 'Synthetische Tests' aufrufen.

Die Nutzung wird in Datenpunkten gemessen. Die geschätzte Anzahl der Datenpunkte wird anhand der folgenden Formel berechnet:

Geschätzte Anzahl der Datenpunkte = T \* L \* (60/M \* 24 \* 30) pro Monat

Dabei gibt T die Anzahl der ausgeführten synthetischen Tests an, L die Anzahl der Standorte und M das Intervall zwischen den Tests (in Minuten).

Bei einfachen Tests, wie z. B. Webseiten- und REST-API-Tests, wird 1 Datenpunkt für jeden Test verwendet. Bei erweiterten Tests, wie z. B. Selenium-Scripts und REST-API-Scripts, werden 100 Datenpunkte für jeden Test verwendet.

Sie können die tatsächliche Nutzung im Nutzungsdashboard auf der {{site.data.keyword.Bluemix_notm}}-Kontoseite anzeigen. Klicken Sie auf **Konto**; wählen Sie anschließend **Nutzungsdashboard** aus und blättern Sie nach unten zum Abschnitt **Servicekosten**. Klicken Sie auf das **Pfeilsymbol** für den {{site.data.keyword.prf_hubshort}}-Service, um die Anzahl der Nutzungsdatenpunkte anzuzeigen. Weitere Informationen zu Preisstrukturplänen und Nutzungsplänen für {{site.data.keyword.prf_hubshort}} finden Sie im Abschnitt zu den Preisstrukturplänen auf der Katalogseite [Availability Monitoring](https://console.{DomainName}/catalog/services/availability-monitoring/ "(Wird in neuer Registerkarte oder neuem Fenster geöffnet)"){: new_window}.
