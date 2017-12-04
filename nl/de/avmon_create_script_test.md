---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Scripttest aus einem hochgeladenen Script erstellen
{: #avmon_upload_script_test}

Laden Sie ein Selenium-Script hoch, um einen Scripttest zu erstellen, der die Verfügbarkeit und Leistung Ihrer Webanwendung in Bezug auf simuliertes Benutzerverhalten testet.
{: shortdesc}

## Vorbereitungen
{: #avmon_script_prereq}

Für funktionsfähige Scripttests sind Selenium-Scripts erforderlich. Vor dem Erstellen eines Scripttests müssen Sie zunächst ein Selenium-Script erstellen. Weitere Informationen zum Erstellen von Selenium-Scripts finden Sie unter [Synthetische Scripts aufzeichnen](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(Wird in neuer Registerkarte oder neuem Fenster geöffnet)"){: new_window}.

## Informationen zu diesem Vorgang
{: #avmon_script_about}

Erstellen Sie einen Scripttest, um ein Selenium-Script zu überwachen, von dem die Interaktionen des Benutzers mit der Webanwendung simuliert werden. Sie können ein Selenium-Script erstellen, das einen Benutzer Ihrer App nachahmt, der sich an Ihrer Anwendung anmeldet, und anschließend regelmäßig einen Scripttest ausführen, um die Leistung Ihrer Anwendung in Bezug auf die simulierten Benutzeraktionen zu testen.

## Test mit hochgeladenem Script erstellen
{: #avmon_script_create_test}

Führen Sie die folgenden Schritte aus, um einen Scripttest zu erstellen.

1.  Wenn die Registerkarte 'Überwachung' angezeigt wird, klicken Sie auf **Neuen Test hinzufügen**.

    ![Die Registerkarte 'Überwachung' für die Cloud Foundry-Anwendung](images/avmon_tab.png)

    Wenn das {{site.data.keyword.prf_hubshort}}-Dashboard angezeigt wird, klicken Sie im Bereich 'Synthetische Tests' auf **Neuen Test hinzufügen**.

    ![Die Schaltfläche 'Neuen Test hinzufügen' im Bereich 'Synthetische Tests'](images/syn_tests_pane.jpg)

2.  Klicken Sie auf der Seite zum Einrichten der Überwachung auf **Scriptgesteuertes Verhalten**. Die Seite zum Einrichten des scriptgesteuerten Verhaltens wird angezeigt. Klicken Sie auf **Datei hochladen**.

    Wenn Sie zu einem späteren Zeitpunkt zur Bearbeitung dieses Tests zurückkehren, können Sie die hochgeladene Scriptdatei herunterladen. Klicken Sie auf das Symbol **Download** ![Downloadsymbol](images/download_icn_white_smll.jpg), um das Script herunterzuladen.

3.  Geben Sie einen aussagefähigen Namen für Ihren Test in das Feld **Name** ein. Fügen Sie eine Beschreibung für den Zweck Ihres Tests im Feld **Beschreibung** hinzu.
4.  Klicken Sie auf **Durchsuchen**, um eine Scriptdatei zu suchen und hochzuladen.
5.  Verwenden Sie die **Blacklist** und **Whitelist**, um anzugeben, an welche URLs und Domänen Anforderungen gesendet werden sollen, und welche URLs und Domänen zu den Metriken und Statuswerten Ihrer Anwendungstests beitragen sollen. Fügen Sie die URLs und Domänen, die Sie einschließen oder blockieren möchten, jeweils zur **Whitelist** bzw. **Blacklist** hinzu. Weitere Informationen zum Blockieren und Filtern finden Sie unter [Blockieren und Filtern mit Whitelist und Blacklist](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "Verwenden Sie die Whitelist und Blacklist, um festzulegen, an welche Ressourcen Anfragen gesendet werden sollen, und welche Ressourcen mit ihren Daten zu den Metriken und Statuswerten der Anwendungstests beitragen sollen. Whitelist und Blacklist sind nur für Tests von Webseiten und des scriptgesteuerten Verhaltens verfügbar.").
6.  Um Ihre Testeinstellungen zu konfigurieren, klicken Sie auf **Weiter**. Eine Zusammenfassung der Testkonfiguration wird angezeigt. Für die Standardeinstellungen wird beispielsweise die folgende Nachricht ausgegeben:

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds 5 seconds``.

    Basierend auf der aktuellen Testkonfiguration werden die geschätzte Nutzung und Anzahl der Tests pro Monat angezeigt.

7.  Klicken Sie im Bereich Einstellungen auf **Bearbeiten**, um die aktuellen Einstellungen für Ihren Test anzuzeigen. Sie können folgende Einstellungen aktualisieren:
    - **Intervall** legt fest, wie oft ein Test ausgeführt wird.
    - **Testhäufigkeit** legt fest, ob ein Test für alle Standorte gleichzeitig oder für einen abweichenden Standort für jedes Intervall ausgeführt wird. Wählen Sie **Simultan** aus, um den Test von allen Standorten aus gleichzeitig auszuführen, oder wählen Sie **Gestaffelt** aus, um den Test in jedem Intervall von einem anderen ausgewählten Standort aus auszuführen.
    - **Kritischer Schwellenwert** legt die Antwortzeit für kritische Alerts für einen Test fest.
    - **Warnungsschwellenwert** legt die Antwortzeit für Schwellenwerte für Warnungen für einen Test fest.
    - **Standorte** legt die Standorte fest, an denen der Test ausgeführt wird.

    Falls erforderlich, können Sie die Werte für Variablen eingeben, die in Ihrem Testscript definiert sind. Wenn Ihr Script z. B. einen Benutzernamen und ein Kennwort erfordert, um die Verbindung zu einer Website herzustellen, können Sie die Werte für diese Variablen eingeben. Sie können an verschiedenen Standorten unterschiedliche Werte für Ihre Variablen in der Tabelle **Scriptvariablen** festlegen.

    Klicken Sie auf **Speichern**, um die Konfiguration des Tests fertigzustellen.

8.  Klicken Sie auf **Fertigstellen**. Das {{site.data.keyword.prf_hubshort}}-Dashboard zeigt eine Zusammenfassung aller Tests an, eine Karte und eine Tabelle mit der Häufigkeit und Position der Alerts, alle synthetischen Tests, die Ihrer Anwendung zugeordnet sind, eine Tabelle Ihrer Aktivitäten und ein Liniendiagramm mit der Antwortzeit und Verfügbarkeit Ihrer Anwendung und weiterer Websites.
