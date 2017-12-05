---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}


# Attività
{: #avmon_activities}

Visualizza le informazioni relative alle attività nel riquadro Attività. Le _attività_ corrispondono alle azioni che si verificano al di fuori degli eventi definiti dall'utente.
{: shortdesc}

Il riquadro Attività visualizza le informazioni su tutte le attività della tua applicazione, come l'avvio, l'arresto e la distribuzione, nelle ultime 24 ore.

![Riquadro Attività nel dashboard Monitoraggio della disponibilità.](images/avmon_activity_pane.png)

Le attività {{site.data.keyword.Bluemix_notm}} sono eventi di applicazione che si verificano in {{site.data.keyword.Bluemix_notm}}, come l'arresto, l'avvio o la ripreparazione della tua applicazione. Le attività Pipeline sono eventi che vengono eseguiti nella tua pipeline DevOps,
come le creazioni, le distribuzioni e i test. L'intestazione della tabella mostra totali separati per le attività {{site.data.keyword.Bluemix_notm}} e le attività Pipeline. Puoi filtrare per attività di Origine per visualizzare attività {{site.data.keyword.Bluemix_notm}} o attività Pipeline facendo clic sulle icone {{site.data.keyword.Bluemix_notm}} o Pipeline nell'intestazione del riquadro Attività.

Per visualizzare le attività Pipeline nel dashboard {{site.data.keyword.prf_hubshort}}, devi prima abilitare {{site.data.keyword.contdelivery_short}} per la tua applicazione e configurare una toolchain che contiene una pipeline e il servizio {{site.data.keyword.DRA_short}}. Fai clic su **Configurazione pipeline** per creare una toolchain per la tua applicazione. Per ulteriori informazioni, vedi [Introduzione a Continuous Delivery](../ContinuousDelivery/index.html "(Si apre in una nuova scheda o finestra)"){:new_window} e [Introduzione a DevOps Insights](../DevOpsInsights/index.html#gettingstarted "(Si apre in una nuova scheda o finestra)").
{: tip}

Se hai configurato {{site.data.keyword.contdelivery_short}} e {{site.data.keyword.DRA_short}} per la tua applicazione, puoi fare clic su **Visualizza Insights** nella colonna Evento per accedere ai dashboard {{site.data.keyword.DRA_short}} e visualizzare ulteriori dettagli sulle tue attività Pipeline.

Le attività {{site.data.keyword.Bluemix_notm}} e Pipeline sono visualizzate anche in **Feed metriche** e sul grafico nel riquadro Tempo di risposta e Disponibilità.
