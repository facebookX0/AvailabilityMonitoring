---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-14"

keywords: Selenium, scripts, script variables, automated tests, configuring tests

subcollection: availability-monitoring
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Creating a script test from an uploaded script
{: #avmon_upload_script_test}

Upload a Selenium script to create a script test that tests the availability and performance of your web application in response to simulated user behavior.
{: shortdesc}

## Before you begin
{: #avmon_script_prereq}

Script tests require Selenium scripts to work. In order to create a script test, you must first create a Selenium script. For more information about creating Selenium scripts, see [Recording synthetic scripts](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(Opens in a new tab or window)"){: new_window}.

## About this task
{: #avmon_script_about}

Create a script test to monitor a Selenium script that simulates your users' interactions with your web application. If you create a Selenium script that mimics a user who is logging in to your application, you can then run a script test periodically to test the performance of your application in response to the simulated user actions.

## Creating a test with an uploaded script
{: #avmon_script_create_test}

To create a script test, complete the following steps.

1.  If you are viewing the Monitoring Tab, click **Add New Test**.

    ![The Monitoring tab for your Cloud Foundry application.](images/avmon_tab.png)

    If you are viewing the {{site.data.keyword.prf_hubshort}} dashboard, click **Add New Test** on the Synthetic Tests pane.

    ![The Add New Test button on the Synthetic Tests pane.](images/syn_tests_pane.jpg)

2.  Click **Scripted Behavior** on the Monitoring Setup page. The Scripted Behavior Setup page is displayed. Click **Upload File**.

    If you return to edit this test at a later point, you can download the uploaded script file. Click the **Download** icon ![Download icon](images/download_icn_white_smll.jpg) to download your script.

3.  Enter a meaningful name for your test in the **Name** field. Add a description of the purpose of your test to the **Description** field.
4.  Click **Browse** to find and upload a script file.
5.  Use the **Blacklist** and **Whitelist** to specify which URLs and domains to send requests to and which URLs and domains contribute to the metrics and status of your application tests. Add URLs and domains that you want to include or block to the **Whitelist** and **Blacklist**. For more information about blocking and filtering, see [Blocking and filtering with the whitelist and blacklist](/docs/services/AvailabilityMonitoring?topic=availability-monitoring-avmon_filters "Use the whitelist and blacklist to determine which resources to send requests to and which resources contribute to the metrics and status of your application tests. Whitelists and blacklists are only available for webpage and scripted behavior tests.").
6.  To configure your test settings, click **Next**. A summary of the test configuration is displayed. For example, the following message is displayed for the default settings:

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds 5 seconds``.

    The estimated usage and estimated number of tests per month are displayed based on your current test configuration.

7.  In the Settings pane, click **Edit** to display the current settings for your test. You can update the following settings:
    - **Interval** defines how often the test runs.
    - **Testing frequency** determines whether your test runs from all locations simultaneously or from a different location at each interval. Select **Simultaneous** to run your test from all locations simultaneously, or select **Staggered** to run your test from a different selected location at each interval.
    - **Critical Threshold** defines the response time for critical alerts for the test.
    - **Warning Threshold** defines the response time for warning alerts for the test.
    - **Locations** determines the locations where your test will run.
    - **Alert triggers** set your test to generate alerts after a set number of consecutive threshold breaches or failures.

8.  Select your locations from a list of **Public Locations**.

9.  In the **Alert Triggers** section, select the **Threshold breached consecutively** check box to set the test to generate an alert only after consecutive threshold breaches. In the **times** field, enter how many threshold breaches must take place before an alert is generated. To enable a test to report test failures, ensure that **Failure detected** is set to **On**.

    To set the test to generate an alert only after consecutive test failures, select the **Failure detected consecutively** check box. In the **times** field, enter how many failures are required before an alert is generated.

    For more information, see [Alert Triggers](/docs/services/AvailabilityMonitoring?topic=availability-monitoring-avmon_alert_triggers "Alert Triggers control when alerts for consecutive threshold breaches or consecutive test failures are generated and reported to the Availability Monitoring dashboard.")

10. If required, you can enter the values for variables that are defined in your test script. For example, if your script requires a user name and password to connect to a website, you can enter the values for these variables. You can set different values for your variables in different locations in the **Script Variables** table.

11. Click **Save** to finish configuring your test; then, click **Finish**. The {{site.data.keyword.prf_hubshort}} dashboard is displayed. After a minute, the dashboard displays information and data for your new test.
