---

copyright:
  years: 2015, 2018
lastupdated: "2018-03-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Synthetic Tests
{: #avmon_synth_tests}

In the Synthetic Tests pane, you can create, edit, delete, and view synthetic tests that monitor the performance and availability of your applications. Tests are displayed in a list or card view in the Synthetic Tests pane.
{: shortdesc}

![The Synthetic Tests pane.](images/syn_tests_pane.jpg)

Each test card displays information about the test:

- **Availability** displays the percentage availability of the test over the past 24 hours.
- **Status** displays the current status of the test. The status can be Critical, Warning, Normal, Failed, Inactive, or Unknown.
- **Avg. Response** displays the average response time of the test over the past 24 hours.

You can monitor three different types of test:

- **REST API** tests report the response time of a REST call. All HTTP request formats, such as GET, POST, PUT, and DELETE are supported.
- **Webpage** tests report the response time for loading the website at the URL that you enter.
- **Scripted behavior** tests monitor Selenium scripts that you create to mimic a user's interactions with a website. For example, you can create a Selenium script that mimics a user who is logging in to your application. You run this script periodically to test the performance of your application in response to the user actions that are automated by the script. You can upload a script or add a script from a GitHub repository. For more information about creating Selenium scripts, see [Recording synthetic scripts](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(Opens in a new tab or window)"){: new_window}.

To add another test, click **Add New Test**.

To stop, start, delete, or edit a synthetic test, click the **Actions** icon ![Actions icon](images/actions_icn_white_smll.jpg) and click the action that you want. To view the Breakdown details of the test, click the test.

To view the specific usage of each synthetic test, click the **Cost** icon ![Cost icon](images/cost_icn_white_smll.jpg). If you are subcribed to the paid plan, your usage is displayed in data points.

## Synthetic tests that share monitored hosts
{: #avmon_synth_tests_shared_hosts}

The Synthetic Tests pane displays all synthetic tests that share a monitored host. If you have more than one {{site.data.keyword.Bluemix_notm}} application bound to {{site.data.keyword.prf_hubshort}}, and if several applications contain different synthetic tests that share the same monitored host, the Synthetic Tests pane displays all synthetic tests for that monitored host including tests that were created for other applications.

For example: Application A has an associated synthetic test ('Test app A') that monitors its location app-a.mybluemix.net. Application B has an associated synthetic test ('Test app B') that monitors its location app-b.mybluemix.net. If you create another test for Application B ('Test app A from app B') that monitors the URL of application A, the Synthetic Tests pane for application B will display the following 3 tests:

- 'Test app B'
- 'Test app A from app B'
- 'Test app A'

'Test app A from app B' and 'Test app A' share the same monitored host, and are displayed in the Synthetic Tests pane for Application B. The Synthetic Tests pane for Application A will display 'Test app A' and 'Test app A from app B'.

It is recommended that you organize your tests so that all synthetic tests for a particular host are attached to one application. To reorganize your tests, complete the following steps.

1. Choose or create an application for all tests that share a monitored host.
2. Create a new synthetic test to monitor that host. The Synthetic Tests pane displays all tests that share that monitored host.
3. Create duplicates of the tests that you want to keep for your current application.
4. Delete the old tests to remove them from all applications.
  **Important**: Displayed tests from other applications are not duplicates. If you delete a test that is visible from another application, that test is deleted from all applications.
