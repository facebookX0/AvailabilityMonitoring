---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 使用白名单和黑名单进行阻止和过滤
{: #avmon_filters}

使用白名单和黑名单可确定要向其发送请求的资源，以及哪些资源会影响应用程序测试的度量和状态。白名单和黑名单仅适用于 Web 页面和脚本行为测试。
{: shortdesc}

**白名单**和**黑名单**字段可定义测试可以访问或无法访问的资源，以及影响测试的度量和状态的资源。白名单和黑名单可以控制影响被测试 Web 应用程序的响应时间的依赖项和资源，例如第三方度量。可以在创建 Web 页面或脚本行为测试时，配置白名单和黑名单。

可以使用**白名单**来定义允许的域和 URL；然后，使用**黑名单**来阻止所允许位置的特定元素。

## 语法

使用逗号 (,) 来分隔黑名单和白名单中的各个项。使用通配符 (\*) 来过滤每个 URL 或域的元素。

## 白名单

向“白名单”字段添加要包含在请求和度量计算中的 URL 或域。在白名单中最多可以列出 10 个项。每个项的长度不能超过 200 个字符。与白名单上的项不匹配的所有域和 URL 都会被阻止。

例如：
```
ibm.com, *developerworks*, *.s81c.com/*
```
{: codeblock}

## 黑名单

向“黑名单”字段添加要排除在请求和度量计算之外的 URL 或域。在黑名单中最多可以列出 20 个项。每个项的长度不能超过 200 个字符。

例如：
```
*.profile.*.cloudfront.net/*.png
```
{: codeblock}

## 过滤和阻止行为

测试可以同时具有白名单和黑名单。确定允许或阻止的位置时，黑名单始终优先于白名单。下表显示所有涉及白名单和黑名单的场景的过滤和阻止行为。

<table id="avmon_whitelist_blacklist__table_gyg_vvp_fbb">
<caption>表 1. 白名单和黑名单的过滤和阻止行为</caption>
<thead>
<tr>
<th>黑名单</th>
<th>白名单</th>
<th>行为</th>
<th>原因</th>
</tr>
</thead>
<tbody>
<tr>
<td>空</td>
<td>空</td>
<td>允许访问</td>
<td>未输入过滤规则。</td>
</tr>
<tr>
<td>空</td>
<td>URL 与列表条目不匹配</td>
<td>阻止访问</td>
<td>URL 不在白名单中。</td>
</tr>
<tr>
<td>空</td>
<td>URL 与列表条目相匹配</td>
<td>允许访问</td>
<td>URL 在白名单中。没有要阻止访问的黑名单条目。</td>
</tr>
<tr>
<td>URL 与列表条目不匹配</td>
<td>空</td>
<td>允许访问</td>
<td>URL 不在黑名单中。没有要阻止访问的白名单条目。</td>
</tr>
<tr>
<td>URL 与列表条目相匹配</td>
<td>空</td>
<td>阻止访问</td>
<td>URL 在黑名单中。</td>
</tr>
<tr>
<td>URL 与列表条目不匹配</td>
<td>URL 与列表条目不匹配</td>
<td>阻止访问</td>
<td>URL 不在白名单中。</td>
</tr>
<tr>
<td>URL 与列表条目不匹配</td>
<td>URL 与列表条目相匹配</td>
<td>允许访问</td>
<td>URL 在白名单中。URL 不在黑名单中。</td>
</tr>
<tr>
<td>URL 与列表条目相匹配</td>
<td>URL 与列表条目不匹配</td>
<td>阻止访问</td>
<td>URL 不在白名单中。URL 在黑名单中。</td>
</tr>
<tr>
<td>URL 与列表条目相匹配</td>
<td>URL 与列表条目相匹配</td>
<td>阻止访问</td>
<td>URL 在黑名单中。黑名单条目将优先于白名单条目。</td>
</tr>
</tbody>
</table>
