---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# 明細ダッシュボード
{: avmon_view_breakdown}

**「明細」**ダッシュボードには、テストに関する主要な統計情報が表示されます。また、ダッシュボードには、可用性、応答時間の情報、過去の傾向、テスト・パフォーマンス・データをこの 24 時間についてまとめたものも表示されます。
{: shortdesc}

テストの詳細な明細を表示するには、「シンセティック・テスト」ペインで対象のテストをクリックします。「アラート頻度」ペインの「アラート」表で**「明細」**をクリックして「明細」ダッシュボードを開くこともできます。

「明細」ダッシュボードには以下の 4 つのペインが表示されます。

## テストの要約
{: #avmon_bdown_summary}

![「テストの要約」ペイン。](images/avmon_bdown_summ.png)

 **「テストの要約」**ペインには、過去 24 時間分の以下のテスト情報が表示されます。

-   **「現在の状況 (Current Status)」**には、テスト状況が表示されます。
-   **「テスト・インスタンス (Test Instances)」**には、標準、警告、重大の各テスト・インスタンスの割合の明細が示されます。
-   **「平均応答時間 (Avg. Response Time)」**には、テストの平均応答時間が表示されます。
-   **「過去の傾向 (Historical Trends)」**には、50、95、99 パーセンタイルのテスト・パフォーマンスの過去の傾向が秒単位またはミリ秒単位で表示されます。

## テスト・インスタンス
{: #avmon_bdown_instances}

![「テスト・インスタンス」表での Rest API テスト・インスタンスの明細。](images/avmon_bdown_apitest_instance.png)

**「テスト・インスタンス」**表には、各テスト・インスタンスに関する詳細情報 (状況、応答時間、テストの実行場所、エラー数、テスト実行時のタイム・スタンプなど) が示されます。
テスト・インスタンスを詳しく調べるには、**「展開 (Expand)」**をクリックします。テスト・インスタンスの各ステップの詳細な応答情報がリストされます。
また任意の列をソートし、速度低下や障害が発生した正確なステップを迅速に特定することもできます。エラー、テスト・シーケンス、応答時間を表示すると、簡単に問題を特定できます。

表示される情報は、モニター対象のシンセティック・テストのタイプによって異なります。

### API
API テスト・インスタンスで**「展開」**をクリックすると 以下の詳細情報の概要が表示されます。

-   **「応答」**には、テスト・インスタンスの合計応答時間が表示されます。この時間にはリダイレクトの時間も含まれます。
-   **「リダイレクト」**には、テスト・インスタンスの合計リダイレクト時間が表示されます。
-   **「サイズ」**には、オブジェクトのサイズが表示されます。
-   **「ダウンロード速度」**には、各オブジェクトのダウンロード速度が表示されます。
-   **「エラー」**には、テスト・インスタンスで発生したエラーの数が表示されます。エラーの詳細を表示するには、**「情報」**アイコンをクリックしてください。

API 呼び出しの各ステップの名前、ステップの順序、各ステップの応答時間をまとめた表が表示されます。次のステップ名が表示されます。

-   **「名前の検索」**には、テスト・インスタンスでオブジェクト名の解決にかかった時間が表示されます。
-   **「接続」**には、テスト・インスタンスでステップの開始からリモート・ホストまたはプロキシーへの接続完了までにかかった時間が表示されます。
-   **「アプリケーション接続」**には、テスト・インスタンスでステップの開始からリモート・ホストへの SSL 接続完了までにかかった時間が表示されます。
-   **「転送前」**には、テスト・インスタンスでステップの開始からファイル転送コマンドの開始直前までにかかった時間が表示されます。
-   **「転送開始」**には、テスト・インスタンスでステップの開始から最初のバイトの受信までにかかった時間が表示されます。
-   **「転送」**には、テスト・インスタンスでファイルの転送にかかった時間が表示されます。

### Web ページ
![「テスト・インスタンス」表での Web ページ・テスト・インスタンスの明細。](images/avmon_bdown_webpage_instance.png)

Web ページ・テスト・インスタンスで**「展開」**をクリックすると 以下の詳細情報の概要が表示されます。

-   **「応答」**には、テスト・インスタンスの応答時間が表示されます。
-   **「合計要求数 (外部)」**には、テスト・インスタンスの要求の総数が表示されます。外部要求の数は括弧内に表示されます。
-   **「ページ・サイズ」**には、Web ページのサイズが表示されます。
-   **「エラー」**には、テスト・インスタンスで発生したエラーの数が表示されます。エラーの詳細を表示するには、「情報」アイコンをクリックします。

テストで実行された各要求についての以下の詳細情報の一覧の表も表示されます。

-   **「タイプ」**には、要求のタイプ (HTML、CSS、JavaScript、イメージなど) が表示されます。外部要求と内部要求は、アイコンで区別がつくようになっています。
-   **「ファイル・パス」**には、要求されたオブジェクトの場所が表示されます。
-   **「サイズ」**には、要求されたオブジェクトのサイズが表示されます。
-   **「順序」**には、テストで実行された要求の順序が表示されます。
-   **「時間」**には、各要求にかかった時間が表示されます。
-   **「状況コード」**には、HTTP 要求の状況コードが表示されます。
-   **「状況」**には、要求の結果 (完了、不明、失敗など) が表示されます。

### スクリプト
![「テスト・インスタンス」表でのスクリプト・テスト・インスタンスの明細。](images/avmon_bdown_script_instance.png)

スクリプト・テスト・インスタンスで**「展開」**をクリックすると 応答時間、スクリプト・ステップの数、エラーの数が表示されます。エラーの詳細を表示するには、**「情報」**アイコンをクリックしてください。

各スクリプト・ステップの以下の情報が、表で表示されます。

-   **「名前」**には、テスト・インスタンスによって呼び出される各 Selenium コマンド (Open、ClickAt、または VerifyBodyText など) が表示されます。
-   **「順序」**には、テスト・インスタンスの最初から最後までのスクリプト・ステップの順序が表示されます。
-   **「時間」**には、各スクリプト・ステップにかかった時間が表示されます。
-   **「エラー」**には、各スクリプト・ステップで発生したエラーの数が表示されます。
-   **「状況」**には、スクリプト・ステップの結果 (完了、不明、失敗など) が表示されます。

各スクリプト・ステップで生成された要求の詳細情報をドリルダウンして表示できます。


![「テスト・インスタンス」表でのスクリプト・テスト・インスタンスの個別ステップ詳細の明細。](images/avmon_bdown_script_subtrans.png)

**「展開」**をクリックすると、以下の詳細情報の表が表示されます。

-   **「タイプ」**には、要求のタイプ (HTML、CSS、JavaScript、イメージなど) が表示されます。外部要求と内部要求は、アイコンで区別がつくようになっています。
-   **「ファイル・パス」**には、要求されたオブジェクトの場所が表示されます。
-   **「サイズ」**には、要求されたオブジェクトのサイズが表示されます。
-   **「順序」**には、テストで実行された要求の順序が表示されます。
-   **「時間」**には、各要求にかかった時間が表示されます。
-   **「状況コード」**には、HTTP 要求の状況コードが表示されます。
-   **「状況」**には、要求の結果 (完了、不明、失敗など) が表示されます。

Web ページがロードに失敗した場合やスクリプトでステップが失敗した場合に、{{site.data.keyword.prf_hubshort}} で自
動的に画面キャプチャーを作成することができます。例えば、スクリプト内のいずれかのステップが Web ページを開くものの、ロードされない場合、{{site.data.keyword.prf_hubshort}} は自動的に画面キャプチャーを作成します。
Web ページまたはスクリプトの画面キャプチャーを表示するには、**「スクリーン・ショット・エラー」**アイコン ![「スクリーン・ショット・エラー」アイコン](images/scrnsht_err_icn_white.jpg) をクリックします。このフィーチャーを使用できるのは、Web ページとスクリプトによるテスト・モニタリングの場合のみです。REST API のモニタリングでは機能しません。

また、**「ダウンロード」**アイコン ![「ダウンロード」アイコン。](images/download_icn_white_smll.jpg) をクリックすることにより、特定のテスト・インスタンスのネットワーク・トラフィックの記録を .har ファイルとしてダウンロードできます。このフィーチャーは、Web ページとスクリプトによる動作のテストのモニタリングで使用できます。

## 応答時間と可用性
{: #avmon_bdown_rt_avail}
「応答時間と可用性」ペインには、定義された期間でのテスト・インスタンスの応答時間と可用性の測定値のグラフが表示されます。詳細情報については、[応答時間と可用性](avmon_resptime_avail.html "「応答時間と可用性」ペインを使用して、一定時間にわたる応答時間、可用性の傾向、アラート、およびアクティビティーの視覚化に役立ててください。メトリック、アラート、およびアクティビティーを相関すると、影響を受けた応答時間を見た時に、特定のアプリケーション変更またはコード・デプロイメントを容易に特定することができます。 ")を参照してください。

## アクティビティー
{: #avmon_bdown_activity}
「アクティビティー」ペインには、過去 24 時間の全アクティビティーの表が表示されます。詳しくは、[アクティビティー](avmon_activities.html "アクティビティーの情報は「アクティビティー」ペインに表示できます。アクティビティーは、ユーザー定義イベントの外部で発生するアクションです。")を参照してください。
