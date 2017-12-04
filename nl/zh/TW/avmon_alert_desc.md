---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Availability Monitoring 中的警示產生
{: #avmon_alert_desc}

在 {{site.data.keyword.prf_hubshort}} 中，測試最多總共可以產生三個警示。您的測試會報告嚴重性最高的警示，直到導致警示的狀況得到解決。
{: shortdesc}

三種不同的狀況都會引發不同的警示：

-   Web 應用程式或 URL 的回應時間超出測試設定的警告或重要臨界值設定時。每個測試預設都會測量回應時間，並根據該測試的警告及重要臨界值來引發警示。
-   測試傳回指出 Web 應用程式或 URL 因用戶端或伺服器錯誤而無法使用的 HTTP 回應碼時。每個測試預設都會檢查回應碼，以判定測試成功還是失敗。
-   測試判定滿足一個以上的自訂條件時，會引發具有一個以上自訂條件所定義的最高嚴重性的警示。判定是否引發警示時，{{site.data.keyword.prf_hubshort}} 會整體考量所有自訂條件。除非測試判定所有自訂條件都不會再產生任何警告或重要警示，否則此警示會持續發生。

發生多個警示時，只要有任何警示，{{site.data.keyword.prf_hubshort}} 就會報告嚴重性最高的警示。

例如，如果測試回應時間引發重要警示，且另一個狀況引發警告警示，則測試會產生重要警示，並顯示在 {{site.data.keyword.prf_hubshort}} 儀表板上。如果不再符合造成重要警示的條件，則測試警示的嚴重性會變更為「警告」。除非所有條件都不再造成警示，否則警示會持續發生。
