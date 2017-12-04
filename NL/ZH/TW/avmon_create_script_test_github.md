---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 從 GitHub 儲存庫中的 Script 建立 Script 測試
{: #avmon_git_script_test}

建立 GitHub 儲存庫中所儲存的 Selenium Script 的 Script 測試。您可以啟用 Script 測試，以持續與您對 GitHub 儲存庫中 Selenium Script 進行的任何變更同步。
{: shortdesc}

## 開始之前
{: #avmon_git_prereq}

Script 測試需要 Selenium Script 運作。若要建立 Script 測試，您必須先建立 Selenium Script。如需建立 Selenium Script 的相關資訊，請參閱[記錄綜合 Script](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "（在新分頁或視窗中開啟）"){: new_window}。

若要從 GitHub 儲存庫中所儲存的 Selenium Script 建立 Script 測試，您必須完成下列步驟：

-   啟用應用程式的 {{site.data.keyword.contdelivery_full}}。如需相關資訊，請參閱 [Continuous Delivery](../ContinuousDelivery/index.html "（在新分頁或視窗中開啟）"){: new_window}。
-   授權 {{site.data.keyword.Bluemix_notm}}，以存取 GitHub 作為工具鏈的一部分。如需相關資訊，請參閱[配置 GitHub](../ContinuousDelivery/toolchains_integrations.html#github "（在新分頁或視窗中開啟）"){: new_window}。

## 關於本作業
{: #avmon_git_about}

如果您啟用應用程式的 {{site.data.keyword.contdelivery_short}}，則可以建立 Script 測試，以與 GitHub 儲存庫中的 Selenium Script 同步。如果您建立可模擬應用程式使用者的 Selenium Script，則可以定期執行 Script 測試來測試應用程式的效能，以回應模擬使用者動作。

## 建立使用 GitHub Script 的測試
{: #avmon_git_create_test}

若要建立 Script 測試，請完成下列步驟。

1.  如果您要檢視「監視標籤」，請按一下**新增測試**。

    ![Cloud Foundry 應用程式的「監視」標籤。](images/avmon_tab.png)

    如果您要檢視 {{site.data.keyword.prf_hubshort}} 儀表板，請按一下「綜合測試」窗格上的**新增測試**。

    ![「綜合測試」窗格上的「新增測試」按鈕。](images/syn_tests_pane.jpg)

2.  按一下「監視設定」頁面上的 **Script 化行為**。即會顯示「Script 化行為設定」頁面。按一下 **Git 儲存庫**。
3.  在**名稱**欄位中，輸入測試的有意義名稱。將測試用途的說明新增至**說明**欄位。
4.  選取可用的 GitHub 儲存庫，然後輸入所選擇儲存庫中 Script 的檔案路徑。
5.  若要確定測試持續使用 **Git 儲存庫**中的最新版 Selenium Script，請選取**使用 Delivery Pipeline 自動同步 Script**。
6.  使用**黑名單**及**白名單**，來指定要將要求傳送至哪些 URL 及網域，以及與應用程式測試的度量值和狀態相關的 URL 及網域。將您要併入或封鎖的 URL 及網域新增至**白名單**及**黑名單**中。如需封鎖及過濾的相關資訊，請參閱[使用白名單及黑名單封鎖及過濾](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "使用白名單及黑名單來決定要將要求傳送至哪些資源，以及與應用程式測試的度量值和狀態相關的資源。白名單及黑名單僅適用於網頁及 Script 化行為測試。")。
7.  若要配置測試設定，請按**下一步**。即會顯示測試配置的摘要。例如，會針對預設值顯示下列訊息：

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds 5 seconds``.

    根據現行測試配置，顯示每個月的預估用量及預估測試數目。

8.  在「設定」窗格中，按一下**編輯**，以顯示測試的現行設定。您可以更新下列設定：
    - **間隔**定義測試執行頻率。
    - **測試頻率**判斷測試是同步從所有位置執行，還是在每一個間隔從不同位置執行。選取**同時**以同時從所有位置執行測試，或是選取**交錯**以在每個間隔從不同選取位置執行測試。
    - **重要臨界值**定義測試的重要警示的回應時間。
    - **警告臨界值**定義測試的警告警示的回應時間。
    - **位置**判斷測試執行的位置。

    必要的話，您可以輸入測試 Script 中所定義變數的值。例如，如果您的 Script 需要使用者名稱及密碼才能連接至網站，則可以輸入這些變數的值。您可以設定 **Script 變數**表格內不同位置中變數的不同值。

    按一下**儲存**，以完成配置您的測試。

9.  按一下**完成**。{{site.data.keyword.prf_hubshort}} 儀表板會顯示所有測試的摘要、顯示警示嚴重性及位置的地圖及表格、所有與應用程式相關聯的綜合測試、活動的表格，以及可描述應用程式和其他網站的回應時間及可用性的折線圖。
