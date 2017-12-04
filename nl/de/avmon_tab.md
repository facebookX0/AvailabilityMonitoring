---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Auf Availability Monitoring zugreifen
{: #avmon_tab}

Über die Registerkarte **Überwachung** besteht Zugriff auf das {{site.data.keyword.prf_hubshort}}-Dashboard. Auf der Registerkarte **Überwachung** für die Cloud Foundry-Anwendung werden Übersichtsdaten zur Verfügbarkeit und zum Status von Tests sowie Details und Nutzungsdaten zum Serviceabonnement angezeigt.
{: shortdesc}

Führen Sie die folgenden Schritte aus, um auf {{site.data.keyword.prf_hubshort}} zuzugreifen:

1.  Klicken Sie auf den Namen einer Cloud Foundry-Anwendung im **Apps**-Dashboard.
2.  Klicken Sie auf die Registerkarte **Überwachung**.

Auf der Registerkarte **Überwachung** werden drei Messanzeigen angezeigt, von denen die **Durchschnittliche Testverfügbarkeit** in den letzten 24 Stunden, der **Aktuelle Teststatus** aller Tests und die **Servicenutzung** der Anwendung für den aktuellen Plan angezeigt werden.

![Registerkarte 'Availability Monitoring'](images/avmon_tab.png)

Sie können konfigurieren, wie von {{site.data.keyword.prf_hubshort}} der Wert für **Durchschnittliche Testverfügbarkeit** berechnet wird; wählen Sie hierzu die Tests aus, die in die Berechnung der Verfügbarkeit einfließen sollen. Klicken Sie auf das Symbol **Pfeil** ![Pfeilsymbol](images/arrow_dwn_icn_white.jpg) in der Messanzeige **Durchschnittliche Testverfügbarkeit**, um die Testkarten anzuzeigen; klicken Sie anschließend auf **Berechnung der Verfügbarkeit**. Klicken Sie auf eine Karte, um diese zur Berechnung hinzuzufügen oder aus der Berechnung zu entfernen. Nicht einbezogene Testkarten werden abgeblendet dargestellt. Wenn Sie diese Schritte fertiggestellt haben, klicken Sie auf **Ich bin fertig**. Die Messanzeige **Durchschnittliche Testverfügbarkeit** wird aktualisiert.

Sie können den Status aller Tests anzeigen, indem Sie auf das Symbol **Pfeil** ![Pfeilsymbol](images/arrow_dwn_icn_white.jpg) in der Messanzeige **Aktueller Teststatus** klicken. Die Testkarten für Ihre Tests werden angezeigt.

Klicken Sie zum Zugreifen auf das {{site.data.keyword.prf_hubshort}}-Dashboard auf **Überwachungsdetails anzeigen**. Im {{site.data.keyword.prf_hubshort}}-Dashboard können Sie die Verfügbarkeit der Anwendung auf der Basis synthetischer Tests überwachen. Sie können auch die Reaktionsfähigkeit und den Durchsatz der Anwendung auf der Basis von Benutzertransaktionsdaten überwachen, die von den Datenkollektoren bereitgestellt werden.

Klicken Sie auf **Alle Tests anzeigen**, wenn Sie Ihre Tests im Fensterbereich Synthetische Tests anzeigen und bearbeiten möchten. Zum Erstellen eines Tests klicken Sie auf **Neuen Test hinzufügen**.

Klicken Sie zum Herunterladen einer Berichtsdatei im CSV-Format mit den monatlichen, wöchentlichen und täglichen Durchschnittswerten für Verfügbarkeit und Antwortzeit für die Anwendung auf das Symbol **Download** ![Symbol 'Download'](images/download_icn_white_smll.jpg).
