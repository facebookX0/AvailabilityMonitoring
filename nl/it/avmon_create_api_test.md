---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Creazione di un test API REST
{: #avmon_rest_api}

Crea un test API REST per testare il tempo di risposta e la disponibilità dell'applicazione web utilizzando i seguenti metodi HTTP: GET, POST, PUT e DELETE.
{: shortdesc}

Utilizza i test API REST per monitorare la disponibilità e le prestazioni dell'applicazione web e di altri URL in risposta alle chiamate REST.

Per creare un test API REST, completa la seguente procedura.

1.  Se stai visualizzando la scheda **Monitoraggio** per la tua applicazione Cloud Foundry, fai clic su **Aggiungi nuovo test**.

    ![Scheda Monitoraggio per la tua applicazione Cloud Foundry.](images/avmon_tab.png)

    Se stai visualizzando il dashboard {{site.data.keyword.prf_hubshort}}, fai clic su **Aggiungi nuovo test** nel riquadro Test sintetici.

    ![Pulsante Aggiungi nuovo test nel riquadro Test sintetici.](images/syn_tests_pane.jpg)

2.  Fai clic su **Azione singola** nella pagina Configurazione del monitoraggio; quindi, fai clic su **API REST** nella pagina Azione singola.
3.  Immetti un nome significativo per il tuo test nel campo **Nome**. Aggiungi una descrizione
del motivo del tuo test nel campo **Descrizione**.
4.  Nella sezione Richiesta, seleziona il tipo di metodo dall'elenco **Metodo** e immetti un **URL** che desideri testare con questo metodo. Puoi scegliere tra
**GET**, **PUT**, **POST** o
**DELETE**. Se scegli il metodo PUT o POST, puoi immettere il contenuto del corpo da testare nel campo **Corpo richiesta (facoltativo)**.

    Ad esempio, il seguente test API REST utilizza il metodo POST per richiedere che la tua applicazione web accetti i dati oltre a testare la disponibilità e le prestazioni di tale applicazione web.

    ![Esempio di test API REST che utilizza il metodo di richiesta POST.](images/avmon_restapi_post.png)

5.  Puoi configurare il tuo test per includere un valore e un'intestazione in particolare. Immetti un nome e un valore dell'intestazione
nei campi **Intestazione**.

    Se l'applicazione web che desideri testare richiede un accesso utente e password, immetti "Autorizzazione" nel campo **Nome intestazione**. Immetti la parola "Basic", uno spazio e il valore con codifica base64 dei tuoi username:password nel campo **Valore intestazione**.

    Ad esempio, se il tuo nome utente è Aladdin e la tua password è OpenSesame, immetti la parola "Basic", uno spazio e il valore con codifica base64 per Aladdin:OpenSesame nel campo **Valore intestazione**.

    ![Campi di intestazione che descrivono le credenziali di autorizzazione del test in base64.](images/avmon_apitest_auth.png)

6.  Configura le soglie di avviso di avvertenza e critico per il test nella sezione Convalida risposta. Modifica **Valore** e **Unità**
per ogni riga. I tempi di risposta che superano le tue soglie critica e di avvertenza attivano gli avvisi.

    ![Sezione Convalida risposta con le soglie di avvertenza e critico predefinite.](images/avmon_restapi_resp_val.png)

7.  Fai clic su **Aggiungi condizione** per definire e aggiungere le condizioni
di convalida della risposta personalizzate. Le condizioni di convalida della risposta personalizzate vengono valutate insieme alla generazione
di un avviso. Puoi definire e aggiungere fino a sei condizioni personalizzate al tuo test.

    In {{site.data.keyword.prf_hubshort}}, ogni test può generare
fino a un totale di tre avvisi. Il test segnala l'avviso con la severità più elevata finché tutte le condizioni che causano gli avvisi non vengono risolte. Per ulteriori informazioni, vedi [Generazione di avvisi in Monitoraggio della disponibilità](avmon_alert_desc.html "In Monitoraggio della disponibilità, i test possono generare un totale di tre avvisi. Il test segnala l'avviso con la severità più elevata finché la condizione che causa l'avviso non viene risolta.")
    {: tip}

    Puoi convalidare i seguenti dati:

    - **Codice risposta intestazione**. Seleziona **Codice risposta intestazione** per verificare un codice o un intervallo
di codici di risposta HTTP.
    - **Proprietà intestazione**. Seleziona **Proprietà intestazione** per verificare la proprietà e il valore di un campo di intestazione HTTP particolare.
    - **Json corpo**. Seleziona **Json corpo** per verificare una proprietà particolare da un corpo JSON

      Per ogni condizione, immetti una proprietà da verificare per il campo **Destinazione**, e
un valore da verificare per il campo **Valore**. Seleziona un operatore dal menu a discesa
**Operazione**. Infine, scegli una Severità avviso di **Avvertenza** o **Critico** per la tua condizione.

    I valori numerici che hai immesso nel campo **Valore** sono trattati come numeri
e non stringhe per impostazione predefinita. Quando immetti un **Valore** per una condizione di convalida della risposta,
utilizza le virgolette "" per la distinzione tra una stringa e un numero. Ad esempio, per testare la stringa 123, immetti "123" nel campo Valore. Per controllare il numero
400, immetti 400 senza alcuna virgoletta.
    {: tip}

    ![Condizioni di convalida della risposta per un test API REST](images/avmon_restapi_resp_val2.png)

8.  Fai clic su **Verifica** per creare il tuo test API REST e per determinare se la tua richiesta
di test sia valida.

    {{site.data.keyword.prf_hubshort}} determina la validità del test
utilizzando il metodo HTTP selezionato e le intestazioni della richiesta definite per il test. Non avviene
alcuna convalida della risposta durante la verifica del test.

    Il test convalidato viene visualizzato nella tabella Elementi verificati. Puoi aggiungere più di un URL ripetendo i passi 3 - 8.

9.  Per configurare le impostazioni del test, fai clic su Avanti.

    Viene visualizzato un riepilogo della configurazione del test. Ad esempio, si visualizza il
seguente messaggio per le impostazioni predefinite:

    ``Il test si verificherà: ogni 15 minuti da 3 posizioni simultaneamente per determinare se il
test supera la soglia specificata.``

    L'utilizzo stimato e il numero stimato di test al mese vengono visualizzati in base alla tua configurazione del test corrente.

10. Nel riquadro Impostazioni, fai clic su **Modifica** per visualizzare le impostazioni correnti per il test.

    Puoi modificare l'intervallo dei test,
la frequenza di test e le ubicazioni da cui vengono inviati i test.

    ![Riquadro Impostazioni del test che visualizza le impostazioni predefinite per un test.](images/avmon_settings.png)

    Seleziona **Simultaneo** per eseguire il tuo test da tutte le ubicazioni simultaneamente
o seleziona **Sfalsato** per eseguire il tuo test
da ubicazioni selezionate diverse ad ogni intervallo. Fai clic su **Salva** per terminare la configurazione del tuo
test.

11. Fai clic su **Fine**. Il dashboard {{site.data.keyword.prf_hubshort}} visualizza un riepilogo di tutti i tuoi test, una mappa e una tabella che indicano la severità e l'ubicazione dei tuoi avvisi, tutti i test sintetici associati alla tua applicazione, una tabella delle tue attività e un grafico a linee che raffigura il tempo di risposta e la disponibilità della tua applicazione e di altri siti web.
