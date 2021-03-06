---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# REST API テストの作成
{: #avmon_rest_api}

REST API テストを作成し、GET、POST、PUT、および DELETE などの HTTP メソッドを使用して、Web アプリケーションの応答時間と可用性をテストします。
{: shortdesc}

REST API テストを使用して、REST 呼び出しへの応答で、Web アプリケーションとその他の URL の可用性とパフォーマンスをモニターします。

REST API テストを作成するには、以下の手順を実行します。

1.  Cloud Foundry アプリケーションの**「モニタリング」**タブを表示している場合は、**「新規テストの追加」**をクリックします。

    ![Cloud Foundry アプリケーションの「モニタリング」タブ。](images/avmon_tab.png)

    {{site.data.keyword.prf_hubshort}} ダッシュボードを表示している場合は、「シンセティック・テスト」ペインで**「新規テストの追加」**をクリックします。

    ![「シンセティック・テスト」ペインの「新規テストの追加」ボタン。](images/syn_tests_pane.jpg)

2.  「モニタリングのセットアップ」ページで**「単一アクション」**をクリックし、「単一アクション」 ページで**「REST API」**をクリックします。
3.  **「名前」**フィールドに、わかりやすいテスト名を入力します。**「説明」**フィールドに、テストの目的についての説明を追加します。
4.  「要求」セクションで、**「メソッド」**リストからメソッドのタイプを選択し、このメソッドでテストする**「URL」**を入力します。**「GET」**、**「PUT」**、**「POST」**、**「DELETE」**のいずれかを選択できます。PUT メソッドまたは POST メソッドを選択した場合、**「要求本文 (オプション)」**フィールドに、テストする本文コンテンツを入力できます。

    例えば、以下の REST API テストは、POST メソッドを使用して、Web アプリケーションの可用性とパフォーマンスをテストすることに加え、その Web アプリケーションがデータを受け入れることを要求します。

    ![POST 要求メソッドを使用する REST API テストの例。](images/avmon_restapi_post.png)

5.  特定のヘッダーと値が含まれるようにテストを構成できます。**「ヘッダー」**フィールドにヘッダー名とヘッダー値を入力します。

    テストする Web アプリケーションでユーザーのログインとパスワードが必要な場合は、**「ヘッダー名」**フィールドに「Authorization」と入力します。**「ヘッダー値」**フィールドには、「Basic」という語、スペース文字、および username:password の Base64 エンコード値を入力します。

    例えば、ユーザー名が Aladdin でパスワードが OpenSesame の場合は、「Basic」という語、スペース文字、および Aladdin:OpenSesame の Base64 エンコード値を**「ヘッダー値」**フィールドに入力します。

    ![base64 のテスト許可資格情報を示す「ヘッダー」フィールド。](images/avmon_apitest_auth.png)

6.  「応答の検証」セクションで、テストの警告アラートしきい値と重大アラートしきい値を構成します。行ごとに**「値」**と**「単位」**を編集します。応答時間が警告しきい値と重大しきい値を超えると、アラートがトリガーされます。

    ![デフォルトの警告しきい値と重大しきい値が示されている「応答の検証」セクション。](images/avmon_restapi_resp_val.png)

7.  **「条件の追加」**をクリックして、カスタマイズした応答の検証条件を定義して追加します。カスタマイズした応答の検証条件は、集合体として評価されてアラートが生成されます。テストに対してカスタマイズ条件を最大 6 つまで定義して追加できます。

    {{site.data.keyword.prf_hubshort}} では、テストごとに最大で合計 3 つのアラートを生成できます。テストは、アラートの原因であるすべての条件が解決されるまで、最高の重大度のアラートを報告します。詳しくは、[ Availability Monitoring でのアラートの生成](avmon_alert_desc.html "Availability Monitoring では、テストは、最大で合計 3 つのアラートを生成できます。テストは、アラートの原因である条件が解決されるまで、最高の重大度のアラートを報告します。")を参照してください。
    {: tip}

    以下のデータを検証できます。

    - **ヘッダー応答コード**。1 つの HTTP 応答コードまたは HTTP 応答コードの範囲をテストするには、**「ヘッダー応答コード (Header response code)」**を選択します。
    - **ヘッダー・プロパティー**。特定の HTTP ヘッダー・フィールド・プロパティーと値をテストするには、**「ヘッダー・プロパティー (Header property)」**を選択します。
    - **本文 JSON**。JSON 本文の特定のプロパティーをテストするには、**「本文 JSON」**を選択します。

      条件ごとに、テスト対象のプロパティーを**「ターゲット」**フィールドに入力し、テスト対象の値を**「値」**フィールドに入力します。**「演算」**ドロップダウン・メニューから演算子を選択します。最後に、条件に対して**警告**または**重大**のアラート重大度を選択します。

    **「値」**フィールドに入力した数値は、デフォルトでは文字列ではなく数字として扱われます。応答の検証条件の値を**「値」**に入力する際には、引用符 "" を使用して文字列と数字を区別します。例えば、文字列 123 についてテストするには、「値」フィールドに "123" と入力します。数字の 400 を検査するには、引用符を使用せずに 400 と入力します。{: tip}

    ![REST API テストの応答の検証条件](images/avmon_restapi_resp_val2.png)

8.  **「検証」**をクリックして、REST API テストを作成し、テスト要求が有効かどうかを調べます。

    {{site.data.keyword.prf_hubshort}} は、選択した HTTP メソッドと、テスト用に定義した任意の要求ヘッダーを使用してテストの有効性を判別します。テスト検証時には、応答の検証は行われません。

    検証されたテストは、「検証済みのアイテム」表に表示されます。ステップ 3 から 8 までを繰り返して、さらに URL を追加できます。

9.  テスト設定を構成するには、「次へ」をクリックします。

    テスト構成のサマリーが表示されます。例えば、デフォルト設定では次のメッセージが表示されます。

    ``テストを行います。指定されたしきい値を超えるかどうかを、3 つの場所で 15 分ごとに同時に調べます。(Test will occur: Every 15 minutes from 3 locations simultaneously to determine if
test exceeds the specified threshold.)``

    現在のテスト構成に基づいて、月ごとのテストの使用量と数の推定値が表示されます。

10. 「設定」ペインで**「編集」**をクリックして、テストの現在の設定を表示します。

    テストの間隔、テストの頻度、テストの送信元の場所を変更できます。

    ![テストのデフォルト設定を表示している「テスト設定」ペイン。](images/avmon_settings.png)

    すべての場所から同時にテストを実行する場合は**「同時」**を選択し、選択した場所を間隔ごとに 1 箇所ずつテストする場合は**「時間差」**を選択します。**「保存」**をクリックして、テストの構成を終了します。

11. **「終了」**をクリックします。{{site.data.keyword.prf_hubshort}} ダッシュボードに、すべてのテストのサマリー、アラートの重大度とロケーションを表示するマップと表、アプリケーションに関連付けられているすべてのシンセティック・テスト、アクティビティーの表、およびアプリケーションと他の Web サイトの応答時間と可用性を示す折れ線グラフが表示されます。
