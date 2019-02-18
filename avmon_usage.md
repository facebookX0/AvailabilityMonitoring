---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Service usage
{: #avmon_usage}

You can view details about your {{site.data.keyword.prf_hubshort}} usage on the **Monitoring** tab for your app, and on the {{site.data.keyword.prf_hubshort}} main dashboard.

To see an overview of your {{site.data.keyword.prf_hubshort}} usage from the **All Applications** table, click your app name; then, click the **Monitoring** tab on your app pane. Your percentage **Usage** is displayed in a gauge graphic, along with the plan that you are using.

To see an overview of your usage from the {{site.data.keyword.prf_hubshort}} main dashboard, click the **Configure** icon ![Configure icon](images/config_icn_white_smll.jpg). If you are a user of the {{site.data.keyword.prf_hubshort}} Lite plan, your usage is displayed as a bar graphic and as a percentage, along with the number of tests in use. If you are a user of the Paid plan, your usage is displayed in data points. You can view the usage details for each individual test in the Synthetic Tests pane.

Your usage is measured in data points. The estimated number of data points is calculated from the following formula:

Estimated number of data points = T \* L \* (60/M \* 24 \* 30) per month

Where T = number of synthetic tests that are executed, L = number of locations, and M = interval between tests (minutes).

Simple tests such as webpage and REST API tests use 1 data point for each test. Advanced tests such as Selenium scripts and REST API scripts use 100 data points for each test.

You can view your actual usage on the Usage Dashboard on the {{site.data.keyword.Bluemix_notm}} Account page. Click **Account**; then select **Usage Dashboard** and scroll down to the **Service Charges** section. Click the **Arrow** icon for the {{site.data.keyword.prf_hubshort}} service to view how many data points you have used. For more information about {{site.data.keyword.prf_hubshort}} pricing and usage plans, see Pricing Plans on the [Availability Monitoring](https://{DomainName}/catalog/services/availability-monitoring/ "(Opens in a new tab or window)"){: new_window} catalog page.
