---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Availability Monitoring 中的警报生成
{: #avmon_alert_desc}

在 {{site.data.keyword.prf_hubshort}} 中，测试最多可生成总计三个警报。测试会报告严重性最高的警报，直到导致警报的条件得到解决。
{: shortdesc}

针对三种不同的情况，会引发不同的警报：

-   当 Web 应用程序或 URL 的响应时间超过为测试设置的警告或严重阈值时。缺省情况下，每个测试都会测量响应时间，并根据该测试的警告和严重阈值引发警报。

-   当测试返回 HTTP 响应代码，指示 Web 应用程序或 URL 因客户机或服务器错误而不可用时。缺省情况下，每个测试都会检查响应代码，以确定测试是成功还是失败。

-   当测试确定满足一个或多个定制条件时，即会以一个或多个定制条件所定义的最高严重性引发警报。
当确定是否引发警报时，{{site.data.keyword.prf_hubshort}} 会综合考虑所有定制条件。
直到测试确定所有定制条件不再生成任何警告或严重警报后，此警报才会消失。


当引发多个警报时，只要存在任何警报，{{site.data.keyword.prf_hubshort}} 就会报告严重性最高的警报。

例如，如果测试响应时间引发了严重警报，另一个条件引发了警告警报，那么测试会生成严重警报，且该警报会显示在 {{site.data.keyword.prf_hubshort}} 仪表板上。如果导致严重警报的条件不再成立，那么测试警报的严重性会更改为“警告”。直到所有条件都不再导致警报，警报才会消失。

