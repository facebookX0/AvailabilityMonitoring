---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# 响应时间和可用性
{: #avmon_resptime_avail}

使用“响应时间和可用性”窗格有助于直观地显示一段时间内的响应时间、可用性趋势、警报和活动。发现受影响的响应时间时，度量、警报和活动的关联有助于轻松确定特定应用程序更改或代码部署。
{: shortdesc}

## 响应时间
{: #avmon_resptime_graph}

在折线图上显示了响应时间信息。要进行查看，请单击**响应时间**选项卡。

![过去 24 小时测试的响应时间图。](images/avmon_rt_gr.jpg)

{{site.data.keyword.prf_hubshort}} 所测量的响应时间比用户所经历的响应时间稍微长一点。
{{site.data.keyword.prf_hubshort}} 模拟真实用户行为，增加响应时间测量的开销。该开销缘于以下因素：

  - {{site.data.keyword.prf_hubshort}} 为每个测试创建新 Firefox 实例，防止之前的回放影响当前测试。
真实最终用户可能因浏览器高速缓存而经历更快速的响应时间。

  - {{site.data.keyword.prf_hubshort}} 在每次测试之前安装 Firefox Web 驱动程序插件。
{: tip}

测试的单个响应时间在折线图上由**响应点**图标 ![“响应点”图标](images/crcl_icn_white.jpg) 表示。不同的颜色表示运行应用程序的不同地理位置。图形的 Y 轴使用警报图标来识别警告和严重阈值范围。黄色**警告**图标 ![黄色警告图标](images/alrt_icn_white_smll.jpg) 表示警告阈值范围，红色**严重**图标 ![红色严重图标](images/wrng_icn_white_smll.jpg) 表示严重阈值范围。单击黄色**警告**图标 ![黄色警告图标](images/alrt_icn_white_smll.jpg) 或红色**严重**图标 ![红色严重图标](images/wrng_icn_white_smll.jpg) 可轻松地识别出现在警告和严重阈值范围中的测试实例。要查看特定测试实例的详细信息，请单击图形上的**响应点**图标 ![“响应点”图标](images/crcl_icn_white.jpg)。

### 过滤器

从**测试**下拉菜单中选择测试。可以过滤 3 个小时、24 个小时、7 天、30 天和 12 个月的数据。
只有对 {{site.data.keyword.prf_hubshort}} 具有付费预订的用户才可以查看超过 12 个月的数据。对大于 24 小时的时间范围进行过滤时，图表上显示的值是平均值。要查看更具体的信息，单击图表向下钻取到单个警报和警告。还可以使用滑块缩短或延长时间范围。

使用“响应时间”图形，您可以在特定存在点位置突出显示和隐藏数据。要突出显示特定位置的响应时间数据，请将鼠标悬停在存在点位置名称上，然后单击**突出显示位置**图标 ![“突出显示位置”图标](images/avmon_location_highlight.jpg)。要隐藏某个位置的响应时间数据，请将鼠标悬停在存在点位置名称，然后单击**隐藏位置**图标 ![“隐藏位置”图标](images/avmon_location_remove.jpg)。要在图形上复原存在点位置数据，请单击**添加更多位置** ![“添加更多位置”图标](images/icn_plus_20x20.jpg) 或**度量选择**选项卡，然后单击之前除去的存在点位置。

### 警报和活动

在“警报”行中，您可以轻松地识别警告和严重警报。将鼠标悬停在**警报图标** ![“严重警报”图标](images/avmon_crit_alert.png)![“警告警报”图标](images/avmon_warn_alert.png) 上可识别该警报的严重性和时间戳记。单击**警报**图标可在**度量订阅源**中显示该警报的详细信息。

您还可以在同一图形上查看活动。_活动_是非用户定义的事件的操作。{{site.data.keyword.Bluemix_notm}} 活动是在 {{site.data.keyword.Bluemix_notm}} 中发生的应用程序事件，如应用程序停止、启动或重新编译打包。管道活动是在 {{site.data.keyword.contdelivery_short}} 工具链中发生的事件，如构建、部署和测试。单击活动以在**度量订阅源**中显示有关该活动的信息。可以在“活动”窗格中查看有关这些活动的信息。

要在 {{site.data.keyword.prf_hubshort}} 仪表板中查看管道活动，必须先为应用程序启用 {{site.data.keyword.contdelivery_short}}，并配置包含管道和 {{site.data.keyword.DRA_short}} 服务的工具链。单击“摘要”窗格或“活动”窗格上的**管道设置**以为应用程序创建工具链。有关更多信息，请参阅 [Continuous Delivery 入门](../ContinuousDelivery/index.html "（在新选项卡或窗口中打开）")和 [DevOps Insights 入门](../DevOpsInsights/index.html#gettingstarted "（在新选项卡或窗口中打开）"){: new_window}。
{: tip}

如果“警报”和“活动”行上有多个活动或警报图标靠在一起，那么**数字**图标会显示该时间的警报数或活动数。将鼠标悬停在**数字**图标上可显示单个警报或活动，然后单击某个警报或活动可在**度量订阅源**中查看相应信息。

### 度量选择和度量订阅源

要按地理区域过滤度量，可单击**度量选择**。单击位置以向图形添加或从图形除去在该位置测量的度量。
单击**添加更多位置**可打开“测试编辑方式”页面，并向所选择的测试添加存在点位置。

![显示存在点位置过滤器的“度量选择”选项卡。](images/avmon_metric_sel.jpg)

要查看度量详细信息列表，请单击**度量订阅源**。度量订阅源将显示执行度量的实例的列表。

![显示警告警报详细信息的“度量订阅源”选项卡。](images/avmon_warn_met_feed.png)

单击图形上的**警报**图标、**活动**图标或**响应点** ![“响应点”图标](images/crcl_icn_white.jpg)，以将该度量的详细信息添加到度量订阅源。

![度量订阅源中的可用测试实例的详细信息。](images/avmon_avail_metfeed.png)

如果针对大于 24 小时的时间范围过滤“响应时间”图，并单击了**响应点**，那么可以在度量订阅源中查看该天的汇总详细信息。

![显示一天测试的所有实例汇总详细信息的度量订阅源。](images/avmon_avail_day_met_feed.png)

单击**缩放**以查看“响应时间”图形中测试所生成的该天的所有响应时间、活动和警报。


要查看警报或测试响应时间的详细信息，请单击度量订阅源中的**细目**。单击**最近的警报**可在度量订阅源中查看该测试实例的最近警报（如果已发生警报）。要查看有关 {{site.data.keyword.DRA_short}} 服务中管道活动的详细信息，请单击度量订阅源中的**查看 Insights**。

## 可用性
{: #avmon_avail_graph}

要查看应用程序的可用性信息，请单击“可用性”。“可用性”图显示所选测试每个存在点 (PoP) 的每日可用性。


![按位置显示过去 7 天每日测试可用性的“可用性”图。](images/avmon_avail_graph.png)

使用“可用性”图形，您可以在特定存在点位置突出显示和隐藏数据。要突出显示特定位置的可用性数据，请将鼠标悬停在**存在点位置名称**上，然后单击**突出显示位置**图标 ![“突出显示位置”图标](images/avmon_location_highlight.jpg)。要隐藏某个位置的可用性数据，请将鼠标悬停在**存在点位置名称**上，然后单击**隐藏位置**图标 ![“隐藏位置”图标](images/avmon_location_remove.jpg)。要在图形上复原存在点位置数据，请单击**度量选择**选项卡，然后单击之前除去的存在点位置。

将鼠标悬停在某个图形点上，以显示特定日和位置测试实例的失败率和数目。
单击图形点可在度量订阅源中显示此信息。

![测试度量订阅源中显示的“达拉斯存在点”的可用性。](images/avmon_avail_metric.png)

单击**缩放**可过滤“可用性”图和“响应时间”图，以显示所选日期的信息。
