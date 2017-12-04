---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Einführung in Availability Monitoring
{: #avmon_gettingstarted}

Verwenden Sie {{site.data.keyword.prf_hublong}} zum Ausführen simulierter Leistungstests von jedem Standort der Welt aus, rund um die Uhr. Damit können Sie Leistungsprobleme proaktiv erkennen, eingrenzen und diagnostizieren, bevor sich diese auf die Benutzer auswirken. Stellen Sie sicher, dass Ihre Anwendungen verfügbar sind und die Sollwerte für Antwortzeiten erfüllen, wenn Sie fortlaufende Aktualisierung implementieren. Konfigurieren Sie die Datenkollektoren für die Anwendungen zum Erfassen der Benutzertransaktionsdaten. Verwenden Sie diese Daten in {{site.data.keyword.prf_hubshort}} zum Überwachen der Reaktionsfähigkeit und des Durchsatzes der Anwendung.
{: shortdesc}

## Informationen zu diesem Vorgang
{: #avmon_start_about}

{{site.data.keyword.prf_hubshort}} ist als Service in der DevOps-Domäne im {{site.data.keyword.Bluemix_notm}}-Katalog verfügbar. Standardmäßig finden Sie die Anwendung auch im Anwendungsdashboard der Registerkarte **Überwachung**. Sie können sofort mit dem Überwachen der Verfügbarkeit und der Leistung Ihrer Anwendung beginnen. Wenn Sie {{site.data.keyword.prf_hubshort}} an Ihre Anwendung binden, wird automatisch ein synthetischer Test erstellt, der die Haupt-URL der Anwendung standardmäßig überwacht.

## Webseitentest erstellen
{: #avmon_start_procedure}

Führen Sie die folgenden Schritte aus, um {{site.data.keyword.prf_hubshort}} für Ihre Anwendung zu öffnen, einen Webseitentest zum Überwachen einer anderen URL zu erstellen und Benachrichtigungsalerts für Ihre Tests einzurichten.

1.  Wenn Sie eine Cloud Foundry-Anwendung haben, die Sie überwachen möchten, klicken Sie in der Tabelle **Alle Anwendungen** im **Apps**-Dashboard auf den entsprechenden Anwendungsnamen. Wenn Sie noch keine Anwendung haben, erstellen Sie sie und die Anwendungskarte öffnet sich automatisch. Cloud Foundry-Anwendungen werden automatisch an {{site.data.keyword.prf_hubshort}} gebunden, wenn Sie auf die Registerkarte 'Überwachung' klicken.
2.  Klicken Sie zum Öffnen von {{site.data.keyword.prf_hubshort}} auf die Registerkarte **Überwachung**. Auf der Registerkarte **Überwachung** werden die drei Messanzeigen **Durchschnittliche Testverfügbarkeit** für die letzten 24 Stunden, **Aktueller Teststatus** und **Nutzung** der aktuellen Planzuordnung angezeigt. Klicken Sie auf **Neuen Test hinzufügen**, um einen Überwachungstest zu konfigurieren.

    ![Registerkarte 'Availability Monitoring'](images/avmon_tab.png)

    Die URL der Hauptanwendung wird standardmäßig überwacht. Alle anderen URLs und Services, die Sie überwachen, können innerhalb oder außerhalb von Bluemix liegen und müssen nicht mit der zugehörigen Cloud Foundry-Anwendung in Zusammenhang stehen.

3.  Klicken Sie auf **Einzelne Aktion** auf der Seite zum Einrichten der Überwachung und klicken Sie anschließend auf der Seite 'Einzelne Aktion' auf **Webseite**.
4.  Geben Sie einen aussagefähigen Namen für Ihren Test in das Feld **Name** ein. Fügen Sie eine Beschreibung für den Zweck Ihres Tests im Feld **Beschreibung** hinzu.
5.  Geben Sie die **URL** der Webanwendung ein, die Sie testen möchten.
6.  Konfigurieren Sie die Schwellenwerte für den Warnungsalert und den kritischen Alert im Abschnitt 'Antwortvalidierung'. Bearbeiten Sie die Felder **Wert** und **Einheit** für jede Zeile. Wenn die Antwortzeiten den Warnungsschwellenwert oder den kritischen Schwellenwert überschreiten, werden Alerts ausgelöst.

    ![Abschnitt 'Antwortvalidierung' mit Standardwarnung und kritischen Schwellenwerten](images/avmon_webpage_resp_val.png)

7.  Verwenden Sie die **Blacklist** und die **Whitelist**, um anzugeben, an welche URLs und Domänen Anforderungen gesendet werden sollen, und welche URLs und Domänen zu den Metriken und Statuswerten Ihrer Anwendungstests beitragen sollen. Fügen Sie die URLs und Domänen, die Sie einschließen oder blockieren möchten, jeweils zur **Whitelist** bzw. **Blacklist** hinzu. Weitere Informationen zum Blockieren und Filtern finden Sie unter [Blockieren und Filtern mit Whitelist und Blacklist](avmon_whitelist_blacklist.html "Verwenden Sie die Whitelist und Blacklist, um festzulegen, an welche Ressourcen Anfragen gesendet werden sollen, und welche Ressourcen mit ihren Daten zu den Metriken und Statuswerten der Anwendungstests beitragen sollen. Whitelist und Blacklist sind nur für Tests von Webseiten und des scriptgesteuerten Verhaltens verfügbar.").
8.  Klicken Sie auf **Überprüfen**, um den Webseitentest zu erstellen und um zu ermitteln, ob Ihre Testanforderung gültig ist.

    {{site.data.keyword.prf_hubshort}} ermittelt die Gültigkeit des Tests, indem eine GET-Anforderung an Ihre Test-URL gesendet wird. Es findet keine Antwortvalidierung während der Testüberprüfung statt.

    Der überprüfte Test wird in der Tabelle Überprüfte Elemente angezeigt. Um weitere URLs hinzuzufügen, wiederholen Sie die Schritte 3 bis 8.

9.  Um Ihre Testeinstellungen zu konfigurieren, klicken Sie auf **Weiter**.

    Eine Zusammenfassung der Testkonfiguration wird angezeigt. Für die Standardeinstellungen wird beispielsweise die folgende Nachricht ausgegeben:

    `Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds the specified threshold.`

    Basierend auf der aktuellen Testkonfiguration werden die geschätzte Nutzung und die geschätzten Tests pro Monat angezeigt.

10. Klicken Sie im Bereich 'Einstellungen' auf **Bearbeiten**, um die aktuellen Einstellungen für Ihren Test anzuzeigen. Sie können folgende Einstellungen aktualisieren:
    - **Intervall** legt fest, wie oft ein Test ausgeführt wird.
    - **Testhäufigkeit** legt fest, ob ein Test für alle Standorte gleichzeitig oder für einen abweichenden Standort für jedes Intervall ausgeführt wird. Wählen Sie **Simultan** aus, um den Test von allen Standorten aus gleichzeitig auszuführen, oder wählen Sie **Gestaffelt** aus, um den Test in jedem Intervall von einem anderen ausgewählten Standort aus auszuführen.
    - **Standorte** legt die Standorte fest, an denen der Test ausgeführt wird.

    Klicken Sie auf **Speichern**, um die Konfiguration des Tests fertigzustellen.

11. Klicken Sie auf **Fertigstellen**. Das {{site.data.keyword.prf_hubshort}}-Dashboard zeigt eine Zusammenfassung der Gesamtanzahl Ihrer Tests, eine Karte und Tabelle mit der Häufigkeit und Position der Alerts, alle synthetischen Tests, die Ihrer Anwendung zugeordnet sind, eine Tabelle Ihrer Aktivitäten und ein Liniendiagramm mit der Antwortzeit und Verfügbarkeit Ihrer Anwendung und weiterer Websites. Sie können bei Bedarf weitere Tests erstellen.
12. Sie können die Überwachungsfunktion mit dem {{site.data.keyword.alertnotificationfull}}-Service so konfigurieren, dass beim Auftreten eines Ereignisses eine Benachrichtigung gesendet wird. Weitere Informationen finden Sie unter [Benachrichtigungen aktivieren](avmon_notifications.html "Sie können die Überwachungsfunktion so konfigurieren, dass beim Auftreten eines Ereignisses eine Benachrichtigung gesendet wird.").

## Ergebnisse
{: #avmon_getstarted_results}

Die Testergebnisse werden nach Ablauf des von Ihnen im Test angegebenen Intervalls angezeigt. Das Standardintervall ist 15 Minuten.

Damit sind Sie bereit, die Verfügbarkeit Ihrer Webanwendungen zu überwachen. Die Informationen zu Antwortzeit und Verfügbarkeit für Ihre Anwendung, Website oder REST-API werden in einem Liniendiagramm zusammen mit Informationen zu kürzlich erfolgten Aktivitäten und Tests im Bereich **Antwortzeit und Verfügbarkeit** angezeigt.

Es sind zwei Handbücher verfügbar, die Informationen über die Features von
{{site.data.keyword.prf_hubshort}} enthalten.

 - **Bibliothek für Schulungsvideos** - Die Bibliothek für Schulungsvideos enthält Videos, die das Erstellen von Bluemix-Anwendungen und Bluemix-Tests, das Erstellen von Testscripts mit Selenium IDE sowie das Senden von Alerts an Slack veranschaulichen.
 - **Willkommen bei Monitoring!** - Das Dokument 'Willkommen bei Monitoring' hebt Bereiche des Dashboards hervor und erklärt die einzelnen Features von {{site.data.keyword.prf_hubshort}}.

Um ein Dokument zu öffnen, klicken Sie auf das Symbol **Hilfe** ![Hilfesymbol](images/help_icn_white_sml.jpg); klicken Sie anschließend auf das Dokument, das Sie anzeigen möchten.
