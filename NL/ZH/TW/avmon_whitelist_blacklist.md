---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 使用白名單及黑名單封鎖及過濾
{: #avmon_filters}

使用白名單及黑名單，來決定要將要求傳送至哪些資源，以及與應用程式測試的度量值和狀態相關的資源。白名單及黑名單僅適用於網頁及 Script 化的行為測試。
{: shortdesc}

**白名單**及**黑名單**欄位定義您的測試可以或無法存取的資源，以及與測試的度量值和狀態相關的資源。白名單及黑名單可以控制與受測試 Web 應用程式的回應時間相關的相依關係及資源，例如協力廠商度量值。建立網頁或 Script 化行為測試時，您可以配置白名單及黑名單。

您可以使用**白名單**來定義容許的網域及 URL，然後，使用**黑名單**來封鎖容許位置的特定元素。

## 語法

使用逗點 (,) 來區隔黑名單及白名單中的項目。使用萬用字元符號 (\*) 來過濾每一個 URL 或網域的元素。

## 白名單

將您要併入要求及AMP計算中的 URL 或網域，新增至「白名單」欄位。您可以在白名單中列出最多 10 個項目。每一個項目的長度不得超出 200 個字元。所有不符合白名單項目的網域及 URL 都會被封鎖。

例如：
```
ibm.com, *developerworks*, *.s81c.com/*
```
{: codeblock}

## 黑名單

將您要自要求及AMP計算中封鎖的 URL 或網域，新增至「黑名單」欄位。您可以在黑名單中列出最多 20 個項目。每一個項目的長度不得超出 200 個字元。

例如：
```
*.profile.*.cloudfront.net/*.png
```
{: codeblock}

## 過濾及封鎖行為

測試可以同時具有白名單及黑名單。在判定容許或封鎖哪些位置時，黑名單一律會置換白名單。下表顯示涉及白名單及黑名單之所有情境的過濾及封鎖行為。

<table id="avmon_whitelist_blacklist__table_gyg_vvp_fbb">
<caption>表 1. 白名單及黑名單的過濾及封鎖行為</caption>
<thead>
<tr>
<th>黑名單</th>
<th>白名單</th>
<th>行為</th>
<th>原因</th>
</tr>
</thead>
<tbody>
<tr>
<td>空的</td>
<td>空的</td>
<td>容許存取</td>
<td>未輸入任何過濾規則。</td>
</tr>
<tr>
<td>空的</td>
<td>URL 不符合清單項目</td>
<td>封鎖存取</td>
<td>URL 不在白名單中。</td>
</tr>
<tr>
<td>空的</td>
<td>URL 符合清單項目</td>
<td>容許存取</td>
<td>URL 在白名單中。沒有可封鎖存取的黑名單項目。</td>
</tr>
<tr>
<td>URL 不符合清單項目</td>
<td>空的</td>
<td>容許存取</td>
<td>URL 不在黑名單中。沒有可封鎖存取的白名單項目。</td>
</tr>
<tr>
<td>URL 符合清單項目</td>
<td>空的</td>
<td>封鎖存取</td>
<td>URL 在黑名單中。</td>
</tr>
<tr>
<td>URL 不符合清單項目</td>
<td>URL 不符合清單項目</td>
<td>封鎖存取</td>
<td>URL 不在白名單中。</td>
</tr>
<tr>
<td>URL 不符合清單項目</td>
<td>URL 符合清單項目</td>
<td>容許存取</td>
<td>URL 在白名單中。URL 不在黑名單中。</td>
</tr>
<tr>
<td>URL 符合清單項目</td>
<td>URL 不符合清單項目</td>
<td>封鎖存取</td>
<td>URL 不在白名單中。URL 在黑名單中。</td>
</tr>
<tr>
<td>URL 符合清單項目</td>
<td>URL 符合清單項目</td>
<td>封鎖存取</td>
<td>URL 在黑名單中。黑名單項目會置換白名單項目。</td>
</tr>
</tbody>
</table>
