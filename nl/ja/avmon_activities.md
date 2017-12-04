---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}


# アクティビティー
{: #avmon_activities}

「アクティビティー」ペインでアクティビティーの情報を表示します。_アクティビティー_ とは、ユーザー定義のイベントとは別に生じるアクションのことです。
{: shortdesc}

「アクティビティー」ペインには、アプリケーションのすべてのアクティビティー (過去 24 時間の開始、停止、およびデプロイメントなど) に関する情報が表示されます。

![Availability Monitoring ダッシュボード上の「アクティビティー」ペイン。](images/avmon_activity_pane.png)

{{site.data.keyword.Bluemix_notm}} アクティビティーは、アプリケーションの停止、始動、または再ステージなどの、{{site.data.keyword.Bluemix_notm}} で起こるアプリケーション・イベントです。パイプライン・アクティビティーは、DevOps パイプ・ラインで発生したイベント (ビルド、デプロイメント、テストなど) です。表のヘッダーには、{{site.data.keyword.Bluemix_notm}} アクティビティーとパイプライン・アクティビティーの別々の総数が表示されます。「アクティビティー」ペインのヘッダーの{{site.data.keyword.Bluemix_notm}} アイコンまたはパイプライン・アイコンをクリックすることにより、アクティビティーの「ソース」でフィルター操作して {{site.data.keyword.Bluemix_notm}} アクティビティーまたはパイプライン・アクティビティーを表示できます。

{{site.data.keyword.prf_hubshort}} ダッシュボードにパイプライン・アクティビティーを表示するには、まずアプリケーションで{{site.data.keyword.contdelivery_short}}を有効にし、パイプラインと {{site.data.keyword.DRA_short}} サービスを含むツールチェーンを構成する必要があります。**「パイプライン・セットアップ」**をクリックして、アプリケーションのツールチェーンを作成します。詳細情報については、[継続的デリバリー概説](../ContinuousDelivery/index.html "(新規のタブまたはウィンドウで開く)"){:new_window}および [DevOps Insights の概説](../DevOpsInsights/index.html#gettingstarted "(新規のタブまたはウィンドウで開く)")を参照してください。
{: tip}

アプリケーション用に{{site.data.keyword.contdelivery_short}}および {{site.data.keyword.DRA_short}} を構成している場合は、「イベント」列の**「インサイトの表示」**をクリックして {{site.data.keyword.DRA_short}} ダッシュボードにアクセスし、パイプライン・アクティビティーに関する詳細を表示できます。

{{site.data.keyword.Bluemix_notm}} アクティビティーおよびパイプライン・アクティビティーは、「応答時間と可用性」ペインの**「メトリック・フィード」**とグラフにも表示されます。
