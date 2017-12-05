---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Tempo di risposta e Disponibilità
{: #avmon_resptime_avail}

Utilizza il riquadro Tempo di risposta e Disponibilità per visualizzare il tempo di risposta, le tendenze di disponibilità, gli avvisi e le attività nel tempo. La correlazione di metriche, avvisi e attività ti consente di isolare facilmente una specifica modifica dell'applicazione o distribuzione del codice quando rilevi un impatto su un tempo di risposta.
{: shortdesc}

## Tempo di risposta
{: #avmon_resptime_graph}

Le informazioni sul tempo di risposta vengono mostrate in un grafico a linee. Per visualizzarlo, fai clic sulla scheda **Tempo di risposta**.

![Grafico dei tempi di risposta per un test nelle precedenti 24 ore.](images/avmon_rt_gr.jpg)

I tempi di risposta misurati da {{site.data.keyword.prf_hubshort}}
sono leggermente più grandi dei tempi di risposta constatati dagli utenti. {{site.data.keyword.prf_hubshort}}
simula il comportamento dell'utente reale, che aggiunge sovraccarichi alla misurazione del tempo di risposta. Il sovraccarico è causato
dai seguenti fattori:
  - {{site.data.keyword.prf_hubshort}} crea una nuova istanza Firefox
per ogni test per evitare che riproduzioni precedenti influenzino il test corrente. Gli utenti finali reali
possono avere tempi di risposta più veloci dovuti alla memorizzazione nella cache del browser.
  - {{site.data.keyword.prf_hubshort}} installa il plugin driver web Firefox
prima di ogni test.
{: tip}

I tempi di risposta individuali per i test sono rappresentati da un'icona **Punto di risposta** ![Icona Punto di risposta](images/crcl_icn_white.jpg) nel grafico a linee. Colori diversi indicano le diverse posizioni geografiche in cui è in esecuzione l'applicazione. L'asse y del grafico utilizza le icone di avviso per identificare gli intervalli della soglia critica e di avvertenza. L'icona di **avvertenza** gialla ![Icona di avvertenza gialla](images/alrt_icn_white_smll.jpg) rappresenta l'intervallo della soglia di avvertenza e l'icona **critico** rossa ![Icona Critico rossa](images/wrng_icn_white_smll.jpg) rappresenta l'intervallo della soglia critica. Fai clic sull'icona di **avvertenza** gialla ![Icona di avvertenza gialla](images/alrt_icn_white_smll.jpg) o sull'icona **critico** rossa ![Icona Critico rossa](images/wrng_icn_white_smll.jpg) per identificare facilmente le istanze di test visualizzate negli intervalli di soglia critica e di avvertenza. Per visualizzare i dettagli di una specifica istanza di test, fai clic sull'icona **Punto di risposta** ![Icona Punto di risposta](images/crcl_icn_white.jpg) nel grafico.

### Filtri

Scegli un test dal menu a discesa **Test**. Puoi filtrare i dati per 3
ore, 24 ore, 7 giorni, 30 giorni e 12 mesi. La capacità di visualizzare i dati
oltre i 12 mesi è disponibile solo agli utenti con sottoscrizioni a pagamento di {{site.data.keyword.prf_hubshort}}. Quando applichi un filtro per un intervallo di tempo superiore a
24 ore, i valori vengono visualizzati nel grafico in base al loro calcolo medio. Per visualizzare
informazioni più specifiche, fai clic sul grafico per eseguire il drill down di singoli avvisi e avvertenze. Puoi anche
utilizzare il dispositivo di scorrimento per restringere o espandere l'intervallo di tempo.

Con il grafico Tempo di risposta, puoi evidenziare e nascondere i dati da determinate ubicazioni
PoP. Per evidenziare i dati del tempo di risposta per un'ubicazione particolare, passa il mouse sul nome dell'ubicazione PoP e quindi fai clic sull'icona **Evidenzia ubicazione** ![Icona Evidenzia ubicazione](images/avmon_location_highlight.jpg). Per nascondere i dati del tempo di risposta per un'ubicazione, passa il mouse sul nome dell'ubicazione PoP e quindi fai clic sull'icona **Nascondi ubicazione** ![Icona Nascondi ubicazione](images/avmon_location_remove.jpg). Per ripristinare i dati dell'ubicazione PoP sul grafico, fai clic su **Aggiungi più ubicazioni** ![Icona Aggiungi più ubicazioni](images/icn_plus_20x20.jpg) o sulla scheda **Selezione metriche**, quindi fai clic sull'ubicazione PoP precedentemente rimossa.

### Avvisi e attività

Puoi facilmente identificare avvisi critici o di avvertenza nella riga Avvisi. Passa il mouse su un'**icona di avviso** ![Icona Avviso critico](images/avmon_crit_alert.png)![Icona Avviso di avvertenza](images/avmon_warn_alert.png) per identificare la severità e la data/ora di tale avviso. Fai clic su un'**icona di avviso** per visualizzare i dettagli di tale avviso nel **Feed metriche**.

Puoi inoltre visualizzare le attività nello stesso grafico. Le _Attività_ sono azioni che si verificano
al di fuori degli eventi definiti dall'utente. Le attività {{site.data.keyword.Bluemix_notm}} sono eventi di applicazione che si verificano in {{site.data.keyword.Bluemix_notm}}, come l'arresto, l'avvio o la ripreparazione della tua applicazione. Le attività Pipeline sono eventi che si verificano nella tua toolchain {{site.data.keyword.contdelivery_short}}, come le creazioni, le distribuzioni e i test. Fai clic su un'attività
per visualizzare le informazioni su tale attività nel **Feed metriche**. Puoi visualizzare le informazioni relative a queste attività nel riquadro Attività.

Per visualizzare le attività Pipeline nel dashboard {{site.data.keyword.prf_hubshort}}, devi prima abilitare {{site.data.keyword.contdelivery_short}} per la tua applicazione e configurare una toolchain che contiene una pipeline e il servizio {{site.data.keyword.DRA_short}}. Fai clic su **Configurazione pipeline** nel riquadro Riepilogo o nel riquadro Attività per creare una toolchain per la tua applicazione. Per ulteriori informazioni, vedi [Introduzione a Continuous Delivery](../ContinuousDelivery/index.html "(Si apre in una nuova scheda o finestra)") e [Introduzione a DevOps Insights](../DevOpsInsights/index.html#gettingstarted "(Si apre in una nuova scheda o finestra)"){: new_window}.
{: tip}

Se è presente più di un'icona di attività o di avviso accanto alle righe Avvisi e Attività, un'**icona numero** visualizza il numero di avvisi o attività in quel momento. Passa il mouse su un'**icona numero** per visualizzare i singoli avvisi o attività e fai clic su un avviso o un'attività per visualizzare le informazioni nel **Feed metriche**.

### Selezione e feed delle metriche

Per filtrare la metriche per regione geografica, fai clic su **Selezione metrica**. Fai clic su
un'ubicazione per aggiungere o rimuovere le metriche misurate in tale regione dal grafico. Fai clic su **Aggiungi più ubicazioni** per aprire la pagina Modalità di modifica del test e aggiungi un'ubicazione PoP al tuo test selezionato.

![Scheda Selezione metriche che visualizza i filtri dell'ubicazione PoP.](images/avmon_metric_sel.jpg)

Per visualizzare un elenco dei dettagli delle metriche, fai clic su **Feed metriche**. Feed metriche visualizza un elenco di istanze in cui viene realizzata una metrica.

![Scheda Feed metriche che visualizza i dettagli di un avviso di avvertenza.](images/avmon_warn_met_feed.png)

Fai clic su un'**icona di avviso**, un'**icona di attività** o su un **punto di risposta** ![Icona Punto di risposta](images/crcl_icn_white.jpg) nel grafico per aggiungere i dettagli di tale metrica al Feed metriche.

![Dettagli di un'istanza di test disponibile nel Feed metriche.](images/avmon_avail_metfeed.png)

Se applichi un filtro nel grafico Tempo di risposta per un intervallo di tempo superiore a 24 ore e fai clic su un **punto di risposta**, puoi visualizzare dei dettagli aggregati per quel giorno nel Feed metriche.

![Feed metriche che mostra i dettagli aggregati di tutte le istanze del tuo test per un giorno.](images/avmon_avail_day_met_feed.png)

Fai clic su **Zoom** per visualizzare tutti i tempi di risposta, le attività e gli
avvisi generati dal test per quel giorno nel grafico Tempo di risposta.

Per visualizzare informazioni dettagliate su un avviso o un tempo di risposta del test, fai clic su **Analisi stratificata** nel Feed metriche. Fai clic su **Avviso più prossimo** per visualizzare l'avviso più prossimo a tale istanza di test nel Feed metriche, se si è verificato un avviso. Per visualizzare informazioni dettagliate su un'attività pipeline nel servizio {{site.data.keyword.DRA_short}}, fai clic su **Visualizza Insights** nel Feed metriche.

## Disponibilità
{: #avmon_avail_graph}

Per visualizzare le informazioni sulla disponibilità delle tue applicazioni, fai clic su Disponibilità. Il grafico Disponibilità mostra la disponibilità giornaliera di ogni PoP (point of presence) per il test selezionato.

![Grafico Disponibilità che visualizza la disponibilità di test giornaliera per ubicazione per i 7 giorni precedenti.](images/avmon_avail_graph.png)

Con il grafico Disponibilità, puoi evidenziare e nascondere i dati da determinate ubicazioni
PoP. Per evidenziare i dati della disponibilità per un'ubicazione particolare, passa il mouse sul **nome ubicazione PoP**, quindi fai clic sull'icona **Evidenzia ubicazione** ![Icona Evidenzia ubicazione](images/avmon_location_highlight.jpg). Per nascondere i dati della disponibilità per un'ubicazione, passa il mouse sul **nome ubicazione PoP** e quindi fai clic sull'icona **Nascondi ubicazione** ![Icona Nascondi ubicazione](images/avmon_location_remove.jpg). Per ripristinare i dati dell'ubicazione PoP sul grafico, fai clic sulla scheda **Selezione
metriche** e quindi fai clic sull'ubicazione PoP precedentemente rimossa.

Passa con il mouse su un punto del grafico per visualizzare la frequenza di errore e il numero di istanze di test per un'ubicazione
e un giorno in particolare. Fai clic su un punto del grafico per visualizzare queste informazioni nel Feed metriche.

![Disponibilità del test nel PoP Dallas visualizzata nel Feed metriche.](images/avmon_avail_metric.png)

Fai clic su **Zoom** per filtrare il grafico Disponibilità e il grafico Tempo di risposta per visualizzare le informazioni per il giorno selezionato.
