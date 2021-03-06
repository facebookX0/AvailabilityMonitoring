---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# GitHub リポジトリーのスクリプトからのスクリプト・テストの作成
{: #avmon_git_script_test}

GitHub リポジトリーに格納されている Selenium スクリプトからスクリプト・テストを作成します。スクリプト・テストに、GitHub リポジトリーにある Selenium スクリプトに加えた変更を常に同期させることができます。
{: shortdesc}

## 始めに
{: #avmon_git_prereq}

スクリプト・テストを実行するには、Selenium スクリプトが必要です。スクリプト・テストを作成するには、まず、Selenium スクリプトを作成する必要があります。Selenium スクリプトの作成について詳しくは、[Recording synthetic scripts ](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(新規のタブまたはウィンドウで開く)"){: new_window}を参照してください。

GitHub リポジトリーに格納されている Selenium スクリプトからスクリプト・テストを作成するには、以下の手順を実行する必要があります。

-   アプリケーションで{{site.data.keyword.contdelivery_full}}を有効にします。詳しくは、[継続的デリバリー](../ContinuousDelivery/index.html "(新規のタブまたはウィンドウで開く)"){: new_window} を参照してください。
-   ツールチェーンの一部として {{site.data.keyword.Bluemix_notm}} に GitHub へのアクセス権限を与えます。詳しくは、[GitHub の構成](../ContinuousDelivery/toolchains_integrations.html#github "(新規のタブまたはウィンドウで開く)"){: new_window}を参照してください。

## このタスクについて
{: #avmon_git_about}

アプリケーションで{{site.data.keyword.contdelivery_short}}を有効にすると、GitHub リポジトリー内の Selenium スクリプトと同期するスクリプト・テストを作成できます。アプリケーションのユーザーを模倣する Selenium スクリプトを作成した場合、スクリプト・テストを定期的に実行して、シミュレートしたユーザー・アクションに応じたアプリケーションのパフォーマンスをテストすることができます。

## GitHub スクリプトを使用するテストの作成
{: #avmon_git_create_test}

スクリプト・テストを作成するには、以下の手順を実行します。

1.  「モニタリング」タブを表示している場合は、**「新規テストの追加」**をクリックします。

    ![Cloud Foundry アプリケーションの「モニタリング」タブ。](images/avmon_tab.png)

    {{site.data.keyword.prf_hubshort}} ダッシュボードを表示している場合は、「シンセティック・テスト」ペインで**「新規テストの追加」**をクリックします。

    ![「シンセティック・テスト」ペインの「新規テストの追加」ボタン。](images/syn_tests_pane.jpg)

2.  「モニタリングのセットアップ」ページで**「スクリプトによる振る舞い」**をクリックします。「スクリプトによる振る舞いのセットアップ」ページが表示されます。**「Git
Repo」**をクリックします。
3.  **「名前」**フィールドに、わかりやすいテスト名を入力します。**「説明」**フィールドに、テストの目的についての説明を追加します。
4.  使用可能な GitHub リポジトリーを選択し、選択したリポジトリー内のスクリプトのファイル・パスを入力します。
5.  **Git リポジトリー**の Selenium スクリプトの最新バージョンがテストで継続して使用されるようにするには、**「スクリプトのデリバリー・パイプラインとの自動同期」**を選択します。
6.  **「ブラックリスト」**と**「ホワイトリスト」**を使用して、要求の送信先の URL とドメイン、およびアプリケーション・テストのメトリックと状況に寄与する URL とドメインを指定します。含める URL とドメイン、またはブロックする URL とドメインを**ホワイトリスト**と**ブラックリスト**に追加します。ブロッキングとフィルタリングについて詳しくは、[ホワイトリストとブラックリストを使用したブロッキングとフィルタリング](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "ホワイトリストとブラックリストを使用して、要求の送信先のリソース、およびアプリケーション・テストのメトリックと状況に寄与するリソースを決定します。ホワイトリストとブラックリストは、Web ページ・テストおよびスクリプトによる振る舞いテストでのみ使用可能です。")を参照してください。
7.  テスト設定を構成するには、**「次へ」**をクリックします。テスト構成のサマリーが表示されます。例えば、デフォルト設定では次のメッセージが表示されます。

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds 5 seconds``.

    現在のテスト構成に基づいて、月ごとのテストの使用量と数の推定値が表示されます。

8.  「設定」ペインで**「編集」**をクリックして、テストの現在の設定を表示します。以下の設定を更新できます。
    - **「間隔」**は、テストの実行頻度を定義します。
    - **「テスト頻度」**は、テストをすべてのロケーションから同時に実行するか、それぞれの間隔で異なるロケーションから実行するかを決定します。すべての場所から同時にテストを実行する場合は**「同時」**を選択し、選択した場所を間隔ごとに 1 箇所ずつテストする場合は**「時間差」**を選択します。
    - **「重大しきい値」**は、テストの重大アラートの応答時間を定義します。
    - **「警告しきい値」**は、テストの警告アラートの応答時間を定義します。
    - **「ロケーション」**は、テストが実行されるロケーションを決定します。

    必要な場合には、テスト・スクリプトで定義されている変数の値を入力できます。例えば、スクリプトで Web サイトに接続するためにユーザー名とパスワードが必要な場合には、それらの変数の値を入力できます。**「スクリプト変数」**表のさまざまなロケーションに、変数のさまざまな値を設定できます。

    **「保存」**をクリックして、テストの構成を終了します。

9.  **「終了」**をクリックします。{{site.data.keyword.prf_hubshort}} ダッシュボードに、すべてのテストのサマリー、アラートの重大度とロケーションを表示するマップと表、アプリケーションに関連付けられているすべてのシンセティック・テスト、アクティビティーの表、およびアプリケーションと他の Web サイトの応答時間と可用性を示す折れ線グラフが表示されます。
