---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# サービスの使用量
{: #avmon_usage}

{{site.data.keyword.prf_hubshort}} の使用量の詳細は、アプリの**「モニタリング」**タブと {{site.data.keyword.prf_hubshort}} のメイン・ダッシュボードに表示できます。

**「すべてのアプリケーション」**表から {{site.data.keyword.prf_hubshort}} の使用量の概要を表示するには、アプリ名をクリックしてから、アプリ・ペインの**「モニタリング」**タブをクリックします。ゲージ・グラフに、パーセンテージ形式の**「
使用量」**と、使用しているプランが表示されます。

{{site.data.keyword.prf_hubshort}} のメイン・ダッシュボードから使用量の概要を表示するには、**「構成」**アイコン ![「構成」アイコン](images/config_icn_white_smll.jpg) をクリックします。{{site.data.keyword.prf_hubshort}} Lite プランのユーザーの場合は、使用量は棒グラフにパーセンテージで表示され、使用中のテストの数がともに表示されます。Paid プランのユーザーの場合は、使用量がデータ・ポイントとして表示されます。それぞれの個別テストの使用量詳細は、「シンセティック・テスト」ペインに表示できます。

使用量がデータ・ポイントとして測定されます。データ・ポイントの推定数は以下の数式で計算されます。

データ・ポイントの推定数 = 1 カ月当たりの T \* L \* (60/M \* 24 \* 30)

T は実行したシンセティック・テストの数、L は場所の数、M はテストの間隔 (分単位) です。

単純なテスト (Web ページや REST API のテスト) では、テストごとに 1 個のデータ・ポイントを使用します。高度なテスト (Selenium スクリプトや REST API スクリプトのテスト) では、テストごとに 100 個のデータ・ポイントを使用します。

実際の使用量は、「{{site.data.keyword.Bluemix_notm}} アカウント」ページの「使用状況ダッシュボード」に表示できます。**「アカウント」**をクリックし、次に**「使用状況ダッシュボード」**を選択し、**「サービス料金」**セクションまでスクロールダウンします。{{site.data.keyword.prf_hubshort}} サービスの**矢印**アイコンをクリックすると、使用したデータ・ポイントの数が表示されます。{{site.data.keyword.prf_hubshort}} の価格設定と使用量のプランについては、[Availability Monitoring](https://console.{DomainName}/catalog/services/availability-monitoring/ "(新規のタブまたはウィンドウで開く)"){: new_window} カタログ・ページの価格プランを参照してください。
