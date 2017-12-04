---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 存取 Availability Monitoring
{: #avmon_tab}

您可以從**監視**標籤存取 {{site.data.keyword.prf_hubshort}} 儀表板。Cloud Foundry 應用程式的**監視**標籤，會顯示有關測試可用性和狀態的摘要資訊，以及服務訂閱的詳細資料和用量。
{: shortdesc}

若要存取 {{site.data.keyword.prf_hubshort}}，請完成下列步驟：

1.  按一下**應用程式**儀表板中的 Cloud Foundry 應用程式名稱。
2.  按一下**監視**標籤。

**監視**標籤顯示的三個量規會顯示過去 24 個小時的**平均測試可用性**、所有測試的**現行測試狀態**，以及現行方案配置的**服務用量**。

![Availability Monitoring 標籤](images/avmon_tab.png)

您可以藉由選取要併入「可用性計算」中的測試，來配置 {{site.data.keyword.prf_hubshort}} 如何計算**平均測試可用性**。按一下**平均測試可用性**量規上的**箭頭**圖示 ![「箭頭」圖示](images/arrow_dwn_icn_white.jpg)，以檢視測試卡；然後，按一下**可用性計算**。按一下卡予以新增或移除計算。已排除的測試卡會變褪色。當您完成時，按一下**我已完成**。即會重新整理**平均測試可用性**量規。

您可以藉由在**現行測試狀態**量規上按一下**箭頭**圖示 ![「箭頭」圖示](images/arrow_dwn_icn_white.jpg)，來檢視所有測試的狀態。即會顯示測試的測試卡。

若要存取 {{site.data.keyword.prf_hubshort}} 儀表板，請按一下**查看監視詳細資料**。從 {{site.data.keyword.prf_hubshort}} 儀表板中，您可以根據綜合測試來監視應用程式的可用性。您也可以根據資料收集器所提供的使用者交易資料，來監視應用程式的回應性及傳輸量。

如果要在「綜合測試」窗格中檢視及編輯測試，請按一下**檢視所有測試**。若要建立測試，請按一下**新增測試**。

若要下載應用程式的每月、每週及每日可用性和回應時間平均值的 .csv 檔案報告，請按一下**下載**圖示 ![「下載」圖示](images/download_icn_white_smll.jpg)。
