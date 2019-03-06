---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-14"


keywords: launching, configuring, accessing, average availability, status overview

subcollection: availability-monitoring

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Accessing Availability Monitoring
{: #avmon_tab}

You can access the {{site.data.keyword.prf_hubshort}} dashboard from the **Monitoring** tab. The **Monitoring** tab for your Cloud Foundry application displays summary information about the availability and status of your tests, and your service subscription details and usage.
{: shortdesc}

To access {{site.data.keyword.prf_hubshort}}, complete the following steps:

1.  Click the name of a Cloud Foundry application in the **Apps** dashboard.
2.  Click the **Monitoring** tab.

The **Monitoring** tab displays three gauges that show **Average Test Availability** in the last 24 hours, **Current Test Status** of all your tests, and **Service Usage** of your allocation for your current plan.

![Availability Monitoring tab](images/avmon_tab.png)

You can configure how {{site.data.keyword.prf_hubshort}} calculates **Average Test Availability** by selecting tests for inclusion in the Availability Calculation. Click the **arrow** icon ![arrow icon](images/arrow_dwn_icn_white.jpg) on the **Average Test Availability** gauge to view your test cards; then, click **Availability Calculation**. Click a card to add or remove it from the calculation. Excluded test cards are faded. When you are finished, click **I'm Done**. The **Average Test Availability** gauge is refreshed.

You can view the status of all your tests by clicking the **arrow** icon ![arrow icon](images/arrow_dwn_icn_white.jpg) on the **Current Test Status** gauge. Test cards for your tests are displayed.

To access the {{site.data.keyword.prf_hubshort}} dashboard, click **See Monitoring Details**. From the {{site.data.keyword.prf_hubshort}} dashboard, you can monitor the availability of your application based on synthetic tests. You can also monitor the responsiveness and throughput of your application based on user transaction data that is provided by your data collectors.

To view and edit your tests in the Synthetic Tests pane, click **View All Tests**. To create a test, click **Add New Test**.

To download a .csv file report of the monthly, weekly, and daily availability and response time averages for your application, click the **Download** icon ![Download icon](images/download_icn_white_smll.jpg).
