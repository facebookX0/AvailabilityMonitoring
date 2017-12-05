---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Generazione di avvisi in Monitoraggio della disponibilità
{: #avmon_alert_desc}

In {{site.data.keyword.prf_hubshort}}, i test possono generare un totale di tre avvisi. Il test segnala l'avviso con la severità più elevata finché la condizione che causa l'avviso non viene risolta.
{: shortdesc}

Viene creato un avviso separato per tre situazioni differenti:

-   Quando il tempo di risposta dell'applicazione web o dell'URL supera le soglie di avvertenza o critiche impostate per il tuo test. Ogni test misura il tempo di risposta per impostazione predefinita e attiva un avviso in base alle soglie critica e di avvertenza
per tale test.
-   Quando il tuo test restituisce un codice di risposta HTTP che indica che l'applicazione web o l'URL non è disponibile a causa di un errore del client o del server. Ogni test controlla il codice di risposta per impostazione predefinita, per determinare
se il test ha avuto esito positivo o negativo.
-   Quando il tuo test determina che una o più condizioni personalizzate sono soddisfatte, viene attivato un allarme
con la severità più elevata come definito da una o più delle tue condizioni personalizzate. {{site.data.keyword.prf_hubshort}}
considera tutte le condizioni personalizzate insieme alla determinazione dell'attivazione di un avviso o
meno. Questo avviso rimane attivo finché il test determina che
tutte le condizioni personalizzate non generino più alcun avviso critico o di avvertenza.

Quando viene emesso più di avviso, {{site.data.keyword.prf_hubshort}} segnalerà l'avviso con la severità più elevata fintanto che tutti gli avvisi sono presenti.

Ad esempio, se il tempo di risposta del test attiva un avviso di avvertenza e un'altra condizione attiva un avviso di avvertenza, il test genera un avviso critico che viene visualizzato nel dashboard {{site.data.keyword.prf_hubshort}}. Se la condizione che causa un avviso critico non è più vera, la severità del tuo avviso di test diventa "Avvertenza". Un avviso rimane
attivo finché tutte le condizioni non ne causano più uno.
