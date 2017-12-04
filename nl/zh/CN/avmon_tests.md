---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# 合成测试
{: #avmon_synth_tests}

在“合成测试”窗格中，您可创建、编辑、删除和查看用于监视应用程序性能与可用性的合成测试。测试会显示在“合成测试”窗格的列表或卡视图中。
{: shortdesc}

![“合成测试”窗格。](images/syn_tests_pane.jpg)

每个测试卡会显示有关测试的以下信息：

- **可用性**显示过去 24 小时内测试的可用性百分比。
- **状态**显示测试的当前状态。状态可以为“严重”、“警告”、“正常”、“失败”、“不活动”或“未知”。
- **平均响应时间**显示测试在过去 24 小时内的平均响应时间。

可以监视三个不同的测试类型：

- **REST API** 测试可报告 REST 调用的响应时间。支持所有 HTTP 请求格式，例如 GET、POST、PUT 和 DELETE。
- **Web 页面**测试可报告在输入的 URL 处装入 Web 站点的响应时间。
- **脚本行为**测试可监视创建用于模拟用户与 Web 站点交互的 Selenium 脚本。例如，可以创建 Selenium 脚本来模拟登录应用程序的用户。
定期运行此脚本可测试应用程序在响应此脚本自动执行的用户操作时的性能。您可以从 GitHub 存储库上传脚本或添加脚本。
有关创建 Selenium 脚本的更多信息，请参阅[记录合成脚本](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "（在新选项卡或窗口中打开）"){: new_window}。

要添加其他测试，请单击**添加新测试**。

要停止、启动、删除或编辑合成测试，请单击**操作**图标 ![“操作”图标](images/actions_icn_white_smll.jpg)，然后单击需要执行的操作。要查看测试的细目详细信息，请单击该测试。

要查看每个合成测试的特定使用情况，请单击**成本**图标 ![“成本”图标](images/cost_icn_white_smll.jpg)。如果您预订的是付费套餐，那么将按数据点显示您的使用情况。
