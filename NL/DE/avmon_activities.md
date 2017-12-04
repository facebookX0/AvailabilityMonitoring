---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}


# Aktivität
{: #avmon_activities}

Im Bereich 'Aktivität' können Sie Informationen zu Aktivitäten anzeigen. _Aktivitäten_ sind Aktionen, die außerhalb benutzerdefinierter Ereignisse auftreten.
{: shortdesc}

Im Bereich 'Aktivität' werden Informationen zu allen Aktivitäten für Ihre Anwendung (z. B. Starten, Stoppen und Bereitstellen) in den letzten 24 Stunden angezeigt.

![Bereich 'Aktivität' im Availability Monitoring-Dashboard](images/avmon_activity_pane.png)

{{site.data.keyword.Bluemix_notm}}-Aktivitäten sind Anwendungsereignisse, die in {{site.data.keyword.Bluemix_notm}} auftreten, zum Beispiel das Starten oder Stoppen einer Anwendung oder ein erneutes Staging. Pipeline-Aktivitäten sind Ereignisse, die in Ihrer DevOps-Pipeline auftreten, z. B. Builds, Bereitstellungen und Tests. In der Tabellenkopfzeile werden separate Gesamtsummen für {{site.data.keyword.Bluemix_notm}}-Aktivitäten und Pipeline-Aktivitäten angezeigt. Sie können nach der Quelle der Aktivitäten filtern, um {{site.data.keyword.Bluemix_notm}}- oder Pipeline-Aktivitäten anzuzeigen, indem Sie auf das Symbol für {{site.data.keyword.Bluemix_notm}} oder Pipeline in der Kopfzeile des Bereichs 'Aktivität' klicken.

Um Pipeline-Aktivitäten im {{site.data.keyword.prf_hubshort}}-Dashboard anzuzeigen, müssen Sie zunächst {{site.data.keyword.contdelivery_short}} für Ihre Anwendung aktivieren und eine Toolchain konfigurieren, die eine Pipeline und den {{site.data.keyword.DRA_short}}-Service enthält. Klicken Sie auf **Aufbau einer Pipeline**, um eine Toolchain für Ihre Anwendung zu erstellen. Weitere Informationen finden Sie unter [Einführung in Continuous Delivery](../ContinuousDelivery/index.html "(Wird in neuer Registerkarte oder neuem Fenster geöffnet)"){:new_window} und [Einführung in DevOps Insights](../DevOpsInsights/index.html#gettingstarted "(Wird in neuer Registerkarte oder neuem Fenster geöffnet)").
{: tip}

Wenn {{site.data.keyword.contdelivery_short}} und {{site.data.keyword.DRA_short}} für die Anwendung konfiguriert sind, können Sie auf **Insights anzeigen** in der Spalte 'Ereignis' klicken, um auf die {{site.data.keyword.DRA_short}}-Dashboards zuzugreifen und weitere Details zu den Pipeline-Aktivitäten anzuzeigen.

{{site.data.keyword.Bluemix_notm}}- und Pipeline-Aktivitäten werden auch im **Metrikfeed** und im Diagramm im Bereich 'Antwortzeit' und im Bereich 'Verfügbarkeit' angezeigt.
