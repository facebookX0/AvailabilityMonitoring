---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# ホワイトリストとブラックリストを使用したブロッキングとフィルタリング
{: #avmon_filters}

ホワイトリストとブラックリストを使用して、アプリケーション・テストのメトリックと状況に寄与する要求の送信先リソースが決定されます。ホワイトリストとブラックリストは、Web ページおよびスクリプトによる振る舞いのテストでのみ使用可能です。
{: shortdesc}

**「ホワイトリスト」**フィールドと**「ブラックリスト」**フィールドは、テストがアクセスできるリソースまたはアクセスできないリソース、およびテストのメトリックと状況に提供されるリソースを定義します。ホワイトリストとブラックリストは、サード・パーティーのメトリックなど、テスト対象の Web アプリケーションの応答時間に寄与する依存関係およびリソースを制御します。ホワイトリストとブラックリストは、Web ページまたはスクリプトによる振る舞いのテストを作成する時に構成できます。

**ホワイトリスト**を使用して、許可されるドメインと URL を定義できます。次に、**ブラックリスト**を使用して、許可されるロケーションの特定の要素をブロックします。

## 構文

ブラックリストとホワイトリスト内の項目を分離するには、コンマ (,) を使用します。各 URL またはドメインの要素をフィルターに掛けるには、ワイルドカード記号 (\*) を使用します。

## ホワイトリスト

要求およびメトリックの計算に含める URL またはドメインを「ホワイトリスト」フィールドに追加します。ホワイトリストには、最大 10 個の項目をリストできます。各項目の長さは、200 文字を超えることはできません。ホワイトリストの項目に一致しないドメインおよび URL はすべてブロックされます。

以下に例を示します。
```
ibm.com, *developerworks*, *.s81c.com/*
```
{: codeblock}

## ブラックリスト

要求およびメトリックの計算からブロックする URL またはドメインを「ブラックリスト」フィールドに追加します。ブラックリストには、最大 20 個の項目をリストできます。各項目の長さは、200 文字を超えることはできません。

以下に例を示します。
```
*.profile.*.cloudfront.net/*.png
```
{: codeblock}

## フィルタリングおよびブロッキングの動作

テストでは、ホワイトリストとブラックリストの両方を使用することができます。どのロケーションが許可され、どのロケーションがブロックされるかを決定する際、ブラックリストは常にホワイトリストに優先されます。以下の表は、ホワイトリストとブラックリストに関連するすべてのシナリオのフィルタリングとブロッキングの動作を示しています。

<table id="avmon_whitelist_blacklist__table_gyg_vvp_fbb">
<caption>表 1. ホワイトリストとブラックリストのフィルタリングとブロッキングの動作</caption>
<thead>
<tr>
<th>ブラックリスト</th>
<th>ホワイトリスト</th>
<th>動作</th>
<th>理由</th>
</tr>
</thead>
<tbody>
<tr>
<td>空</td>
<td>空</td>
<td>アクセスを許可する</td>
<td>フィルター・ルールが入力されていない。</td>
</tr>
<tr>
<td>空</td>
<td>URL がリスト項目に一致しない</td>
<td>アクセスをブロックする</td>
<td>URL がホワイトリストに含まれていない。</td>
</tr>
<tr>
<td>空</td>
<td>URL がリスト項目に一致する</td>
<td>アクセスを許可する</td>
<td>URL がホワイトリストに含まれている。アクセスをブロックするためのブラックリスト項目がない。</td>
</tr>
<tr>
<td>URL がリスト項目に一致しない</td>
<td>空</td>
<td>アクセスを許可する</td>
<td>URL がブラックリストに含まれていない。アクセスをブロックするためのホワイトリスト項目がない。</td>
</tr>
<tr>
<td>URL がリスト項目に一致する</td>
<td>空</td>
<td>アクセスをブロックする</td>
<td>URL がブラックリストに含まれている。</td>
</tr>
<tr>
<td>URL がリスト項目に一致しない</td>
<td>URL がリスト項目に一致しない</td>
<td>アクセスをブロックする</td>
<td>URL がホワイトリストに含まれていない。</td>
</tr>
<tr>
<td>URL がリスト項目に一致しない</td>
<td>URL がリスト項目に一致する</td>
<td>アクセスを許可する</td>
<td>URL がホワイトリストに含まれている。URL がブラックリストに含まれていない。</td>
</tr>
<tr>
<td>URL がリスト項目に一致する</td>
<td>URL がリスト項目に一致しない</td>
<td>アクセスをブロックする</td>
<td>URL がホワイトリストに含まれていない。URL がブラックリストに含まれている。</td>
</tr>
<tr>
<td>URL がリスト項目に一致する</td>
<td>URL がリスト項目に一致する</td>
<td>アクセスをブロックする</td>
<td>URL がブラックリストに含まれている。ブラックリスト項目がホワイトリスト項目に優先される。</td>
</tr>
</tbody>
</table>
