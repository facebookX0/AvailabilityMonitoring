---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# 綜合測試
{: #avmon_synth_tests}

在「綜合測試」窗格中，您可以建立、編輯、刪除及檢視用於監視應用程式的效能及可用性的綜合測試。在「綜合測試」窗格中，會以清單或卡片視圖顯示測試。
{: shortdesc}

![「綜合測試」窗格。](images/syn_tests_pane.jpg)

每一個測試卡都會顯示測試的相關資訊：

- **可用性**會顯示過去 24 小時的測試可用性百分比。
- **狀態**會顯示測試的現行狀態。狀態可能為「重要」、「警告」、「正常」、「失敗」、「非作用中」或「不明」。
- **平均回應**會顯示過去 24 小時的測試平均回應時間。

您可以監視三種不同類型的測試：

- **REST API** 測試會報告 REST 呼叫的回應時間。支援所有 HTTP 要求格式（例如 GET、POST、PUT 及 DELETE）。
- **網頁**測試會報告在所輸入的 URL 中載入網站的回應時間。
- **Script 化行為**測試會監視您建立以模擬使用者與網站之互動的 Selenium Script。例如，您可以建立模擬登入應用程式之使用者的 Selenium Script。您可以定期執行此 Script 來測試應用程式的效能，以回應 Script 所自動化的使用者動作。您可以上傳 Script，或從 GitHub 儲存庫新增 Script。如需建立 Selenium Script 的相關資訊，請參閱[記錄綜合 Script](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "（在新分頁或視窗中開啟）"){: new_window}。

若要新增另一個測試，請按一下**新增測試**。

若要停止、啟動、刪除或編輯綜合測試，請按一下**動作**圖示 ![「動作」圖示](images/actions_icn_white_smll.jpg)，然後按一下您要的動作。若要檢視測試的「分解」詳細資料，請按一下測試。

若要檢視每一個綜合測試的特定用量，請按一下**成本**圖示 ![「成本」圖示](images/cost_icn_white_smll.jpg)。如果您已訂閱付費方案，則會以資料點顯示您的用量。
