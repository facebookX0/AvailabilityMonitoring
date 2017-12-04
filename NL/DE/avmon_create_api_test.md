---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# REST-API-Test erstellen
{: #avmon_rest_api}

Erstellen Sie einen REST-API-Test, um die Antwortzeit und Verfügbarkeit Ihrer Webanwendung mithilfe der HTTP-Methoden GET, POST, PUT und DELETE zu testen.
{: shortdesc}

Testen Sie mithilfe von REST-API-Tests die Verfügbarkeit und Leistung Ihrer Webanwendung und anderer URLs in Bezug auf REST-Aufrufe.

Führen Sie die folgenden Schritte aus, um einen REST-API-Test zu erstellen.

1.  Wenn die Registerkarte **Überwachung** für Ihre Cloud Foundry-Anwendung angezeigt wird, klicken Sie auf **Neuen Test hinzufügen**.

    ![Die Registerkarte 'Überwachung' für die Cloud Foundry-Anwendung](images/avmon_tab.png)

    Wenn das {{site.data.keyword.prf_hubshort}}-Dashboard angezeigt wird, klicken Sie im Bereich 'Synthetische Tests' auf **Neuen Test hinzufügen**.

    ![Die Schaltfläche 'Neuen Test hinzufügen' im Bereich 'Synthetische Tests'](images/syn_tests_pane.jpg)

2.  Klicken Sie auf **Einzelne Aktion** auf der Seite zum Einrichten der Überwachung und klicken Sie anschließend auf der Seite 'Einzelne Aktion' auf **REST-API**.
3.  Geben Sie einen aussagefähigen Namen für Ihren Test in das Feld **Name** ein. Fügen Sie eine Beschreibung für den Zweck Ihres Tests im Feld **Beschreibung** hinzu.
4.  Wählen Sie im Abschnitt 'Anforderung' den Methodentyp in der Liste **Methode** aus und geben Sie eine **URL** ein, die Sie mit dieser Methode testen möchten. Sie haben die Wahl zwischen **GET**, **PUT**, **POST** und **DELETE**. Wenn Sie die Methode PUT oder POST auswählen, können Sie den zu testenden Inhalt des Hauptteils in das Feld **Anforderungshauptteil (optional)** eingeben.

    Im folgenden REST-API-Test wird beispielsweise mithilfe der Methode POST angefordert, dass Ihre Webanwendung nicht nur die Verfügbarkeit und Leistung der Webanwendung testet, sondern zusätzlich noch Daten akzeptiert.

    ![Beispiel für einen REST-API-Test, der die Anforderungsmethode POST verwendet](images/avmon_restapi_post.png)

5.  Sie können den Test so konfigurieren, dass ein bestimmter Header und ein bestimmter Wert enthalten sind. Geben Sie einen Headernamen und einen Headerwert in die Felder für den **Header** ein.

    Wenn für die Webanwendung, die Sie testen möchten eine Benutzeranmeldung mit Kennwort erforderlich ist, geben Sie 'Authorization' in das Feld **Headername** ein. Geben Sie das Wort 'Basic' gefolgt von einem Leerzeichen und dem Wert der Base64-Codierung für die Kombination 'benutzername:kennwort' in das Feld **Headerwert** ein.

    Beispiel: Wenn Ihr Benutzername 'Aladdin' und Ihr Kennwort 'OpenSesame' lautet, geben Sie das Wort 'Basic', gefolgt von einem Leerzeichen und dem Wert der Base64-Codierung für 'Aladdin:OpenSesame' in das Feld **Headerwert** ein.

    ![Headerfelder mit Berechtigungsnachweisen für den Test in Base64-Codierung](images/avmon_apitest_auth.png)

6.  Konfigurieren Sie die Schwellenwerte für den Warnungsalert und den kritischen Alert im Abschnitt Antwortvalidierung. Bearbeiten Sie die Felder **Wert** und **Einheit** für jede Zeile. Wenn die Antwortzeiten den Warnungsschwellenwert oder den kritischen Schwellenwert überschreiten, werden Alerts ausgelöst.

    ![Abschnitt 'Antwortvalidierung' mit Standardwarnung und kritischen Schwellenwerten](images/avmon_restapi_resp_val.png)

7.  Klicken Sie auf **Bedingung hinzufügen**, um angepasste Bedingungen für die Antwortvalidierung zu definieren und hinzuzufügen. Angepasste Bedingungen für die Antwortvalidierung werden kumulierend ausgewertet, um einen Alert zu generieren. Sie können bis zu sechs angepasste Bedingungen für Ihren Test hinzufügen.

    In {{site.data.keyword.prf_hubshort}} kann jeder Test insgesamt bis zu drei Alerts generieren. Ihr Test meldet den Alert mit der höchsten Wertigkeit, bis alle Bedingungen, die Alerts verursachen, behoben werden. Weitere Informationen finden Sie unter [Alertgenerierung in Availability Monitoring](avmon_alert_desc.html "In Availability Monitoring können in Tests bis zu drei Alerts generiert werden. In einem Test wird der Alert mit dem höchsten Schweregrad gemeldet, bis die Bedingung beseitigt ist, von der der Alert ausgelöst wird.")
    {: tip}

    Sie können die folgenden Daten validieren:

    - **Headerantwortcode**. Wählen Sie **Headerantwortcode** aus, um einen Test für einen einzelnen HTTP-Antwortcode oder für einen Bereich von HTTP-Antwortcodes durchzuführen. 
    - **Headereigenschaft**. Wählen Sie **Headereigenschaft** aus, um die Eigenschaft und den Wert für ein bestimmtes HTTP-Headerfeld zu testen. 
    - **JSON-Hauptteil**. Wählen Sie **JSON-Hauptteil** aus, um eine bestimmte Eigenschaft in einem JSON-Hauptteil zu testen.

      Geben Sie für jede Bedingung eine Eigenschaft, die getestet werden soll, in das Feld **Ziel** ein, und einen Wert, der getestet werden soll, in das Feld **Wert**. Wählen Sie im Dropdown-Menü **Operation** einen Operator aus. Wählen Sie schließlich die Alertpriorität **Warnung** oder **Kritisch** für Ihre Bedingung aus.

    Numerische Werte, die Sie in das Feld **Wert** eingeben, werden standardmäßig wie Zahlen behandelt und nicht wie Zeichenfolgen. Verwenden Sie beim Eingeben eines **Werts** für eine Bedingung zum Validieren einer Antwort Anführungszeichen (""), um zwischen einer Zeichenfolge und einer Zahl zu unterscheiden. Geben Sie beispielsweise "123" in das Feld Wert ein, um auf die Zeichenfolge 123 zu testen. Geben Sie 400 (ohne Anführungszeichen) ein, um auf die Zahl 400 zu testen.
    {: tip}

    ![Bedingungen für die Antwortvalidierung für einen REST-API-Test](images/avmon_restapi_resp_val2.png)

8.  Klicken Sie auf **Überprüfen**, um den REST-API-Test zu erstellen und zu ermitteln, ob Ihre Testanforderung gültig ist.

    {{site.data.keyword.prf_hubshort}} ermittelt die Gültigkeit des Tests mithilfe der ausgewählten HTTP-Methode und aller Anforderungsheader, die Sie für den Test definiert haben. Es findet keine Antwortvalidierung während der Testüberprüfung statt.

    Der überprüfte Test wird in der Tabelle 'Überprüfte Elemente' angezeigt. Um weitere URLs hinzuzufügen, wiederholen Sie die Schritte 3 bis 8.

9.  Um Ihre Testeinstellungen zu konfigurieren, klicken Sie auf 'Weiter'.

    Eine Zusammenfassung der Testkonfiguration wird angezeigt. Für die Standardeinstellungen wird beispielsweise die folgende Nachricht ausgegeben:

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds the specified threshold.``

    Basierend auf der aktuellen Testkonfiguration werden die geschätzte Nutzung und die geschätzte Anzahl der Tests pro Monat angezeigt.

10. Klicken Sie im Bereich Einstellungen auf **Bearbeiten**, um die aktuellen Einstellungen für Ihren Test anzuzeigen.

    Sie können das Testintervall ändern, die Testhäufigkeit und die Standorte, von denen aus die Tests gesendet werden.

    ![Bereich für Testeinstellungen mit Standardeinstellungen für einen Test](images/avmon_settings.png)

    Wählen Sie **Simultan** aus, um den Test von allen Standorten aus gleichzeitig auszuführen, oder wählen Sie **Gestaffelt** aus, um den Test in jedem Intervall von einem anderen ausgewählten Standort aus auszuführen. Klicken Sie auf **Speichern**, um die Konfiguration des Tests fertigzustellen.

11. Klicken Sie auf **Fertigstellen**. Das {{site.data.keyword.prf_hubshort}}-Dashboard zeigt eine Zusammenfassung aller Tests an, eine Karte und eine Tabelle mit der Häufigkeit und Position der Alerts, alle synthetischen Tests, die Ihrer Anwendung zugeordnet sind, eine Tabelle Ihrer Aktivitäten und ein Liniendiagramm mit der Antwortzeit und Verfügbarkeit Ihrer Anwendung und weiterer Websites.
