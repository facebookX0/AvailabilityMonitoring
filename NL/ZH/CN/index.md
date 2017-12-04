---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Availability Monitoring 入门
{: #avmon_gettingstarted}

使用 {{site.data.keyword.prf_hublong}} 随时随地运行模拟的性能测试。主动检测、确定和诊断性能问题，避免对用户造成影响。在进行连续更新时，请确保您的应用程序可用并满足响应时间目标。为应用程序配置数据收集器以收集用户交易数据。在 {{site.data.keyword.prf_hubshort}} 中使用这些数据来监视应用程序的响应能力和吞吐量。
{: shortdesc}

## 关于此任务
{: #avmon_start_about}

{{site.data.keyword.prf_hubshort}} 在 {{site.data.keyword.Bluemix_notm}} 目录的 DevOps 域中作为一项服务提供。缺省情况下也在**监视**选项卡的“应用程序”仪表板中提供。您可以立即开始监视应用程序可用性和性能。将 {{site.data.keyword.prf_hubshort}} 绑定到应用程序时，缺省情况下系统会自动创建合成测试，以监视主应用程序 URL。

## 创建 Web 页面测试
{: #avmon_start_procedure}

完成以下步骤，以打开应用程序的 {{site.data.keyword.prf_hubshort}}，创建 Web 页面测试以监视其他 URL，并为测试设置通知警报。

1.  如果有 Cloud Foundry 应用程序要监视，请单击**应用程序**仪表板上**所有应用程序**表中的应用程序名称。如果还没有应用程序，请进行创建，然后应用程序卡将自动打开。单击“监视”选项卡时，Cloud Foundry 应用程序会自动与 {{site.data.keyword.prf_hubshort}} 绑定。
2.  要打开 {{site.data.keyword.prf_hubshort}}，请单击**监视**选项卡。**监视**选项卡显示三个标尺，分别显示过去 24 小时的**平均测试可用性**、**当前测试状态**和当前套餐配置的**使用情况**。
单击**添加新测试**以配置监视测试。

    ![Availability Monitoring 选项卡](images/avmon_tab.png)

    缺省情况下将监视主应用程序 URL。您可以监视 Bluemix 之内或之外的任何其他 URL 和服务，这些 URL 和服务不需要与相关联的 Cloud Foundry
应用程序相关。

3.  单击“监视设置”页面上的**单个操作**，然后单击“单个操作”页面上的 **Web 页面**。
4.  在**名称**字段中为测试输入有意义的名称。在**描述**字段中添加测试目的的描述。
5.  输入要测试的 Web 应用程序的 **URL**。
6.  在“响应验证”部分中，为测试配置警告和严重警报阈值。编辑每一行的**值**和**单位**。超过警告和严重阈值的响应时间会触发警报。


    ![具有缺省“警告”和“严重”阈值的“响应验证”部分。](images/avmon_webpage_resp_val.png)

7.  使用**黑名单**和**白名单**来指定向哪些 URL 和域发送请求，以及哪些 URL 和域影响应用程序测试的度量和状态。向**白名单**和**黑名单**添加要包含或阻止的 URL 和域。有关阻止和过滤的更多信息，请参阅[使用白名单和黑名单进行阻止和过滤](avmon_whitelist_blacklist.html "使用白名单和黑名单可确定要向其发送请求的资源，以及哪些资源会影响应用程序测试的度量和状态。白名单和黑名单仅适用于 Web 页面和脚本行为测试。")。
8.  单击**验证**以创建 Web 页面测试并确定测试请求是否有效。


    {{site.data.keyword.prf_hubshort}} 通过向测试 URL 发送 GET 请求，来确定测试的有效性。在测试验证期间，不会发生响应验证。


    经验证的测试将显示在“已验证的项”表中。 您可以重复步骤 3 至 8 来添加更多 URL。

9.  要配置测试设置，请单击**下一步**。

    此时将显示测试配置的摘要。例如，这将针对缺省设置显示以下消息：

    `将进行测试：同时从 3 个位置每 15 分钟进行一次测试，以确定测试是否超过指定阈值。`

    每月估计的使用情况和估计的测试数将基于当前测试配置显示。

10. 在“设置”窗格中，单击**编辑**以显示测试的当前设置。可以更新以下设置：
    - **时间间隔**定义测试运行的频率。
    - **测试频率**确定测试是同时从所有位置运行还是在每个时间间隔从不同位置运行。选择**同时**可从所有位置同时运行测试；选择**交错**可在每个时间间隔后从选定的不同位置运行测试。
    - **位置**确定将运行测试的位置。

    单击**保存**以完成测试配置。

11. 单击**完成**。{{site.data.keyword.prf_hubshort}} 仪表板显示了全部测试的摘要、用于描述警报频率和位置的图和表、与应用程序相关联的所有合成测试、包含活动的表，以及描述应用程序和其他 Web 站点响应时间和可用性的折线图。可以根据需要创建更多测试。
12. 可以使用 {{site.data.keyword.alertnotificationfull}} 服务来配置监视功能，以在事件发生时发送通知。有关更多信息，请参阅[启用通知](avmon_notifications.html "配置监视功能以在事件发生时发送通知。")。

## 结果
{: #avmon_getstarted_results}

测试结果在测试中指定的时间间隔已过之后显示。缺省时间间隔为 15 分钟。

现在，您已经准备好监视 Web 应用程序的可用性。应用程序、Web 站点或 REST API 的响应时间和可用性信息将显示在折线图上，同时会在**响应时间和可用性**窗格中会显示有关最近活动和测试的信息。

有两个可用的指南，可帮助您了解 {{site.data.keyword.prf_hubshort}} 的功能。

 - **视频教程库** -《视频教程库》包含有关如何创建 Bluemix 应用程序、创建 Availability Monitoring 测试、使用 Selenium IDE 创建测试脚本以及向 Slack 发送警报的视频。
 - **欢迎使用 Monitoring！**-《欢迎使用 Monitoring》指南重点阐述仪表板的各区域，并说明 {{site.data.keyword.prf_hubshort}} 的每个功能。

要打开指南，请单击**帮助**图标 ![“帮助”图标](images/help_icn_white_sml.jpg)，然后单击要查看的指南。
