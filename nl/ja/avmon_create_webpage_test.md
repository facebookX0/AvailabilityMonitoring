---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Web ページ・テストの作成
{: #avmon_webpage_test}

Web アプリケーションの可用性をテストし、そのページを開くために要する時間をモニターするための Web ページ・テストを作成します。
{: shortdesc}

## このタスクについて
{: #avmon_webpage_about}

Web ページ・テストは、Web アプリケーションの URL をロードするための応答時間を報告します。Web アプリケーションの可用性と応答時間をモニターするための Web ページ・テストを作成します。

## Web ページ・テストの作成および構成
{: #avmon_create_web_test}

Web ページ・テストを作成するには、以下の手順を実行します。

1.  「モニタリング」タブを表示している場合は、**「新規テストの追加」**をクリックします。

    ![Cloud Foundry アプリケーションの「モニタリング」タブ。](images/avmon_tab.png)

    {{site.data.keyword.prf_hubshort}} ダッシュボードを表示している場合は、「シンセティック・テスト」ペインで**「新規テストの追加」**をクリックします。

    ![「シンセティック・テスト」ペインの「新規テストの追加」ボタン。](images/syn_tests_pane.jpg)

2.  「モニタリングのセットアップ」ページで**「単一アクション」**をクリックし、次に「単一アクション」ページで**「Web ページ」**をクリックします。
3.  **「名前」**フィールドに、わかりやすいテスト名を入力します。**「説明」**フィールドに、テストの目的についての説明を追加します。
4.  テストする Web アプリケーションの**「URL」**を入力します。
5.  「応答の検証」セクションで、テストの警告アラートしきい値と重大アラートしきい値を構成します。行ごとに**「値」**と**「単位」**を編集します。応答時間が警告しきい値と重大しきい値を超えると、アラートがトリガーされます。

    ![デフォルトの警告しきい値と重大しきい値が示されている「応答の検証」セクション。](images/avmon_webpage_resp_val.png)

6.  **「ブラックリスト」**と**「ホワイトリスト」**を使用して、要求の送信先の URL とドメイン、およびアプリケーション・テストのメトリックと状況に寄与する URL とドメインを指定します。含める URL とドメイン、またはブロックする URL とドメインを**ホワイトリスト**と**ブラックリスト**に追加します。ブロッキングとフィルタリングについて詳しくは、[ホワイトリストとブラックリストを使用したブロッキングとフィルタリング](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "ホワイトリストとブラックリストを使用して、要求の送信先のリソース、およびアプリケーション・テストのメトリックと状況に寄与するリソースを決定します。ホワイトリストとブラックリストは、Web ページ・テストおよびスクリプトによる振る舞いテストでのみ使用可能です。")を参照してください。
7.  「**検証**」をクリックして、Web ページ・テストを作成し、テスト要求が有効かどうかを調べます。

    {{site.data.keyword.prf_hubshort}} は、GET 要求をテスト URL に送信してテストの有効性を判断します。テスト検証時には、応答の検証は行われません。

    検証されたテストは、「検証済みのアイテム」表に表示されます。ステップ 3 から 7 を繰り返して、さらに URL を追加できます。

8.  テスト設定を構成するには、**「次へ」**をクリックします。テスト構成のサマリーが表示されます。例えば、デフォルト設定では次のメッセージが表示されます。

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds the specified threshold``.

    現在のテスト構成に基づいて、月ごとのテストの使用量と数の推定値が表示されます。

9.  「設定」ペインで**「編集」**をクリックして、テストの現在の設定を表示します。以下の設定を更新できます。
    - **「間隔」**は、テストの実行頻度を定義します。
    - **「テスト頻度」**は、テストをすべてのロケーションから同時に実行するか、それぞれの間隔で異なるロケーションから実行するかを決定します。すべての場所から同時にテストを実行する場合は**「同時」**を選択し、選択した場所を間隔ごとに 1 箇所ずつテストする場合は**「時間差」**を選択します。
    - **「ロケーション」**は、テストが実行されるロケーションを決定します。

    **「保存」**をクリックして、テストの構成を終了します。

10. **「終了」**をクリックします。{{site.data.keyword.prf_hubshort}} ダッシュボードに、すべてのテストのサマリー、アラートの重大度とロケーションを表示するマップと表、アプリケーションに関連付けられているすべてのシンセティック・テスト、アクティビティーの表、およびアプリケーションと他の Web サイトの応答時間と可用性を示す折れ線グラフが表示されます。