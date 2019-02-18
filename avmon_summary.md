---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-14"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Application Summary
{: #avmon_summary_pane}

The Application Summary pane displays an overview of current test status, alerts, team activity, and application availability data.
{: shortdesc}

![The Application Summary pane](images/avmon_test_summ2.png)

The Application Summary pane displays the following information:

- **Current Status** displays the highest severity status of all your tests. The severity can be Normal, Warning, or Critical.
- **Alerts (Past 24 Hrs)** displays the number of open, critical, and warning alerts.
- **Activities (Past 24 Hrs)** displays the number of activities for this application. Bluemix activities are application events that take place in {{site.data.keyword.Bluemix_notm}}, such as your application stopping, starting, or being restaged. Pipeline activities are events that take place in your {{site.data.keyword.contdelivery_short}} toolchain with the {{site.data.keyword.DRA_full}} service, such as builds, deployments, and tests. Click the **Setup** link to connect your application to a toolchain that includes the {{site.data.keyword.DRA_short}} service.
- Use **Availability Report** to download a .csv file report of the monthly, weekly, and daily availability and response time averages for the application. Click the **Download** icon ![Download icon](images/download_icn_white_smll.jpg) to download the report.
