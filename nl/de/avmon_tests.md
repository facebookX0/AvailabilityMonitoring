---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Synthetische Tests
{: #avmon_synth_tests}

Im Bereich 'Synthetische Tests' können Sie synthetische Tests erstellen, bearbeiten, löschen und anzeigen, mit denen die Leistung und Verfügbarkeit Ihrer Anwendungen überwacht werden. In diesem Bereich werden Tests in einer Listen- oder Kartenansicht angezeigt.
{: shortdesc}

![Der Bereich für synthetische Tests](images/syn_tests_pane.jpg)

Auf jeder Testkarte werden die Informationen zum Test angezeigt:

- Unter **Verfügbarkeit** wird die prozentuale Verfügbarkeit des Tests in den vergangenen 24 Stunden angezeigt.
- Unter **Status** wird der aktuelle Status des Tests angezeigt. Der Status kann 'Kritisch', 'Warnung', 'Normal', 'Fehlgeschlagen', 'Inaktiv' oder 'Unbekannt' lauten.
- Unter **Durchschnittliche Antwortzeit** wird die durchschnittliche Antwortzeit des Tests in den vergangenen 24 Stunden angezeigt.

Sie können drei unterschiedlichen Testtypen überwachen:

- Von Tests des Typs **REST-API** wird die Antwortzeit eines REST-Aufrufs gemeldet. Alle HTTP-Anforderungsformate wie GET, POST, PUT und DELETE werden unterstützt.
- Von Tests des Typs **Webseite** wird die Antwortzeit beim Laden der Webseite der URL gemeldet, die Sie eingeben.
- Von Tests des Typs **Scriptgesteuertes Verhalten** werden Selenium-Scripts überwacht, die Sie erstellen, um die Interaktionen eines Benutzers mit einer Website zu imitieren. Sie können z. B. ein Selenium-Script erstellen, das einen Benutzer abbildet, der sich bei Ihrer Anwendung anmeldet. Sie führen dieses Script in regelmäßigen Abständen aus, um die Leistung Ihrer Anwendung als Antwort auf die durch das Script automatisierten Benutzeraktionen zu testen. Sie können ein Script hochladen oder ein Script aus einem GitHub-Repository hinzufügen. Weitere Informationen zum Erstellen von Selenium-Scripts finden Sie unter [Synthetische Scripts aufzeichnen](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(Wird in neuer Registerkarte oder neuem Fenster geöffnet)"){: new_window}.

Zum Hinzufügen eines weiteren Tests klicken Sie auf **Neuen Test hinzufügen**.

Zum Stoppen, Starten, Löschen oder Bearbeiten eines synthetischen Tests klicken Sie auf das Symbol **Aktionen** ![Symbol 'Aktionen'](images/actions_icn_white_smll.jpg) und klicken anschließend auf die jeweils gewünschte Aktion. Klicken Sie auf den Test, wenn Sie die Details der Aufgliederung anzeigen möchten.

Wenn Sie die konkrete Verwendung jedes einzelnen synthetischen Tests anzeigen möchten, klicken Sie auf das Symbol **Kosten** ![Symbol 'Kosten'](images/cost_icn_white_smll.jpg). Falls Sie einen kostenpflichtigen Plan abonniert haben, wird die Verwendung in Datenpunkten angezeigt.
