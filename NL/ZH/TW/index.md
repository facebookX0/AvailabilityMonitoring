---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 開始使用 Availability Monitoring
{: #avmon_gettingstarted}

使用 {{site.data.keyword.prf_hublong}}，以從全球各位置不間斷地執行模擬效能測試。在效能問題影響您的使用者之前主動進行偵測、隔離及診斷。請確定，部署持續更新時，您的應用程式可用且符合回應時間目標。配置應用程式的資料收集器，以收集使用者交易資料。在 {{site.data.keyword.prf_hubshort}} 中使用此資料，以監視應用程式的回應性及傳輸量。
{: shortdesc}

## 關於本作業
{: #avmon_start_about}

{{site.data.keyword.prf_hubshort}} 是當成 {{site.data.keyword.Bluemix_notm}} 型錄之 DevOps 網域中的服務。它預設也可以在**監視**標籤的「應用程式」儀表板中取得。您可以立即開始監視應用程式可用性及效能。當您將 {{site.data.keyword.prf_hubshort}} 連結至應用程式時，依預設會自動建立綜合測試來監視主要應用程式 URL。

## 建立網頁測試
{: #avmon_start_procedure}

完成下列步驟，以開啟應用程式的 {{site.data.keyword.prf_hubshort}}、建立網頁測試來監視另一個 URL，以及設定測試的通知警示。

1.  如果您有要監視的 Cloud Foundry 應用程式，請按一下**應用程式**儀表板上**所有應用程式**表格中的應用程式名稱。如果還沒有應用程式，請建立它，即會自動開啟應用程式卡。按一下「監視」標籤時，Cloud Foundry 應用程式會自動與 {{site.data.keyword.prf_hubshort}} 連結。
2.  若要開啟 {{site.data.keyword.prf_hubshort}}，請按一下**監視**標籤。**監視**標籤所顯示的三個量規會顯示過去 24 個小時的**平均測試可用性**、**現行測試狀態**，以及現行計劃配置的**使用情形**。按一下**新增測試**，以配置監視測試。

    ![Availability Monitoring 標籤](images/avmon_tab.png)

    預設會監視主要應用程式 URL。您監視的任何其他 URL 及服務都可以位於 Bluemix 內部或外部，而且不需要與相關聯 Cloud Foundry 應用程式有關。

3.  按一下「監視設定」頁面上的**單一動作**；然後，按一下「單一動作」頁面上的**網頁**。
4.  在**名稱**欄位中，輸入測試的有意義名稱。將測試用途的說明新增至**說明**欄位。
5.  輸入您要測試的 Web 應用程式的 **URL**。
6.  在「回應驗證」區段中，配置測試的警告及重要警示臨界值。編輯每個橫列的**值**及**單位**。超過警告及重要臨界值觸發警示的回應時間。

    ![「回應驗證」區段，其中包含預設警告及重要臨界值。](images/avmon_webpage_resp_val.png)

7.  使用**黑名單**及**白名單**，來指定要將要求傳送至哪些 URL 及網域，以及與應用程式測試的度量值和狀態相關的 URL 及網域。將您要併入或封鎖的 URL 及網域新增至**白名單**及**黑名單**中。如需封鎖及過濾的相關資訊，請參閱[使用白名單及黑名單封鎖及過濾](avmon_whitelist_blacklist.html "使用白名單及黑名單來決定要將要求傳送至哪些資源，以及與應用程式測試的度量值和狀態相關的資源。白名單及黑名單僅適用於網頁及 Script 化行為測試。")。
8.  按一下**驗證**以建立網頁測試，並判定測試要求是否有效。

    {{site.data.keyword.prf_hubshort}} 會傳送 GET 要求至您的測試 URL 以判斷測試有效性。在測試驗證期間不會發生回應驗證。

    經過驗證的測試即會顯示在「已驗證的項目」表格中。重複步驟 3 - 8，即可新增更多 URL。

9.  若要配置測試設定，請按**下一步**。

    即會顯示測試配置的摘要。例如，會針對預設值顯示下列訊息：

    `Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds the specified threshold.`

    根據現行測試配置，顯示每個月的預估用量及預估測試數。

10. 在「設定」窗格中，按一下**編輯**，以顯示測試的現行設定。您可以更新下列設定：
    - **間隔**定義測試執行頻率。
    - **測試頻率**判斷測試是同步從所有位置執行，還是在每一個間隔從不同位置執行。選取**同時**以同時從所有位置執行測試，或是選取**交錯**以在每個間隔從不同選取位置執行測試。
    - **位置**判斷測試執行的位置。

    按一下**儲存**，以完成配置您的測試。

11. 按一下**完成**。{{site.data.keyword.prf_hubshort}} 儀表板會顯示測試總計的摘要、用於描述警示頻率及位置的地圖及表格、所有與應用程式相關聯的綜合測試、活動的表格，以及用於描述應用程式和其他網站的回應時間及可用性的折線圖。您可以視需要建立更多測試。
12. 您可以使用 {{site.data.keyword.alertnotificationfull}} 服務來配置監視特性，以在發生事件時傳送通知。如需相關資訊，請參閱[啟用通知](avmon_notifications.html "配置監視特性，以在發生事件時傳送通知。")。

## 結果
{: #avmon_getstarted_results}

經過測試中所指定的間隔之後，就會顯示測試結果。預設間隔是 15 分鐘。

您現在已經準備好監視 Web 應用程式的可用性。在**回應時間及可用性**窗格中，會以折線圖顯示應用程式、網站或 REST API 的回應時間及可用性資訊，以及最近活動及測試的相關資訊。

有兩份手冊可以幫助您瞭解 {{site.data.keyword.prf_hubshort}} 的特性。

 - **Video tutorial library** - Video tutorial library 包含如何建立 Bluemix 應用程式、建立 Availability Monitoring 測試、使用 Selenium IDE 建立測試 Script，以及傳送警示至 Slack 的視訊。
 - **Welcome to Monitoring!** - Welcome to Monitoring 手冊強調顯示儀表板的區域，並解釋 {{site.data.keyword.prf_hubshort}} 的每一項特性。

若要開啟手冊，請按一下**說明**圖示 ![「說明」圖示](images/help_icn_white_sml.jpg)；然後，按一下您要檢視的手冊。
