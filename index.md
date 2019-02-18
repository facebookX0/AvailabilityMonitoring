---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Getting started with Availability Monitoring
{: #avmon_gettingstarted}

Use {{site.data.keyword.prf_hublong}} to run simulated performance tests from locations around the world, around the clock. Proactively detect, isolate, and diagnose performance issues before they impact your users. Ensure that your applications are available and meet response time targets when you roll out continuous updates. Configure data collectors for your applications to collect user transaction data. Use this data in {{site.data.keyword.prf_hubshort}} to monitor the responsiveness and throughput of your application.
{: shortdesc}

## About this task
{: #avmon_start_about}

{{site.data.keyword.prf_hubshort}} is available as a service in the DevOps domain in the {{site.data.keyword.Bluemix_notm}} catalog. It is also available by default in the Application dashboard on the **Monitoring** tab. You can start monitoring your application availability and performance immediately. When you bind {{site.data.keyword.prf_hubshort}} to your application, a synthetic test is automatically created to monitor the main application URL by default.

## Creating a webpage test
{: #avmon_start_procedure}

Complete the following steps to open {{site.data.keyword.prf_hubshort}} for your application, to create a webpage test to monitor another URL, and to set up notification alerts for your tests.

1.  If you have a Cloud Foundry application that you want to monitor, click the application name in the **All Applications** table on the **Apps** dashboard. If you do not have an application yet, create it and the application card opens automatically. Cloud Foundry applications are automatically bound with {{site.data.keyword.prf_hubshort}} when you click the Monitoring tab.
2.  To open {{site.data.keyword.prf_hubshort}}, click the **Monitoring** tab. The **Monitoring** tab displays three gauges that show **Average Test Availability** in the last 24 hours, **Current Test Status**, and **Usage** of your current plan allocation. Click **Add New Test** to configure a monitoring test.

    ![Availability Monitoring tab](images/avmon_tab.png)

    The main application URL is monitored by default. Any other URLs and services that you monitor can be inside or outside of Bluemix and do not need to be related to the associated Cloud Foundry application.

3.  Click **Single Action** on the Monitoring Setup page; then, click **Webpage** on the Single Action page.
4.  Enter a meaningful name for your test in the **Name** field. Add a description of the purpose of your test to the **Description** field.
5.  Enter the **URL** of the web application that you want to test.
6.  Configure the warning and critical alert thresholds for your test in the Response Validation section. Edit the **Value** and **Unit** for each row. Response times that exceed your warning and critical thresholds trigger alerts.

    ![Response Validation section with default warning and critical thresholds.](images/avmon_webpage_resp_val.png)

7.  Use the **Blacklist** and **Whitelist** to specify which URLs and domains to send requests to and which URLs and domains contribute to the metrics and status of your application tests. Add URLs and domains that you want to include or block to the **Whitelist** and **Blacklist**. For more information about blocking and filtering, see [Blocking and filtering with the whitelist and blacklist](/docs/services/AvailabilityMonitoring?topic=availability-monitoring-avmon_filters "Use the whitelist and blacklist to determine which resources to send requests to and which resources contribute to the metrics and status of your application tests. Whitelists and blacklists are only available for webpage and scripted behavior tests.").
8.  Click **Verify** to create your webpage test and to determine whether your test request is valid.

    {{site.data.keyword.prf_hubshort}} determines the test validity by sending a GET request to your test URL. No response validation takes place during test verification.

    Your validated test is displayed in the Verified Items table. You can add more URLs by repeating steps 3 - 8.

9.  To configure your test settings, click **Next**. A summary of the test configuration is displayed. For example, the following message is displayed for the default settings:

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds the specified threshold``.

    The estimated usage and estimated number of tests per month are displayed based on your current test configuration.

10.  In the **Settings** pane, click **Edit** to display the current settings for your test. You can update the following settings:
    - **Interval** defines how often the test runs.
    - **Testing frequency** determines whether your test runs from all locations simultaneously or from a different location at each interval. Select **Simultaneous** to run your test from all locations simultaneously, or select **Staggered** to run your test from a different selected location at each interval.
    - **Locations** determines the locations where your test will run.
    - **Alert triggers** set your test to generate alerts after a set number of consecutive threshold breaches or failures.

11. Select your locations from a list of **Public Locations**.

12. In the **Alert Triggers** section, select the **Threshold breached consecutively** check box to set the test to generate an alert only after consecutive threshold breaches. In the **times** field, enter how many threshold breaches must take place before an alert is generated. To enable a test to report test failures, ensure that **Failure detected** is set to **On**.

    To set the test to generate an alert only after consecutive test failures, select the **Failure detected consecutively** check box. In the **times** field, enter how many failures are required before an alert is generated.

    For more information, see [Alert Triggers](/docs/services/AvailabilityMonitoring?topic=availability-monitoring-avmon_alert_triggers "Alert Triggers control when alerts for consecutive threshold breaches or consecutive test failures are generated and reported to the Availability Monitoring dashboard.")

12. Click **Save** to finish configuring your test; then, click **Finish**. The {{site.data.keyword.prf_hubshort}} dashboard is displayed. After a minute, the dashboard displays information and data for your new test.

13. You can use the {{site.data.keyword.alertnotificationfull}} service to configure the monitoring feature to send notifications when an event occurs. For more information, see [Enabling notifications](/docs/services/AvailabilityMonitoring?topic=availability-monitoring-avmon_notifications "Configure the monitoring feature to send notifications when an event occurs.").

## Results
{: #avmon_getstarted_results}

The test results are displayed after the interval that you specified in the test elapses. The default interval is 15 minutes.

You are now ready to monitor the availability of your web applications. The response time and availability information for your application, website, or REST API is displayed on a line graph along with information about recent activities and tests in the **Response Time and Availability** pane.

There are two guides available to help you to learn about the features of {{site.data.keyword.prf_hubshort}}.

 - **Video tutorial library** - The Video tutorial library contains videos on how to create Bluemix applications, create Availability Monitoring tests, create test scripts with Selenium IDE, and send alerts to Slack.
 - **Welcome to Monitoring!** - The Welcome to Monitoring guide highlights areas of the dashboard and explains each feature of {{site.data.keyword.prf_hubshort}}.

To open a guide, click the **Help** icon ![Help icon](images/help_icn_white_sml.jpg); then, click the guide that you want to view.
