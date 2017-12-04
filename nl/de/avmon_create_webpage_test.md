---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Webseitentest erstellen
{: #avmon_webpage_test}

Erstellen Sie einen Webseitentest, um die Verfügbarkeit Ihrer Webanwendung zu testen und die erforderliche Zeit zum Öffnen der betreffenden Seite zu überwachen.
{: shortdesc}

## Informationen zu diesem Vorgang
{: #avmon_webpage_about}

Webseitentests überwachen die Antwortzeit beim Laden der URL Ihrer Webanwendung. Erstellen Sie einen Webseitentest, um die Verfügbarkeit und Antwortzeit Ihrer Webanwendung zu überwachen.

## Webseitentest erstellen und konfigurieren
{: #avmon_create_web_test}

Führen Sie die folgenden Schritte aus, um einen Webseitentest zu erstellen.

1.  Wenn die Registerkarte 'Überwachung' angezeigt wird, klicken Sie auf **Neuen Test hinzufügen**.

    ![Die Registerkarte 'Überwachung' für die Cloud Foundry-Anwendung](images/avmon_tab.png)

    Wenn das {{site.data.keyword.prf_hubshort}}-Dashboard angezeigt wird, klicken Sie im Bereich 'Synthetische Tests' auf **Neuen Test hinzufügen**.

    ![Die Schaltfläche 'Neuen Test hinzufügen' im Bereich 'Synthetische Tests'](images/syn_tests_pane.jpg)

2.  Klicken Sie auf **Einzelne Aktion** auf der Seite zum Einrichten der Überwachung und klicken Sie anschließend auf der Seite 'Einzelne Aktion' auf **Webseite**.
3.  Geben Sie einen aussagefähigen Namen für Ihren Test in das Feld **Name** ein. Fügen Sie eine Beschreibung für den Zweck Ihres Tests im Feld **Beschreibung** hinzu.
4.  Geben Sie die **URL** der Webanwendung ein, die Sie testen möchten.
5.  Konfigurieren Sie die Schwellenwerte für den Warnungsalert und den kritischen Alert im Abschnitt 'Antwortvalidierung'. Bearbeiten Sie die Felder **Wert** und **Einheit** für jede Zeile. Wenn die Antwortzeiten den Warnungsschwellenwert oder den kritischen Schwellenwert überschreiten, werden Alerts ausgelöst.

    ![Abschnitt 'Antwortvalidierung' mit Standardwarnung und kritischen Schwellenwerten](images/avmon_webpage_resp_val.png)

6.  Verwenden Sie die **Blacklist** und **Whitelist**, um anzugeben, an welche URLs und Domänen Anforderungen gesendet werden sollen, und welche URLs und Domänen zu den Metriken und Statuswerten Ihrer Anwendungstests beitragen sollen. Fügen Sie die URLs und Domänen, die Sie einschließen oder blockieren möchten, jeweils zur **Whitelist** bzw. **Blacklist** hinzu. Weitere Informationen zum Blockieren und Filtern finden Sie unter [Blockieren und Filtern mit Whitelist und Blacklist](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "Verwenden Sie die Whitelist und Blacklist, um festzulegen, an welche Ressourcen Anfragen gesendet werden sollen, und welche Ressourcen mit ihren Daten zu den Metriken und Statuswerten der Anwendungstests beitragen sollen. Whitelist und Blacklist sind nur für Tests von Webseiten und des scriptgesteuerten Verhaltens verfügbar.").
7.  Klicken Sie auf **Überprüfen**, um den Webseitentest zu erstellen und um zu ermitteln, ob Ihre Testanforderung gültig ist.

    {{site.data.keyword.prf_hubshort}} ermittelt die Gültigkeit des Tests, indem eine GET-Anforderung an Ihre Test-URL gesendet wird. Es findet keine Antwortvalidierung während der Testüberprüfung statt.

    Der überprüfte Test wird in der Tabelle 'Überprüfte Elemente' angezeigt. Um weitere URLs hinzuzufügen, wiederholen Sie die Schritte 3 bis 7.

8.  Um Ihre Testeinstellungen zu konfigurieren, klicken Sie auf **Weiter**. Eine Zusammenfassung der Testkonfiguration wird angezeigt. Für die Standardeinstellungen wird beispielsweise die folgende Nachricht ausgegeben:

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds the specified threshold``.

    Basierend auf der aktuellen Testkonfiguration werden die geschätzte Nutzung und Anzahl der Tests pro Monat angezeigt.

9.  Klicken Sie im Bereich Einstellungen auf **Bearbeiten**, um die aktuellen Einstellungen für Ihren Test anzuzeigen. Sie können folgende Einstellungen aktualisieren:
    - **Intervall** legt fest, wie oft ein Test ausgeführt wird.
    - **Testhäufigkeit** legt fest, ob ein Test für alle Standorte gleichzeitig oder für einen abweichenden Standort für jedes Intervall ausgeführt wird. Wählen Sie **Simultan** aus, um den Test von allen Standorten aus gleichzeitig auszuführen, oder wählen Sie **Gestaffelt** aus, um den Test in jedem Intervall von einem anderen ausgewählten Standort aus auszuführen.
    - **Standorte** legt die Standorte fest, an denen der Test ausgeführt wird.

    Klicken Sie auf **Speichern**, um die Konfiguration des Tests fertigzustellen.

10. Klicken Sie auf **Fertigstellen**. Das {{site.data.keyword.prf_hubshort}}-Dashboard zeigt eine Zusammenfassung aller Tests an, eine Karte und eine Tabelle mit der Häufigkeit und Position der Alerts, alle synthetischen Tests, die Ihrer Anwendung zugeordnet sind, eine Tabelle Ihrer Aktivitäten und ein Liniendiagramm mit der Antwortzeit und Verfügbarkeit Ihrer Anwendung und weiterer Websites.
