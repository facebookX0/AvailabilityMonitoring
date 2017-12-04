---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# 分解儀表板
{: avmon_view_breakdown}

**分解**儀表板顯示您測試的重要統計資訊。此儀表板也會彙總過去 24 個小時的可用性及回應時間資訊、歷程趨勢以及測試效能資料。
{: shortdesc}

若要檢視測試的詳細分解，請按一下「綜合測試」窗格中的測試。您也可以藉由在「警示頻率」窗格中，按一下警示表格中的**分解**，來開啟「分解」儀表板。

「分解」儀表板會顯示四個窗格：

## 測試摘要
{: #avmon_bdown_summary}

![「測試摘要」窗格。](images/avmon_bdown_summ.png)

**測試摘要**窗格會顯示過去 24 小時的下列測試資訊：

-   **現行狀態**會顯示測試狀態。
-   **測試實例**會顯示正常、警告及重要測試實例的百分比分解。
-   **平均回應時間**會顯示測試的平均回應時間。
-   **歷程趨勢**會顯示第 50 個、第 95 個及第 99 個百分位的測試效能歷程趨勢（秒或毫秒）。

## 測試實例
{: #avmon_bdown_instances}

![「測試實例」表格中的 Rest API 測試實例分解。](images/avmon_bdown_apitest_instance.png)

**測試實例**表格會顯示每一個測試實例的詳細資訊（包括狀態、回應時間、測試執行位置、錯誤數目，以及執行測試時的時間戳記）。若要往下探查至測試實例，請按一下**展開**。會列出測試實例中每一個步驟的詳細回應資訊。您可以排序任何直欄，以協助您快速識別速度變慢或失敗的確切步驟。檢視錯誤、測試序列及回應時間，可協助您輕鬆地找出問題。

顯示的資訊取決於所監視的「綜合測試」類型：

### API
當您針對 API 測試實例按一下**展開**時，會顯示下列詳細資料的高階摘要：

-   **回應**會顯示測試實例的回應時間總計（包括重新導向時間）。
-   **重新導向**會顯示測試實例的重新導向時間總計。
-   **大小**會顯示物件的大小。
-   **下載速度**會顯示每個物件下載的速度。
-   **錯誤**會顯示在測試實例期間發生的錯誤數。若要檢視錯誤資料，請按一下**資訊**圖示。

表格會顯示 API 呼叫中的每一個步驟，以及步驟的名稱、一系列步驟，以及每一個步驟的回應時間。會顯示下列步驟名稱：

-   **名稱查閱**代表測試實例解析物件名稱所耗費的時間。
-   **連接**代表測試實例從步驟開始到完成與遠端主機或 Proxy 之連線所耗費的時間。
-   **應用程式連接**代表測試實例從步驟開始到完成與遠端主機之 SSL 連線所耗費的時間。
-   **傳送前**代表測試實例從步驟開始到檔案傳送指令開始前一刻所耗費的時間。
-   **傳送開始**代表測試實例從步驟開始到收到第一個位元組所耗費的時間。
-   **傳送**代表測試實例傳送檔案所耗費的時間。

### 網頁
![「測試實例」表格中的「網頁」測試實例分解。](images/avmon_bdown_webpage_instance.png)

當您針對網頁測試實例按一下**展開**時，會顯示下列詳細資料的高階摘要：

-   **回應**會顯示測試實例的回應時間。
-   **要求總數（外部）**會顯示測試實例的要求總數。外部要求數目位於括弧中。
-   **頁面大小**會顯示網頁的大小。
-   **錯誤**會顯示在測試實例期間發生的錯誤數。若要檢視錯誤詳細資料，請按一下「資訊」圖示。

也會顯示一個表格，針對測試所提出的每個要求列出下列詳細資料：

-   **類型**會顯示要求的類型，例如 HTML、CSS、JavaScript 或影像。外部及內部要求以圖示表示。
-   **檔案路徑**說明所要求物件的位置。
-   **大小**會顯示所要求物件的大小。
-   **順序**會顯示測試所提出的要求順序。
-   **時間**會顯示每一個要求所耗費的時間。
-   **狀態碼**會顯示 HTTP 要求狀態碼。
-   **狀態**說明要求的結果，例如「已完成」、「不明」或「失敗」。

### Script
![「測試實例」表格中的 Script 測試實例分解。](images/avmon_bdown_script_instance.png)

當您針對 Script 測試實例按一下**展開**時，會顯示回應時間、Script 步驟數目和錯誤數。若要檢視錯誤資料，請按一下**資訊**圖示。

每個 Script 步驟的下列詳細資料會顯示在表格中：

-   **名稱**會顯示測試實例所呼叫的每一個 Selenium 指令，例如 Open、ClickAt 或 VerifyBodyText。
-   **順序**會顯示測試實例從頭到尾的 Script 步驟順序。
-   **時間**會顯示每一個 Script 步驟所耗費的時間。
-   **錯誤**會顯示在每個 Script 步驟期間發生的錯誤數。
-   **狀態**說明 Script 步驟的結果，例如「已完成」、「不明」或「失敗」。

您可以往下探查並檢視每個 Script 步驟所產生之要求的詳細資料。

![「測試實例」表格中 Script 測試實例的個別步驟詳細資料分解。](images/avmon_bdown_script_subtrans.png)

按一下**展開**即可檢視包含下列詳細資料的表格：

-   **類型**會顯示要求的類型，例如 HTML、CSS、JavaScript 或影像。外部及內部要求以圖示表示。
-   **檔案路徑**說明所要求物件的位置。
-   **大小**會顯示所要求物件的大小。
-   **順序**會顯示測試所提出的要求順序。
-   **時間**會顯示每一個要求所耗費的時間。
-   **狀態碼**會顯示 HTTP 要求狀態碼。
-   **狀態**說明要求的結果，例如「已完成」、「不明」或「失敗」。

如果無法載入網頁，或 Script 中的步驟失敗，則 {{site.data.keyword.prf_hubshort}} 可以自動建立畫面擷取。例如，如果 Script 中的其中一個步驟開啟網頁，但未載入網頁，則 {{site.data.keyword.prf_hubshort}} 會自動建立畫面擷取。
若要檢視網頁或 Script 的畫面擷取，請按一下**擷取畫面錯誤**圖示 ![「擷取畫面錯誤」 圖示](images/scrnsht_err_icn_white.jpg)。此特性僅適用於網頁及 Script 化測試監視。但不適用於 REST API 監視。

您也可以藉由按一下**下載**圖示 ![「下載」圖示。](images/download_icn_white_smll.jpg)，來將特定測試實例的網路資料流量記錄下載為 .har 檔案。此特性適用於網頁及 Script 化行為測試監視。

## 回應時間及可用性
{: #avmon_bdown_rt_avail}
「回應時間及可用性」窗格會顯示在定義的期間內，測試實例的測量回應時間及可用性的圖形。如需相關資訊，請參閱[回應時間及可用性](avmon_resptime_avail.html "使用「回應時間及可用性」窗格，協助您視覺化一段時間的回應時間、可用性趨勢、警示及活動。在查看受影響的回應時間時，度量值、警示及活動的相關性，有助於輕鬆地隔離特定的應用程式變更或程式碼部署。")。

## 活動
{: #avmon_bdown_activity}
「活動」窗格會顯示一個包含過去 24 小時內所有活動的表格。如需相關資訊，請參閱[活動](avmon_activities.html "您可以在「活動」窗格中檢視活動的資訊。這些活動是指發生在使用者定義的事件之外的動作。")。