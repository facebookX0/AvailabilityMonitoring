---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Introduzione a Monitoraggio della disponibilità
{: #avmon_gettingstarted}

Utilizza {{site.data.keyword.prf_hublong}} per eseguire test delle
prestazioni simulati da posizioni in tutto il mondo a tutte le ore. Rileva, isola ed esegui la diagnosi
dei problemi di prestazioni in modo proattivo prima che compromettano l'attività degli utenti. Assicurati che le tue applicazioni
siano disponibili e soddisfino gli obiettivi dei tempi di risposta quando distribuisci continui aggiornamenti. Configura i raccoglitori di dati per le tue applicazioni per raccogliere i dati delle transazioni degli utenti. Utilizza questi dati in {{site.data.keyword.prf_hubshort}} per monitorare la reattività e la velocità effettiva della tua applicazione.
{: shortdesc}

## Informazioni su questa attività
{: #avmon_start_about}

{{site.data.keyword.prf_hubshort}} è disponibile come servizio nel
dominio DevOps all'interno del catalogo
{{site.data.keyword.Bluemix_notm}}. Per impostazione predefinita, è disponibile anche nel dashboard Applicazione sulla
scheda **Monitoraggio**. Puoi iniziare a monitorare la disponibilità e le prestazioni della tua applicazione immediatamente. Quando esegui il bind di {{site.data.keyword.prf_hubshort}} alla tua applicazione, viene creato automaticamente un test sintetico per monitorare l'URL dell'applicazione principale per impostazione predefinita. 

## Creazione di un test della pagina web
{: #avmon_start_procedure}

Completa la seguente procedura per aprire {{site.data.keyword.prf_hubshort}} per la tua applicazione, per creare un test della pagina web per monitorare un altro URL e per configurare gli avvisi di notifica per i tuoi test.

1.  Se disponi di un'applicazione Cloud Foundry che vuoi monitorare, fai clic sul nome dell'applicazione nella tabella **Tutte le applicazioni** nel dashboard **Applicazioni**. Se non hai ancora un'applicazione, creala e la scheda dell'applicazione si aprirà automaticamente. Le applicazioni Cloud Foundry vengono associate automaticamente a {{site.data.keyword.prf_hubshort}} quando fai clic sulla scheda Monitoraggio.
2.  Per aprire {{site.data.keyword.prf_hubshort}}, fai clic sulla scheda
**Monitoraggio**. La scheda **Monitoraggio**
visualizza tre misuratori che mostrano la **Disponibilità del test media** nelle ultime 24 ore,
lo **Stato del test corrente** e l'**Utilizzo** dell'assegnazione del tuo piano corrente. Seleziona **Aggiungi nuovo
test** per configurare e monitorare il test.

    ![Scheda Monitoraggio della disponibilità](images/avmon_tab.png)

    L'URL dell'applicazione principale viene monitorato per impostazione predefinita. Tutti gli altri URL e servizi che monitori
possono trovarsi all'interno o all'esterno di Bluemix e non devono necessariamente esser correlati all'applicazione Cloud Foundry
associata.

3.  Fai clic su **Azione singola** nella pagina Configurazione del monitoraggio; quindi, fai clic su **Pagina web** nella pagina Azione singola.
4.  Immetti un nome significativo per il tuo test nel campo **Nome**. Aggiungi una descrizione
del motivo del tuo test nel campo **Descrizione**.
5.  Immetti l'**URL** dell'applicazione web che desideri testare.
6.  Configura le soglie di avviso di avvertenza e critico per il test nella sezione Convalida risposta. Modifica **Valore** e **Unità**
per ogni riga. I tempi di risposta che superano le tue soglie critica e di avvertenza attivano gli avvisi.

    ![Sezione Convalida risposta con le soglie di avvertenza e critico predefinite.](images/avmon_webpage_resp_val.png)

7.  Utilizza la **Blacklist** e la **Whitelist** per specificare a quali URL e domini inviare richieste e quali URL e domini contribuiscono alle metriche e allo stato dei test dell'applicazione. Aggiungi URL e domini che desideri includere o bloccare nella **Whitelist** e **Blacklist**. Per ulteriori informazioni su blocco e filtro, vedi [Blocco e filtro con la whitelist e la blacklist](avmon_whitelist_blacklist.html "Utilizza la whitelist e la blacklist per determinare a quali risorse inviare le richieste e quali risorse contribuiscono alle metriche e allo stato dei test dell'applicazione. Le whitelist e le blacklist sono disponibili solo per i test delle pagine web e del funzionamento con script.").
8.  Fai clic su **Verifica** per creare il tuo test della pagina web e per determinare se la tua richiesta
di test è valida.

    {{site.data.keyword.prf_hubshort}} determina la validità del test
inviando una richiesta GET al tuo URL di test. Non avviene
alcuna convalida della risposta durante la verifica del test.

    Il test convalidato viene visualizzato nella tabella Elementi verificati. Puoi aggiungere più di un URL ripetendo i passi 3 - 8.

9.  Per configurare le impostazioni del tuo test, fai clic su
**Avanti**.

    Viene visualizzato un riepilogo della configurazione del test. Ad esempio, si visualizza il
seguente messaggio per le impostazioni predefinite:

    `Il test si verificherà: ogni 15 minuti da 3 posizioni simultaneamente per determinare se il
test supera la soglia specificata.`

    L'utilizzo stimato e i test stimati al mese vengono visualizzati in base alla tua configurazione di test corrente.

10. Nel riquadro Impostazioni, fai clic su **Modifica** per visualizzare le impostazioni correnti per il test. Puoi aggiornare le seguenti impostazioni:
    - **Intervallo** definisce la frequenza con cui viene eseguito il test.
    - **Frequenza dei test** determina se il test viene eseguito da tutte le ubicazioni simultaneamente o da una ubicazione diversa ad ogni intervallo. Seleziona **Simultaneo** per eseguire il tuo test da tutte le ubicazioni simultaneamente
o seleziona **Sfalsato** per eseguire il tuo test
da ubicazioni selezionate diverse ad ogni intervallo.
    - **Ubicazioni** determina le ubicazioni in cui verrà eseguito il test.

    Fai clic su **Salva** per terminare la configurazione del tuo
test.

11. Fai clic su **Fine**. Il dashboard {{site.data.keyword.prf_hubshort}} visualizza un riepilogo dei test totali, una mappa e una tabella che indicano la frequenza e l'ubicazione dei tuoi avvisi, tutti i test sintetici associati alla tua applicazione, una tabella delle tue attività e un grafico a linee che raffigura il tempo di risposta e la disponibilità della tua applicazione e di altri siti web. Puoi creare più test in base
alle esigenze.
12. Puoi utilizzare il servizio {{site.data.keyword.alertnotificationfull}} per configurare la funzione di monitoraggio per inviare notifiche quando si verifica un evento. Per ulteriori informazioni, vedi [Abilitazione delle notifiche](avmon_notifications.html "Configura la funzione di monitoraggio per inviare notifiche quando si verifica un evento.").

## Risultati
{: #avmon_getstarted_results}

I risultati dei test vengono visualizzati una volta trascorso l'intervallo specificato nel test. L'intervallo predefinito è 15 minuti.

Sei ora pronto a monitorare la disponibilità delle tue applicazioni web. Le informazioni sul
tempo di risposta e sulla disponibilità relative all'applicazione, al sito Web o all'API REST vengono visualizzate in un grafico a linee
insieme alle informazioni su attività e test recenti nel pannello **Tempo di risposta e Disponibilità**.

Ci sono due guide disponibili per aiutarti a conoscere le funzioni di
{{site.data.keyword.prf_hubshort}}.

 - **Libreria di esercitazioni video** - La libreria di esercitazioni video contiene video su come creare applicazioni Bluemix, creare test di Monitoraggio della disponibilità, creare script di test con Selenium IDE e inviare avvisi a Slack.
 - **Introduzione al monitoraggio** - La guida Introduzione al monitoraggio evidenzia le aree del dashboard e spiega tutte le funzioni di {{site.data.keyword.prf_hubshort}}.

Per aprire una guida, fai clic sull'icona **Guida** ![Icona Guida](images/help_icn_white_sml.jpg), quindi fai clic sulla guida che vuoi visualizzare.
