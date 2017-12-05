---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Test sintetici
{: #avmon_synth_tests}

Nel riquadro Test sintetici, puoi creare, modificare, eliminare e visualizzare i test sintetici che monitorano le prestazioni e la disponibilità delle tue applicazioni. I test vengono visualizzati in una vista a elenco o a schede nel riquadro Test sintetici.
{: shortdesc}

![Riquadro Test sintetici.](images/syn_tests_pane.jpg)

Ogni scheda di test mostra informazioni sul test:

- **Disponibilità** visualizza la percentuale di disponibilità del test nelle ultime 24 ore.
- **Stato**  visualizza lo stato corrente del test. Lo stato può essere Critico, Avvertenza, Normale, Non riuscito, Inattivo o Sconosciuto.
- **Tempo di risposta medio** visualizza il tempo di risposta medio del test nelle ultime 24 ore.

Puoi monitorare tre tipi di test diversi:

- I test dell'**API REST** segnalano il tempo di risposta di una chiamata REST. Sono supportati tutti formati della richiesta HTTP, come GET, POST, PUT e
DELETE .
- I test della **pagina web** segnalano il tempo di risposta per il caricamento del sito web all'URL immesso.
- I test del **Funzionamento con script** monitorano gli script Selenium che crei per simulare le interazioni di un utente con un sito Web. Ad
esempio, puoi creare uno script Selenium che simuli un utente che accede alla tua applicazione. Puoi quindi eseguire periodicamente questo script per testare le prestazioni della tua applicazione in risposta alle azioni dell'utente automatizzate dallo script. Puoi caricare uno script o aggiungerne uno da un repository GitHub. Per ulteriori informazioni sulla creazione degli script Selenium, vedi [Registrazione di script sintetici](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(Si apre in una nuova scheda o finestra)"){: new_window}.

Per aggiungere un altro test, fai clic su **Aggiungi nuovo test**.

Per arrestare, avviare, eliminare o modificare un test sintetico, fai clic sull'icona **Azioni** ![Icona Azioni](images/actions_icn_white_smll.jpg) e seleziona l'azione desiderata. Per visualizzare i dettagli di Analisi stratificata del test, fai clic sul test.

Per visualizzare l'utilizzo specifico di ogni test sintetico, fai clic sull'icona **Costo** ![Icona Costo](images/cost_icn_white_smll.jpg). Se hai sottoscritto al piano di pagamento, il tuo utilizzo viene visualizzato in punti dati.
