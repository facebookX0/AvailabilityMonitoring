---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Creazione di un test da un script in un repository GitHub
{: #avmon_git_script_test}

Crea un test dello script da uno script Selenium archiviato nel tuo repository GitHub. Puoi
abilitare il tuo test dello script per sincronizzarsi continuamente con tutte le modifiche che effettui nel tuo script Selenium
nel tuo repository GitHub.
{: shortdesc}

## Prima di iniziare
{: #avmon_git_prereq}

I test dello script hanno bisogno degli script Selenium per funzionare. Per poter creare un test dello script, devi
prima creare uno script Selenium. Per ulteriori informazioni sulla creazione degli script Selenium, vedi [Registrazione di script sintetici](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(Si apre in una nuova scheda o finestra)"){: new_window}.

Per creare i test dello script dagli script Selenium archiviati in un repository GitHub, devi
completare le seguenti istruzioni:

-   Abilita {{site.data.keyword.contdelivery_full}} per la tua applicazione. Per ulteriori informazioni, vedi [Continuous Delivery](../ContinuousDelivery/index.html "(Si apre in una nuova scheda o finestra)"){: new_window}.
-   Autorizza {{site.data.keyword.Bluemix_notm}} ad accedere a GitHub come parte della tua toolchain. Per ulteriori informazioni, vedi [Configurazione di GitHub](../ContinuousDelivery/toolchains_integrations.html#github "(Si apre in una nuova scheda o finestra)"){: new_window}.

## Informazioni su questa attività
{: #avmon_git_about}

Se abiliti {{site.data.keyword.contdelivery_short}} per la tua applicazione, puoi creare un test dello script che si sincronizza con uno script Selenium nel tuo repository GitHub. Se crei uno script Selenium che simula un utente della tua applicazione, puoi eseguire periodicamente un test dello script per testare le prestazioni della tua applicazione in risposta alle azioni dell'utente simulato.

## Creazione di un test che utilizza uno script GitHub
{: #avmon_git_create_test}

Per creare un test dello script, completa la seguente procedura.

1.  Se stai visualizzando la scheda Monitoraggio, fai clic su **Aggiungi nuovo test**.

    ![Scheda Monitoraggio per la tua applicazione Cloud Foundry.](images/avmon_tab.png)

    Se stai visualizzando il dashboard {{site.data.keyword.prf_hubshort}}, fai clic su **Aggiungi nuovo test** nel riquadro Test sintetici.

    ![Pulsante Aggiungi nuovo test nel riquadro Test sintetici.](images/syn_tests_pane.jpg)

2.  Fai clic su **Funzionamento con script** nella pagina Configurazione del monitoraggio. Viene visualizzata la pagina Configurazione funzionamento con script. Fai clic su
**Repository Git**.
3.  Immetti un nome significativo per il tuo test nel campo **Nome**. Aggiungi una descrizione
del motivo del tuo test nel campo **Descrizione**.
4.  Seleziona un Repository GitHub disponibile e immetti il percorso file dello script nel repository che hai scelto.
5.  Per garantire che il tuo test utilizzi continuamente la versione più recente dello script Selenium dal tuo **repository Git**, seleziona **Sincronizza automaticamente lo script con delivery pipeline**.
6.  Utilizza la **Blacklist** e la **Whitelist** per specificare a quali URL e domini inviare richieste e quali URL e domini contribuiscono alle metriche e allo stato dei test dell'applicazione. Aggiungi URL e domini che desideri includere o bloccare nella **Whitelist** e **Blacklist**. Per ulteriori informazioni su blocco e filtro, vedi [Blocco e filtro con la whitelist e la blacklist](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "Utilizza la whitelist e la blacklist per determinare a quali risorse inviare le richieste e quali risorse contribuiscono alle metriche e allo stato dei test dell'applicazione. Le whitelist e le blacklist sono disponibili solo per i test delle pagine web e del funzionamento con script.").
7.  Per configurare le impostazioni del tuo test, fai clic su
**Avanti**. Viene visualizzato un riepilogo della configurazione del test. Ad esempio, si visualizza il
seguente messaggio per le impostazioni predefinite:

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds 5 seconds``.

    L'utilizzo stimato e il numero stimato di test al mese vengono visualizzati in base alla tua configurazione del test corrente.

8.  Nel riquadro Impostazioni, fai clic su **Modifica** per visualizzare le impostazioni correnti per il test. Puoi aggiornare le seguenti impostazioni:
    - **Intervallo** definisce la frequenza con cui viene eseguito il test.
    - **Frequenza dei test** determina se il test viene eseguito da tutte le ubicazioni simultaneamente o da una ubicazione diversa ad ogni intervallo. Seleziona **Simultaneo** per eseguire il tuo test da tutte le ubicazioni simultaneamente
o seleziona **Sfalsato** per eseguire il tuo test
da ubicazioni selezionate diverse ad ogni intervallo.
    - **Soglia critica** definisce il tempo di risposta per gli avvisi critici per il test.
    - **Soglia di avvertenza** definisce il tempo di risposta per gli avvisi di avvertenza per il test.
    - **Ubicazioni** determina le ubicazioni in cui verrà eseguito il test.

    Se necessario, puoi immettere i valori delle variabili definite nel tuo script di test. Ad
esempio, se lo script richiede un nome utente e password per la connessione a un sito Web, puoi immettere i
valori per queste variabili. Puoi impostare valori diversi per le tue variabili in diverse posizioni
nella tabella **Variabili di script**.

    Fai clic su **Salva** per terminare la configurazione del tuo
test.

9.  Fai clic su **Fine**. Il dashboard {{site.data.keyword.prf_hubshort}} visualizza un riepilogo di tutti i tuoi test, una mappa e una tabella che indicano la severità e l'ubicazione dei tuoi avvisi, tutti i test sintetici associati alla tua applicazione, una tabella delle tue attività e un grafico a linee che raffigura il tempo di risposta e la disponibilità della tua applicazione e di altri siti web.
