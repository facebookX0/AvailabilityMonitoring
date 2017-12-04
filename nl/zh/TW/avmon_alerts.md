---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 警示頻率
{: #avmon_alert_freq}

「警示頻率」畫面包含一個顯示最新警示的地圖。這些警示是依位置進行分組，並列在「警示」表格中。
{: shortdesc}

## 警示頻率地圖
{: #avmon_alertmap}

「警示頻率」地圖會顯示測試的所有存在點 (PoP) 的一覽資訊。

請使用縮放功能來放大地圖的任何區域，或將它還原至原始大小。將滑鼠移至每一個位置上即可檢視該位置的名稱，以及該位置的警告及重要警示數目。您可以從**警示**下拉清單選取**全部**、**已開啟**或**已關閉**，過濾地圖上顯示的警示。

![「警示頻率」地圖，其顯示四個存在點的測試。](images/alert_freq_map2.png)

### 主機位置
**主機位置**圖示 ![主機位置圖示。](images/icn_host_crit_whtbackground30.jpg) 代表執行所監視應用程式的伺服器位置。**主機位置**圖示的顏色代表該位置最新警示的嚴重性：正常 ![綠色邊框的主機位置圖示，指出該位置沒有任何警示。](images/icn_host_normal_whtbckgrnd_30x38.jpg)、警告 ![黃色邊框的主機位置圖示，指出該位置有一個警示。](images/icn_host_warning_whtbackground30.jpg)，或重要 ![紅色邊框的主機位置圖示，指出該位置有一個警示。](images/icn_host_crit_whtbackground30.jpg)。動畫**主機位置**圖示指出此位置有最多警示，且嚴重性在所有測試實例位置中最高。

### PoP 位置
**PoP 位置**圖示 ![PoP 位置圖示。](images/icn_pop_normal_whtbckgrnd30x30.jpg) 指出測試的 PoP 位置。每一個 **PoP 位置**圖示的顏色代表每一個位置最新警示的嚴重性：正常 ![綠色邊框的 PoP 位置圖示，指出該位置沒有任何警示。](images/icn_pop_normal_whtbckgrnd30x30.jpg)、警告 ![黃色邊框的 PoP 位置圖示，指出該位置有一個警示。](images/icn_pop_warning_whtbckgrnd30x30.jpg)，或重要 ![紅色邊框的 PoP 位置圖示，指出該位置有一個警示。](images/icn_pop_crit_whtbckgrnd30x30.jpg)。動畫 **PoP 位置**圖示指出此位置有最多警示，且嚴重性在所有測試實例位置中最高。

藉由將游標移至**非作用中 PoP 位置**圖示 ![非作用中 PoP 位置](images/icn_avbl_pop.jpg) 上方，然後按一下**在這裡測試**，以將 PoP 位置新增至選取的測試。即會針對選取的測試顯示「測試編輯模式」頁面。您可以從**回應時間**及**可用性**窗格的**測試**下拉功能表中選取測試。

<!--
Private PoP locations are represented by **Private PoP location** icons ![Private PoP location icon that indicates 2 alerts with one or more critical alerts at that location.](images/avmon_private_pop.png).
-->
### 警示數目
**主機位置**圖示及 **PoP 位置**圖示會顯示每一個位置產生的已開啟、已關閉或所有警示數目。「重要」、「警告」及「正常」圖示 ![「重要」、「警告」及「正常」圖示。](images/fltr_alrts_tbl.jpg) 會顯示各位置每一個嚴重性的警示數目。

### 失敗的測試
發生失敗測試實例的位置會以**主機位置**圖示或有不連續邊框的 **PoP 位置**圖示 ![紅色邊框的 PoP 位置圖示，指出該位置有 10 個警示，且有一個以上的失敗測試。](images/avmon_pop_fail_32x33.png) 表示。

## 警示表格
{: #avmon_alertstable}

所有位置的警示顯示在一個表格中。

![警示表格，其顯示所有 PoP 位置的警示。](images/alert_table.jpg)

此表格會顯示警示的下列相關資訊：

-   **嚴重性**說明警示為重要或警告。
-   **時間戳記**顯示警示的建立時間。
-   **說明**彙總測試實例的效能。
-   **觸發者**顯示觸發警示的測試名稱。
-   **位置**陳述發生問題的位置。
-   **狀態**顯示警示是已開啟還是已關閉。

### 檢視警示詳細資料
表格中的每個警示都包含**分解**儀表板的鏈結。使用「分解」儀表板，可協助您疑難排解問題。

### 過濾警示
若要過濾特定位置的警示，請按一下地圖上的**主機位置**圖示或 **PoP 位置**圖示。若要顯示所有位置的警示，請按一下地圖上不是**主機位置**圖示或 **PoP 位置**圖示的任意處。

若要依嚴重性過濾表格中的警示，請按一下**重要**、**警告**或**正常**圖示 ![「重要」、「警告」及「正常」圖示。](images/fltr_alrts_tbl.jpg)。若要移除過濾器並在表格中包含每個嚴重性的警示，請再按一下選取的圖示。


### 變更警示臨界值
警示是透過您在建立測試時所指定的臨界值所觸發。在大部分情況下，它們是因可用性失敗或緩慢回應時間所產生。若要變更臨界值設定，請針對「綜合測試」窗格中產生警示的測試按一下**動作**圖示 ![「動作」圖示。](images/actions_icn_white_smll.jpg)，然後按一下**編輯**。
