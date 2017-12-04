---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Alertgenerierung in Availability Monitoring
{: #avmon_alert_desc}

In {{site.data.keyword.prf_hubshort}} können durch Tests insgesamt bis zu drei Alerts generiert werden. Im Test wird der Alert mit dem höchsten Schweregrad gemeldet, bis die Bedingung behoben ist, durch die der Alert verursacht wurde.
{: shortdesc}

Für die folgenden drei weiteren Situationen wird ein separater Alert ausgelöst:

-   Wenn die Antwortzeit Ihrer Webanwendung oder URL den für Ihren Test festgelegten Warnungsschwellenwert oder kritischen Schwellenwert überschreitet. Bei jedem Test wird standardmäßig die Antwortzeit gemessen und ein Alert ausgelöst, wenn der Warnungsschwellenwert oder der kritische Schwellenwert für den Test überschritten wird.
-   Wenn Ihr Test einen HTTP-Antwortcode zurückgibt, der angibt, dass Ihre Webanwendung oder URL aufgrund eines Client- oder Serverfehlers nicht verfügbar ist. Bei jedem Test wird standardmäßig der Antwortcode überprüft, um zu ermitteln, ob der Test erfolgreich ist oder fehlschlägt.
-   Wenn Ihr Test feststellt, dass mindestens eine angepasste Bedingung erfüllt ist, wird eine Alarmnachricht mit der höchsten Priorität ausgelöst, die in mindestens einer Ihrer angepassten Bedingungen definiert ist. {{site.data.keyword.prf_hubshort}} berücksichtigt alle angepassten Bedingungen kumulierend, um zu ermitteln, ob ein Alarm ausgelöst wird. Der ausgelöste Alarm bleibt bestehen, bis Ihr Test feststellt, dass Ihre angepassten Bedingungen keine Alerts für Warnungsschwellenwerte oder kritische Schwellenwerte mehr auslösen.

Wenn mehrere Alerts auftreten, wird von {{site.data.keyword.prf_hubshort}} der Alert mit dem höchsten Schweregrad gemeldet, so lange Alerts auftreten.

Wenn zum Beispiel in der Testantwortzeit ein Warnungsalert auftritt und aufgrund einer weiteren Bedingung ein Warnungsalert auftritt, wird vom Test ein kritischer Alert generiert und im {{site.data.keyword.prf_hubshort}}-Dashboard angezeigt. Wenn die Bedingung, die einen kritischen Alert ausgelöst hat, nicht länger zutrifft, wird die Priorität Ihres Testalerts in 'Warnung' geändert. Ein Alert bleibt bestehen, bis die bestehenden Bedingungen keinen Alert mehr auslösen.
