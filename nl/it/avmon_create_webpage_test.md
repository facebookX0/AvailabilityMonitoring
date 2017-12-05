---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Creazione di un test della pagina web
{: #avmon_webpage_test}

Crea un test della pagina web per testare la disponibilità della tua applicazione web e per monitorare il tempo necessario per aprire tale pagina.
{: shortdesc}

## Informazioni su questa attività
{: #avmon_webpage_about}

I test della pagina web segnalano il tempo di risposta per il caricamento dell'URL della tua applicazione web. Crea un test della pagina web per monitorare la disponibilità e il tempo di risposta dell'applicazione web.

## Creazione e configurazione del test della pagina web
{: #avmon_create_web_test}

Per creare un test della pagina web, completa la seguente procedura.

1.  Se stai visualizzando la scheda Monitoraggio, fai clic su **Aggiungi nuovo test**.

    ![Scheda Monitoraggio per la tua applicazione Cloud Foundry.](images/avmon_tab.png)

    Se stai visualizzando il dashboard {{site.data.keyword.prf_hubshort}}, fai clic su **Aggiungi nuovo test** nel riquadro Test sintetici.

    ![Pulsante Aggiungi nuovo test nel riquadro Test sintetici.](images/syn_tests_pane.jpg)

2.  Fai clic su **Azione singola** nella pagina Configurazione del monitoraggio; quindi, fai clic su **Pagina web** nella pagina Azione singola.
3.  Immetti un nome significativo per il tuo test nel campo **Nome**. Aggiungi una descrizione
del motivo del tuo test nel campo **Descrizione**.
4.  Immetti l'**URL** dell'applicazione web che desideri testare.
5.  Configura le soglie di avviso di avvertenza e critico per il test nella sezione Convalida risposta. Modifica **Valore** e **Unità**
per ogni riga. I tempi di risposta che superano le tue soglie critica e di avvertenza attivano gli avvisi.

    ![Sezione Convalida risposta con le soglie di avvertenza e critico predefinite.](images/avmon_webpage_resp_val.png)

6.  Utilizza la **Blacklist** e la **Whitelist** per specificare a quali URL e domini inviare richieste e quali URL e domini contribuiscono alle metriche e allo stato dei test dell'applicazione. Aggiungi URL e domini che desideri includere o bloccare nella **Whitelist** e **Blacklist**. Per ulteriori informazioni su blocco e filtro, vedi [Blocco e filtro con la whitelist e la blacklist](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "Utilizza la whitelist e la blacklist per determinare a quali risorse inviare le richieste e quali risorse contribuiscono alle metriche e allo stato dei test dell'applicazione. Le whitelist e le blacklist sono disponibili solo per i test delle pagine web e del funzionamento con script.").
7.  Fai clic su **Verifica** per creare il tuo test della pagina web e per determinare se la tua richiesta
di test è valida.

    {{site.data.keyword.prf_hubshort}} determina la validità del test
inviando una richiesta GET al tuo URL di test. Non avviene
alcuna convalida della risposta durante la verifica del test.

    Il test convalidato viene visualizzato nella tabella Elementi verificati. Puoi aggiungere più URL ripetendo i passi 3 - 7.

8.  Per configurare le impostazioni del tuo test, fai clic su
**Avanti**. Viene visualizzato un riepilogo della configurazione del test. Ad esempio, si visualizza il
seguente messaggio per le impostazioni predefinite:

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds the specified threshold``.

    L'utilizzo stimato e il numero stimato di test al mese vengono visualizzati in base alla tua configurazione del test corrente.

9.  Nel riquadro Impostazioni, fai clic su **Modifica** per visualizzare le impostazioni correnti per il test. Puoi aggiornare le seguenti impostazioni:
    - **Intervallo** definisce la frequenza con cui viene eseguito il test.
    - **Frequenza dei test** determina se il test viene eseguito da tutte le ubicazioni simultaneamente o da una ubicazione diversa ad ogni intervallo. Seleziona **Simultaneo** per eseguire il tuo test da tutte le ubicazioni simultaneamente
o seleziona **Sfalsato** per eseguire il tuo test
da ubicazioni selezionate diverse ad ogni intervallo.
    - **Ubicazioni** determina le ubicazioni in cui verrà eseguito il test.

    Fai clic su **Salva** per terminare la configurazione del tuo
test.

10. Fai clic su **Fine**. Il dashboard {{site.data.keyword.prf_hubshort}} visualizza un riepilogo di tutti i tuoi test, una mappa e una tabella che indicano la severità e l'ubicazione dei tuoi avvisi, tutti i test sintetici associati alla tua applicazione, una tabella delle tue attività e un grafico a linee che raffigura il tempo di risposta e la disponibilità della tua applicazione e di altri siti web.
