---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 服務用量
{: #avmon_usage}

您可以在應用程式的**監視**標籤，以及在 {{site.data.keyword.prf_hubshort}} 主要儀表板上，檢視 {{site.data.keyword.prf_hubshort}} 用量的詳細資料。

若要從**所有應用程式**表格中查看 {{site.data.keyword.prf_hubshort}} 使用情形的概觀，請按一下應用程式名稱，然後按一下應用程式窗格上的**監視**標籤。即會以量規圖形顯示您的**使用情形**百分比，以及您所使用的方案。

若要從 {{site.data.keyword.prf_hubshort}} 主要儀表板中查看用量概觀，請按一下**配置**圖示 ![「配置」圖示](images/config_icn_white_smll.jpg)。如果您是 {{site.data.keyword.prf_hubshort}} 精簡方案的使用者，會以長條圖及百分比顯示您的用量，以及使用中的測試數目。如果您是付費方案的使用者，會以資料點顯示您的用量。您可以在「綜合測試」窗格中檢視每一個個別測試的用量詳細資料。

您的用量以資料點為單位來測量。預估的資料點數目是根據下列公式計算：

預估的資料點數目 = 每個月 T \* L \* (60/M \* 24 \* 30)

其中 T = 已執行的綜合測試數目，L = 位置數目，M = 測試之間的間隔（分鐘）。

若為簡單的測試，例如網頁及 REST API 測試，每個測試使用 1 個資料點。若為進階測試，例如 Selenium Script 及 REST API Script，每個測試使用 100 個資料點。

您可以在 {{site.data.keyword.Bluemix_notm}}「帳戶」頁面的「用量儀表板」上，檢視您的實際用量。按一下**帳戶**；然後選取**用量儀表板**，並向下捲動至**服務費用**區段。按一下
{{site.data.keyword.prf_hubshort}} 服務的**箭頭**圖示，以檢視您已使用多少資料點。如需 {{site.data.keyword.prf_hubshort}} 定價及用量方案的相關資訊，請參閱 [Availability Monitoring](https://console.{DomainName}/catalog/services/availability-monitoring/ "（在新分頁或視窗中開啟）"){: new_window} 型錄頁面上的「定價方案」。
