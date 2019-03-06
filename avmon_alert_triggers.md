---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-14"

keywords: consecutive alerts, deduplication, alert generation

subcollection: availability-monitoring

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Alert Triggers
{: #avmon_alert_triggers}

Alert Triggers control when alerts for consecutive threshold breaches or consecutive test failures are generated and reported to the {{site.data.keyword.prf_hubshort}} dashboard.
{: shortdesc}

{{site.data.keyword.prf_hubshort}} generates a consecutive threshold breach alert after a test reports an unbroken sequence of warning or critical threshold breaches across the PoP locations for that test. {{site.data.keyword.prf_hubshort}} can also generate a failure alert after a test reports an unbroken sequence of test failures across the PoP locations for that test.

{{site.data.keyword.prf_hubshort}} only raises consecutive alerts for threshold alerts and failure alerts. Consecutive alert detection is not enabled for customized response validation conditions (**Header Response Code**, **Header Property**, and **Body JSON**). For more information, see [Creating a REST API test](/docs/services/AvailabilityMonitoring?topic=availability-monitoring-avmon_rest_api "Create a REST API test to test the response time and availability of your web application by using the following HTTP methods: GET, POST, PUT, and DELETE.")
{: tip}

When **Alert Triggers** generate an alert for your test, that alert suggests that your web application is unavailable or slow. A test instance can fail or perform poorly for reasons that are related to the PoP location where it runs rather than the web application. But a test that reports failures or threshold breaches consecutively across several locations indicates a potential issue with the web application.

{{site.data.keyword.prf_hubshort}} uses the following rules to generate alerts for consecutive threshold breaches or failures:

-   Consecutive threshold breaches or failures are evaluated in the order that test instance results are received by {{site.data.keyword.prf_hubshort}} and not in the order that each test instance starts. For tests running in multiple PoP locations, the test results from all PoP locations are evaluated in the order in which they are received. This order is used to determine whether a consecutive alert is generated for a test result on a PoP location. If a test runs in only one PoP location, the test results at subsequent intervals are used to determine whether a consecutive alert is generated.

    The order of test instances displayed on the **Alert Frequency** table can differ from the order of test instances in a consecutive sequence of alerts. {{site.data.keyword.prf_hubshort}} displays the timestamp of the start time of synthetic tests in the **Alert Frequency**, **Test Instances**, and **Response Time** panes. Consecutive alerts are determined according to the completion time (start time + response time) of each test instance.
    {: tip}

-   {{site.data.keyword.prf_hubshort}} generates an alert of the highest severity possible after consecutive threshold breaches. For example, a test is configured to run at 2 PoP locations and to trigger an alert after 3 consecutive threshold breaches. The test reports a warning alert, a critical alert, and a critical alert in sequence. {{site.data.keyword.prf_hubshort}} generates a warning alert for those 3 consecutive threshold breaches. If the next test instance in the sequence reports a critical alert, then a critical alert for 3 consective critical threshold breaches is generated.

-   {{site.data.keyword.prf_hubshort}} ignores a failed test playback instance when it determines whether the conditions for an Alert Trigger for consecutive threshold breaches are met. For example, a test is configured to run at 1 PoP location and to trigger an alert after 3 consecutive threshold breaches. The test reports a warning alert, a failed test, a warning alert, and a critical alert in subsequent intervals. {{site.data.keyword.prf_hubshort}} ignores the failed test result and generates a warning alert for 3 consecutive threshold breaches after the fourth test result.

-   If an alert for consecutive threshold breaches is in place for a PoP, that alert is not cleared until that PoP reports an acceptable response time.

-   A failed test playback instance does not clear an existing alert, including alerts for consecutive threshold breaches.

-   Alerts that are generated before you configure {{site.data.keyword.prf_hubshort}} to generate alerts for consecutive threshold breaches or failures stay open.

This example shows how these rules can affect alert generation. The following table shows a test that runs at 3 PoP locations. **Testing Frequency** set to staggered, and the test is configured to trigger an alert after 3 consecutive threshold breaches and 3 consecutive test failures. In this example, test results are returned in the order PoP A -> PoP B -> PoP C.

<table style="width:60%" id="avmon_alert_trigger_example">
<caption>Table 1. Results of a test that runs at 3 PoP locations with alert triggers for 3 consecutive threshold breaches and 3 consecutive test failures.</caption>
<thead>
<tr>
<th>PoP</th>
<th>Interval 1</th>
<th>Interval 2</th>
<th>Interval 3</th>
<th>Interval 4</th>
<th>Interval 5</th>
<th>Interval 6</th>
</tr>
</thead>
<tbody>
<tr>
<td>A</td>
<td>Normal</td>
<td>Critical</td>
<td>Failure</td>
<td>Failure</td>
<td>Failure</td>
<td>Normal</td>
</tr>
<tr>
<td>B</td>
<td>Warning</td>
<td>Critical</td>
<td>Normal</td>
<td>Failure</td>
<td>Warning</td>
<td>Normal</td>
</tr>
<tr>
<td>C</td>
<td>Critical</td>
<td>Failure</td>
<td>Failure</td>
<td>Warning</td>
<td>Critical</td>
<td>Normal</td>
</tr>
</tbody>
</table>

The following table describes which alerts are generated and cleared by interval for the test.

<table id="avmon_alert_trigger_example_explanation">
<caption>Table 2. Consecutive alerts generated and cleared by interval.</caption>
<thead>
<tr>
<th>Interval</th>
<th>Result</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>No consecutive alerts are generated.</td>
</tr>
<tr>
<td>2</td>
<td>Warning alert for consecutive threshold breaches on PoP A. Critical alert for consecutive threshold breaches on PoP B. No alert on PoP C.</td>
</tr>
<tr>
<td>3</td>
<td>Warning alert for consecutive threshold breaches remains on PoP A as a failed test does not remove that alert. Critical alert for consecutive threshold breaches is cleared on PoP B. No consecutive alert on PoP C.</td>
</tr>
<tr>
<td>4</td>
<td>Warning alert for consecutive threshold breaches remains on PoP A as a failed test does not remove that alert. Alert for consecutive failures is generated on PoP B. No consecutive alert on PoP C.</td>
</tr>
<tr>
<td>5</td>
<td>Warning alert for consecutive threshold breaches remains on PoP A as a failed test does not remove that alert. Alert for consecutive failures is cleared on PoP B because the test runs successfully, even though it breaches a threshold. Warning alert for consecutive threshold breaches is generated on PoP C.</td>
</tr>
<tr>
<td>6</td>
<td>Warning alert for consecutive threshold breaches is cleared on PoP A. There is no consecutive alert on PoP B. The warning alert for consecutive threshold breaches is cleared on PoP C.</td>
</tr>
</tbody>
</table>

Results appear on the **Alert Frequency** map and table and on the **Breakdown** dashboard for the relevant test.
