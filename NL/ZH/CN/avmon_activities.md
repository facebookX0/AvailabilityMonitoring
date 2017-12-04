---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}


# 活动
{: #avmon_activities}

在“活动”窗格中可查看活动的信息。_活动_是用户定义的事件之外发生的操作。
{: shortdesc}

“活动”窗格显示有关过去 24 小时内应用程序的所有活动（如启动、停止和部署）的信息。

![Availability Monitoring 仪表板上的“活动”窗格。](images/avmon_activity_pane.png)

{{site.data.keyword.Bluemix_notm}} 活动是在 {{site.data.keyword.Bluemix_notm}} 中发生的应用程序事件，如应用程序停止、启动或重新编译打包。管道活动是在 DevOps 管道中发生的事件，如构建、部署和测试。表头分别显示 {{site.data.keyword.Bluemix_notm}} 活动和管道活动的总计。可以通过单击“活动”窗格标题上的 {{site.data.keyword.Bluemix_notm}} 或管道图标，按活动源进行过滤，以显示 {{site.data.keyword.Bluemix_notm}} 活动或管道活动。

要在 {{site.data.keyword.prf_hubshort}} 仪表板中查看管道活动，必须先为应用程序启用 {{site.data.keyword.contdelivery_short}}，并配置包含管道和 {{site.data.keyword.DRA_short}} 服务的工具链。单击**管道设置**可为应用程序创建工具链。有关更多信息，请参阅 [Continuous Delivery 入门](../ContinuousDelivery/index.html "（在新选项卡或窗口中打开）"){:new_window}和 [DevOps Insights 入门](../DevOpsInsights/index.html#gettingstarted "（在新选项卡或窗口中打开）")。
{: tip}

如果已为应用程序配置 {{site.data.keyword.contdelivery_short}} 和 {{site.data.keyword.DRA_short}}，那么可以单击“事件”列中的**查看 Insights** 来访问 {{site.data.keyword.DRA_short}} 仪表板，并查看有关管道活动的进一步详细信息。

{{site.data.keyword.Bluemix_notm}} 和管道活动还会显示在**度量订阅源**中以及“响应时间和可用性”窗格中的图形上。
