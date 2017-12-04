---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# 回應時間及可用性
{: #avmon_resptime_avail}

使用「回應時間及可用性」窗格，可協助您視覺化回應時間、可用性趨勢、警示，以及一段時間的活動。AMP、警示及活動的相關性，可協助您在看到受影響的回應時間時輕鬆地隔離特定應用程式變更或程式碼部署。
{: shortdesc}

## 回應時間
{: #avmon_resptime_graph}

回應時間資訊會以折線圖顯示。若要進行檢視，請按一下**回應時間**標籤。

![前 24 小時測試的回應時間圖形。](images/avmon_rt_gr.jpg)

{{site.data.keyword.prf_hubshort}} 所測量的回應時間略大於使用者所經歷的回應時間。{{site.data.keyword.prf_hubshort}} 會模擬實際使用者行為，這樣會增加回應時間測量的額外負擔。額外負擔是由下列因素所造成：

  - {{site.data.keyword.prf_hubshort}} 會為每一個測試建立新的 Firefox 實例，以防止先前的播放影響現行測試。實際一般使用者可能會因為瀏覽器快取而有較快速的回應時間。
  - {{site.data.keyword.prf_hubshort}} 會在每一個測試之前安裝 Firefox Web 驅動程式外掛程式。
{: tip}

在折線圖上，測試的個別回應時間是以**回應點**圖示 ![「回應點」圖示](images/crcl_icn_white.jpg) 表示。不同的顏色表示應用程式執行所在的不同地理位置。此圖形的 Y 軸使用警示圖示來識別警告及重要臨界值範圍。黃色**警告**圖示 ![黃色警告圖示](images/alrt_icn_white_smll.jpg) 代表警告臨界值範圍，紅色**重要**圖示 ![紅色重要圖示](images/wrng_icn_white_smll.jpg) 則代表重要臨界值範圍。按一下黃色**警告**圖示 ![黃色警告圖示](images/alrt_icn_white_smll.jpg) 或紅色**重要**圖示 ![紅色重要圖示](images/wrng_icn_white_smll.jpg)，以輕鬆地識別警告及重要臨界值範圍中出現的測試實例。若要檢視特定測試實例的詳細資料，請按一下圖形上的**回應點**圖示 ![「回應點」圖示](images/crcl_icn_white.jpg)。

### 過濾器

從**測試**下拉功能表中，選擇測試。您可以過濾 3 小時、24 小時、7 天、30 天及 12 個月的資料。只有具有已付費 {{site.data.keyword.prf_hubshort}} 訂閱的使用者才有檢視 12 個月資料的能力。當您針對大於 24 小時的時間範圍進行過濾時，會取得圖形中所顯示值的平均值。若要檢視更特定資訊，請按一下圖形，以往下探查至個別警示及警告。您也可以使用調節器來縮短或延長時間範圍。

使用「回應時間」圖形，您可以強調顯示及隱藏特定 PoP 位置的資料。若要強調顯示特定位置的回應時間資料，請將滑鼠移到 PoP 位置名稱上，然後按一下**強調顯示位置**圖示 ![強調顯示位置圖示](images/avmon_location_highlight.jpg)。若要隱藏位置的回應時間資料，請將滑鼠移到 PoP 位置名稱上，然後按一下**隱藏位置**圖示 ![隱藏位置圖示](images/avmon_location_remove.jpg)。若要將 PoP 位置資料還原至圖形，請按一下**新增其他位置** ![「新增其他位置」圖示](images/icn_plus_20x20.jpg) 或**選取度量值**標籤；然後，按一下您先前移除的 PoP 位置。

### 警示及活動

您可以輕鬆地識別「警示」列中的警告及重要警示。將游標移至**警示圖示** ![重要警示圖示](images/avmon_crit_alert.png)![警告警示圖示](images/avmon_warn_alert.png) 上方，以識別該警示的嚴重性及時間戳記。按一下**警示圖示**，以在**度量資訊來源**中顯示該警示的詳細資料。

您也可以檢視相同圖形上的活動。_活動_ 是非使用者定義事件的動作。{{site.data.keyword.Bluemix_notm}} 活動是 {{site.data.keyword.Bluemix_notm}} 中發生的應用程式事件（例如停止、啟動或重新編譯打包應用程式）。管線活動是在 {{site.data.keyword.contdelivery_short}} 工具鏈中發生的事件（例如建置、部署及測試）。在**度量資訊來源**中，按一下活動以顯示該活動的相關資訊。您可以在「活動」窗格中檢視這些活動的相關資訊。

若要在 {{site.data.keyword.prf_hubshort}} 儀表板中檢視「管線」活動，您必須先啟用應用程式的 {{site.data.keyword.contdelivery_short}}，並且配置包含管線及 {{site.data.keyword.DRA_short}} 服務的工具鏈。按一下「摘要」窗格或「活動」窗格上的**管線設定**，以建立應用程式的工具鏈。如需相關資訊，請參閱[開始使用 Continuous Delivery](../ContinuousDelivery/index.html "（在新分頁或視窗中開啟）") 及[開始使用 DevOps Insights](../DevOpsInsights/index.html#gettingstarted "（在新分頁或視窗中開啟）"){: new_window}。
{: tip}

如果有多個活動或警示圖示在「警示」及「活動」列上緊靠在一起，則**數目圖示**會顯示該時間的警示或活動數目。將游標移至**數目圖示**上方以顯示個別警示或活動，然後按一下警示或活動以檢視**度量資訊來源**中的資訊。

### 選取度量及度量資訊來源

若要依地理區域過濾AMP，請按一下**選取AMP**。按一下位置，以新增或移除在圖形該位置所測量的AMP。按一下**新增其他位置**，以開啟「測試編輯模式」頁面，然後將 PoP 位置新增至選取的測試。

![「選取AMP」標籤，其顯示 PoP 位置過濾。](images/avmon_metric_sel.jpg)

若要檢視度量詳細資料清單，請按一下**度量資訊來源**。「度量資訊來源」會顯示滿足度量的實例清單。

![「度量資訊來源」標籤，其顯示警告警示的詳細資料。](images/avmon_warn_met_feed.png)

按一下圖形上的**警示圖示**、**活動圖示**或**回應點** ![「回應點」圖示](images/crcl_icn_white.jpg)，以將該度量的詳細資料新增至「度量資訊來源」。

![「度量資訊來源」中可用測試實例的詳細資料。](images/avmon_avail_metfeed.png)

如果您針對大於 24 小時的時間範圍來過濾「回應時間」圖形，並按一下**回應點**，則可以在「度量資訊來源」中看到該日的聚集詳細資料。

![「度量資訊來源」顯示某日的所有測試實例的聚集詳細資料。](images/avmon_avail_day_met_feed.png)

按一下**縮放**以在「回應時間」圖形中檢視所有回應時間、活動及當天測試產生的警示。

若要檢視警示或測試回應時間的詳細資訊，請按一下「度量資訊來源」中的**分解**。按一下**最近的警示**，以在「度量資訊來源」中檢視該測試實例的最近警示（如果有發生警示的話）。若要檢視 {{site.data.keyword.DRA_short}} 服務中管線活動的詳細資訊，請按一下「度量資訊來源」中的**檢視 Insights**。

## 可用性
{: #avmon_avail_graph}

若要檢視應用程式的可用性資訊，請按一下「可用性」。「可用性」圖形會顯示所選取測試的每一個存在點 (PoP) 的每日可用性。

![「可用性」圖形，依位置顯示前 7 天的每日測試可用性。](images/avmon_avail_graph.png)

使用「可用性」圖形，您可以強調顯示及隱藏特定 PoP 位置的資料。若要強調顯示特定位置的可用性資料，請將游標移至 **PoP 位置名稱**上方；然後，按一下**強調顯示位置**圖示 ![「強調顯示位置」圖示](images/avmon_location_highlight.jpg)。若要隱藏位置的可用性資料，請將游標移至 **PoP 位置名稱**上方；然後，按一下**隱藏位置**圖示 ![「隱藏位置」圖示](images/avmon_location_remove.jpg)。若要將 PoP 位置資料還原至圖形，請按一下**選取AMP**標籤，然後按一下您先前移除的 PoP 位置。

將滑鼠指標移至圖形點上方，以顯示特定一天及特定位置的失敗率及測試實例數目。按一下圖形點，即可在「度量資訊來源」中顯示此資訊。

![「度量資訊來源」中顯示的達拉斯 PoP 的測試可用性。](images/avmon_avail_metric.png)

按一下**縮放**，以過濾「可用性」圖形及「回應時間」圖形，以顯示所選取日期的資訊。
