---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}


# 活動
{: #avmon_activities}

在「活動」窗格中檢視活動的資訊。_活動_ 是在使用者定義事件外部發生的動作。
{: shortdesc}

「活動」窗格會顯示應用程式過去 24 小時的所有活動的相關資訊（例如啟動、停止及部署）。

![Availability Monitoring 儀表板上的「活動」窗格。](images/avmon_activity_pane.png)

{{site.data.keyword.Bluemix_notm}} 活動是 {{site.data.keyword.Bluemix_notm}} 中發生的應用程式事件（例如停止、啟動或重新編譯打包應用程式）。管線活動是在 DevOps 管線中發生的事件（例如建置、部署及測試）。表格標頭會顯示 {{site.data.keyword.Bluemix_notm}} 活動及「管線」活動的不同總計。您可以按一下「活動」窗格標頭上的 {{site.data.keyword.Bluemix_notm}} 或「管線」圖示，依活動「來源」進行過濾來顯示 {{site.data.keyword.Bluemix_notm}} 活動或「管線」活動。

若要在 {{site.data.keyword.prf_hubshort}} 儀表板中檢視「管線」活動，您必須先啟用應用程式的 {{site.data.keyword.contdelivery_short}}，並且配置包含管線及 {{site.data.keyword.DRA_short}} 服務的工具鏈。按一下**管線設定**，以建立應用程式的工具鏈。如需相關資訊，請參閱[開始使用 Continuous Delivery](../ContinuousDelivery/index.html "（在新分頁或視窗中開啟）"){:new_window} 及[開始使用 DevOps Insights](../DevOpsInsights/index.html#gettingstarted "（在新分頁或視窗中開啟）")。
{: tip}

如果您已針對應用程式配置 {{site.data.keyword.contdelivery_short}} 及 {{site.data.keyword.DRA_short}}，則可以按一下「事件」直欄中的**檢視 Insights** 來存取 {{site.data.keyword.DRA_short}} 儀表板，以及檢視「管線」活動的進一步詳細資料。

{{site.data.keyword.Bluemix_notm}} 及「管線」活動也會顯示在**度量資訊來源**中，以及「回應時間及可用性」窗格的圖形上。
