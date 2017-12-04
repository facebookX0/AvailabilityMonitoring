---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# 服务使用情况
{: #avmon_usage}

您可以在应用程序的**监视**选项卡上和 {{site.data.keyword.prf_hubshort}} 主仪表板上，查看有关 {{site.data.keyword.prf_hubshort}} 使用情况的详细信息。

要从**所有应用程序**表中查看 {{site.data.keyword.prf_hubshort}} 使用情况的概述，请单击应用程序名称，然后单击应用程序窗格上的**监视**选项卡。此时将以标尺图形显示您的**使用情况**百分比，同时显示您使用的套餐。

要在 {{site.data.keyword.prf_hubshort}} 主仪表板上查看使用情况的概述，请单击**配置**图标 ![“配置”图标](images/config_icn_white_smll.jpg)。如果您是 {{site.data.keyword.prf_hubshort}} Lite 套餐的用户，那么将以条形图和百分比显示您的使用情况，同时还会显示使用中的测试数。如果您是付费套餐用户，那么将按数据点显示您的使用情况。您可以在“合成测试”窗格中查看各个测试的使用情况详细信息。

按数据点度量使用情况。按以下公式计算估算的数据点数：

估算的数据点数 = T \* L \* (60/M \* 24 \* 30)/月

其中，T = 执行的合成测试数，L = 位置数，M = 各测试之间的时间间隔（分钟）。

简单的测试（如网页和 REST API）每个测试仅使用 1 个数据点。高级的测试（如 Selenium 脚本和 REST API 脚本）每个测试会使用 100 个数据点。

您可以在“{{site.data.keyword.Bluemix_notm}} 帐户”页面上的“使用情况仪表板”中查看实际使用情况。单击**帐户**，然后选择**使用情况仪表板**，并向下滚动到**服务费用**部分。单击 {{site.data.keyword.prf_hubshort}} 服务的**箭头**图标可查看使用了多少个数据点。有关 {{site.data.keyword.prf_hubshort}} 定价和使用情况套餐的更多信息，请参阅 [Availability Monitoring](https://console.{DomainName}/catalog/services/availability-monitoring/ "（在新选项卡或窗口中打开）"){: new_window} 目录页面中的“价格套餐”。
