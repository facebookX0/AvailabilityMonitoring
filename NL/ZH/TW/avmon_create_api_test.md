---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# 建立 REST API 測試
{: #avmon_rest_api}

建立 REST API 測試，以使用下列 HTTP 方法來測試 Web 應用程式的回應時間及可用性：GET、POST、PUT 及 DELETE。
{: shortdesc}

使用 REST API 測試來監視 Web 應用程式及其他 URL 的可用性及效能，以回應 REST 呼叫。

若要建立 REST API 測試，請完成下列步驟。

1.  如果您要檢視 Cloud Foundry 應用程式的**監視**標籤，請按一下**新增測試**。

    ![Cloud Foundry 應用程式的「監視」標籤。](images/avmon_tab.png)

    如果您要檢視 {{site.data.keyword.prf_hubshort}} 儀表板，請按一下「綜合測試」窗格上的**新增測試**。

    ![「綜合測試」窗格上的「新增測試」按鈕。](images/syn_tests_pane.jpg)

2.  按一下「監視設定」頁面上的**單一動作**；然後，按一下「單一動作」頁面上的 **REST API**。
3.  在**名稱**欄位中，輸入測試的有意義名稱。將測試用途的說明新增至**說明**欄位。
4.  在「要求」區段中，從**方法**清單中選取方法的類型，並且輸入要使用此方法測試的 **URL**。您可以選擇 **GET**、**PUT**、**POST** 或 **DELETE**。如果您選擇 PUT 或 POST 方法，則可以在**要求內文（選用）**欄位中輸入要測試的內文內容。

    例如，下列 REST API 測試會使用 POST 方法，要求您的 Web 應用程式除了測試該 Web 應用程式的可用性及效能之外，還接受資料。

    ![使用 POST 要求方法的 REST API 測試範例。](images/avmon_restapi_post.png)

5.  您可以配置測試來包括特定標頭及值。在**標頭**欄位中，輸入標頭名稱及標頭值。

    如果您要測試的 Web 應用程式需要使用者登入及密碼，請在**標頭名稱**欄位中輸入 "Authorization"。在**標頭值**欄位中，輸入 "Basic" 這個字、一個空格字元及 username:password 的 base64 編碼值。

    例如，如果使用者名稱是 Aladdin、密碼是 OpenSesame，則請在**標頭值**欄位中輸入 "Basic" 這個字、一個空格字元及 Aladdin:OpenSesame 的 base64 編碼值。

    ![標頭欄位以 base64 格式描述測試授權認證。](images/avmon_apitest_auth.png)

6.  在「回應驗證」區段中，配置測試的警告及重要警示臨界值。編輯每個橫列的**值**及**單位**。超過警告及重要臨界值觸發警示的回應時間。

    ![「回應驗證」區段，其中包含預設警告及重要臨界值。](images/avmon_restapi_resp_val.png)

7.  按一下**新增條件**，以定義及新增自訂回應驗證條件。整體評估自訂回應驗證條件，以產生警示。您最多可以為測試定義及新增六個自訂條件。

    在 {{site.data.keyword.prf_hubshort}} 中，每一個測試最多總共可以產生三個警示。您的測試會報告嚴重性最高的警示，直到導致警示的所有狀況都得到解決。如需相關資訊，請參閱[Availability Monitoring 中的警示產生](avmon_alert_desc.html "在 Availability Monitoring 中，測試最多總共可以產生三個警示。您的測試會報告嚴重性最高的警示，直到導致警示的狀況得到解決。")
    {: tip}

    您可以驗證下列資料：

    - **標頭回應碼**。選取**標頭回應碼**，以測試其中一個 HTTP 回應碼或某範圍的 HTTP 回應碼。
    - **標頭內容**。選取**標頭內容**，以測試特定 HTTP 標頭欄位內容及值。
    - **內文 json**。選取**內文 json**，以測試 JSON 內文中的特定內容。

      對於每一個條件，在**目標**欄位中輸入要測試的內容，並在**值**欄位中輸入要測試的值。從**作業**下拉功能表中選取運算子。最後，為條件選擇**警告**或**重要**的「警示」嚴重性。

    您在**值**欄位中輸入的數值預設會視為數字，而不是字串。輸入回應驗證條件的**值**時，請使用引號 "" 來識別字串與數字。例如，若要測試字串 123，請在「值」欄位中輸入 "123"。若要檢查是否有數字 400，請輸入沒有任何引號的 400。{: tip}

    ![REST API 測試的回應驗證條件](images/avmon_restapi_resp_val2.png)

8.  按一下**驗證**以建立 REST API 測試，並判定測試要求是否有效。

    {{site.data.keyword.prf_hubshort}} 使用選取的 HTTP 方法及您為測試所定義的任何要求標頭來判斷測試有效性。在測試驗證期間不會發生回應驗證。

    經過驗證的測試即會顯示在「已驗證的項目」表格中。重複步驟 3 - 8，即可新增更多 URL。

9.  若要配置測試設定，請按「下一步」。

    即會顯示測試配置的摘要。例如，會針對預設值顯示下列訊息：

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds the specified threshold.``

    根據現行測試配置，顯示每個月的預估用量及預估測試數目。

10. 在「設定」窗格中，按一下**編輯**，以顯示測試的現行設定。

    您可以變更測試的間隔、測試頻率，以及從中傳送測試的位置。

    ![「測試設定」窗格會顯示測試的預設值。](images/avmon_settings.png)

    選取**同時**以同時從所有位置執行測試，或是選取**交錯**以在每個間隔從不同選取位置執行測試。按一下**儲存**，以完成配置您的測試。

11. 按一下**完成**。{{site.data.keyword.prf_hubshort}} 儀表板會顯示所有測試的摘要、顯示警示嚴重性及位置的地圖及表格、所有與應用程式相關聯的綜合測試、活動的表格，以及可描述應用程式和其他網站的回應時間及可用性的折線圖。
