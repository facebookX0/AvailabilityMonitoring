---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 访问 Availability Monitoring
{: #avmon_tab}

您可以通过**监视**选项卡访问 {{site.data.keyword.prf_hubshort}} 仪表板。Cloud Foundry 应用程序的**监视**选项卡显示有关测试的可用性和状态的摘要信息，还显示服务预订详细信息和使用情况。
{: shortdesc}

要访问 {{site.data.keyword.prf_hubshort}}，请完成以下步骤：

1.  单击**应用程序**仪表板中某个 Cloud Foundry 应用程序的名称。
2.  单击**监视**选项卡。

**监视**选项卡会显示三个标尺，分别标示过去 24 小时的**平均测试可用性**、所有测试的**当前测试状态**以及当前套餐分配的**服务使用情况**。


![Availability Monitoring 选项卡](images/avmon_tab.png)

可以通过选择要包含在“可用性计算”中的测试来配置 {{site.data.keyword.prf_hubshort}} 计算**平均测试可用性**的方式。单击**平均测试可用性**标尺上的**箭头**图标 ![“箭头”图标](images/arrow_dwn_icn_white.jpg) 可查看测试卡；然后单击**可用性计算**。单击某个卡即可将其添加到计算或从计算中移除。被排除的测试卡将变暗。完成后，单击**我已完成**。这将刷新**平均测试可用性**标尺。

可以通过单击**当前测试状态**标尺上的**箭头**图标 ![“箭头”图标](images/arrow_dwn_icn_white.jpg) 来查看所有测试的状态。此时将显示您的测试的测试卡。

要访问 {{site.data.keyword.prf_hubshort}} 仪表板，请单击**查看监视详细信息**。在 {{site.data.keyword.prf_hubshort}} 仪表板中，可以基于合成测试来监视应用程序的可用性。还可以基于数据收集器提供的用户交易数据来监视应用程序的响应能力和吞吐量。

要在“合成测试”窗格中查看并编辑测试，请单击**查看所有测试**。要创建测试，请单击**添加新测试**。

要下载应用程序的每月、每周和每日可用性和响应时间平均值的 .csv 文件报告，请单击**下载**图标 ![“下载”图标](images/download_icn_white_smll.jpg)。
