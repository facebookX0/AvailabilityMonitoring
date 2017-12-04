---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 从 GitHub 存储库中的脚本创建脚本测试
{: #avmon_git_script_test}

从存储在 GitHub 存储库中的 Selenium 脚本创建脚本测试。您可以启用脚本测试，以持续与 GitHub 存储库中 Selenium 脚本的任何更改同步。
{: shortdesc}

## 开始之前
{: #avmon_git_prereq}

脚本测试需要 Selenium 脚本才能运作。要创建脚本测试，必须先创建 Selenium 脚本。有关创建 Selenium 脚本的更多信息，请参阅[记录合成脚本](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "（在新选项卡或窗口中打开）"){: new_window}。

要从存储在 GitHub 存储库中的 Selenium 脚本创建脚本测试，必须完成以下步骤：

-   为应用程序启用 {{site.data.keyword.contdelivery_full}}。有关更多信息，请参阅 [Continuous Delivery](../ContinuousDelivery/index.html "（在新选项卡或窗口中打开）"){: new_window}。
-   授权 {{site.data.keyword.Bluemix_notm}} 访问作为工具链一部分的 GitHub。有关更多信息，请参阅[配置 GitHub](../ContinuousDelivery/toolchains_integrations.html#github "（在新选项卡或窗口中打开）"){: new_window}。

## 关于此任务
{: #avmon_git_about}

如果为应用程序启用了 {{site.data.keyword.contdelivery_short}}，那么您可以创建脚本测试，用于与 GitHub 存储库中的 Selenium 脚本同步。如果创建 Selenium 脚本来模拟应用程序的用户，那么可以定期运行脚本测试，以测试应用程序在响应模拟用户操作时的性能。

## 创建使用 GitHub 脚本的测试
{: #avmon_git_create_test}

要创建脚本测试，请完成以下步骤。

1.  如果您正在查看“监视”选项卡，请单击**添加新测试**。

    ![Cloud Foundry 应用程序的“监视”选项卡。](images/avmon_tab.png)

    如果您正在查看 {{site.data.keyword.prf_hubshort}} 仪表板，请单击“合成测试”窗格上的**添加新测试**。

    ![“合成测试”窗格上的“添加新测试”按钮。](images/syn_tests_pane.jpg)

2.  单击“监视设置”页面上的**脚本行为**。这将显示“脚本行为设置”页面。单击 **Git 存储库**。
3.  在**名称**字段中为测试输入有意义的名称。在**描述**字段中添加测试目的的描述。
4.  选择可用的 GitHub 存储库，然后输入所选存储库中脚本的文件路径。
5.  要确保测试持续使用 **Git 存储库**中最新版本的 Selenium 脚本，请选择**通过 Delivery Pipeline 自动同步脚本**。
6.  使用**黑名单**和**白名单**来指定向哪些 URL 和域发送请求，以及哪些 URL 和域影响应用程序测试的度量和状态。向**白名单**和**黑名单**添加要包含或阻止的 URL 和域。有关阻止和过滤的更多信息，请参阅[使用白名单和黑名单进行阻止和过滤](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "使用白名单和黑名单可确定要向其发送请求的资源，以及哪些资源会影响应用程序测试的度量和状态。白名单和黑名单仅适用于 Web 页面和脚本行为测试。")。
7.  要配置测试设置，请单击**下一步**。此时将显示测试配置的摘要。例如，这将针对缺省设置显示以下消息：

    ``测试将每 15 分钟同时从 3 个位置执行一次，以确定测试是否超过 5 秒``。

    每月估计的使用情况和估计的测试数将基于当前测试配置显示。

8.  在“设置”窗格中，单击**编辑**以显示测试的当前设置。可以更新以下设置：
    - **时间间隔**定义测试运行的频率。
    - **测试频率**确定测试是同时从所有位置运行还是在每个时间间隔从不同位置运行。选择**同时**可从所有位置同时运行测试；选择**交错**可在每个时间间隔后从选定的不同位置运行测试。
    - **严重阈值**定义测试的严重警报的响应时间。
    - **警告阈值**定义测试的警告警报的响应时间。
    - **位置**确定将运行测试的位置。

    如果需要，可以为测试脚本中定义的变量输入值。例如，如果您的脚本需要用户名和密码来连接 Web 站点，可以输入这些变量的值。您可以在**脚本变量**表中为不同位置的变量设置不同的值。

    单击**保存**以完成测试配置。

9.  单击**完成**。{{site.data.keyword.prf_hubshort}} 仪表板显示了所有测试的摘要、用于显示警报严重性和位置的图和表、与应用程序相关联的所有合成测试、包含活动的表，以及描述应用程序和其他 Web 站点的响应时间和可用性的折线图。
