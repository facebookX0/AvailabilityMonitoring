---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Antwortzeit und Verfügbarkeit
{: #avmon_resptime_avail}

Im Bereich 'Antwortzeit und Verfügbarkeit' können Sie Antwortzeiten, Verfügbarkeitstrends, Alerts und Aktivitäten im Zeitverlauf darstellen. Die unkomplizierte Korrelation von Metriken, Alerts und Aktivitäten hilft Ihnen, eine bestimmte Änderung einfach an einer Anwendung oder Codebereitstellung einzugrenzen, wenn Sie eine zu lange Antwortzeit feststellen.
{: shortdesc}

## Antwortzeit
{: #avmon_resptime_graph}

Informationen zur Antwortzeit werden in einem Liniendiagramm angezeigt. Zum Anzeigen des Diagramms klicken Sie auf die Registerkarte **Antwortzeit**.

![Diagramm der Antwortzeiten für einen Test für die letzten 24 Stunden](images/avmon_rt_gr.jpg)

Von {{site.data.keyword.prf_hubshort}} gemessene Antwortzeiten sind etwas länger als die Antwortzeiten, die Benutzer erleben. {{site.data.keyword.prf_hubshort}} simuliert praxisnahes Benutzerverhalten, was einen erhöhten Systemaufwand für das Messen von Antwortzeiten bedeutet. Aufgrund der folgenden Faktoren kommt es zu diesem erhöhten Systemaufwand:
  - {{site.data.keyword.prf_hubshort}} erstellt für jeden Test eine neue Firefox-Instanz, um zu verhindern, dass frühere Wiedergaben den aktuellen Test beeinflussen. Für echte Endbenutzer kann es aufgrund von Browser-Caching zu schnelleren Antwortzeiten kommen.
  - {{site.data.keyword.prf_hubshort}} installiert vor jedem Test das Firefox-Webtreiber-Plug-in.
{: tip}

Einzelne Antwortzeiten für Tests werden durch das Symbol **Antwortpunkt** ![Antwortpunktsymbol](images/crcl_icn_white.jpg) im Kurvendiagramm dargestellt. Unterschiedliche Farben bezeichnen unterschiedliche Standorte, an denen die Anwendung ausgeführt wird. Auf der Y-Achse des Diagramms werden die Bereiche für den Warnungsschwellenwert und den kritischen Schwellenwert durch Altertsymbolee dargestellt. Das gelbe Symbol **Warnung** ![Gelbes Symbol 'Warnung'](images/alrt_icn_white_smll.jpg) gibt den Bereich für den Warnungsschwellenwert an und das rote Symbol **Kritisch** ![Rotes Symbol 'Kritisch'](images/wrng_icn_white_smll.jpg) gibt den Bereich für den kritischen Schwellenwert an. Klicken Sie auf das gelbe Symbol **Warnung** ![Gelbes Symbol 'Warnung'](images/alrt_icn_white_smll.jpg) oder das rote Symbol **Kritisch** ![Rotes Symbol 'Kritisch'](images/wrng_icn_white_smll.jpg), um ohne großen Aufwand die Testinstanzen der Bereiche für den Schwellenwert für 'Warnung' bzw. 'Kritisch' zu ermitteln. Klicken Sie zum Anzeigen der Details für eine bestimmte Testinstanz auf das Symbol **Antwortpunkt** ![Symbol 'Antwortpunkt'](images/crcl_icn_white.jpg) im Diagramm.

### Filter

Wählen Sie im Dropdown-Menü **Test** einen Test aus. Sie können als Vorgabe zur Datenfilterung 3 Stunden, 24 Stunden, 7 Tage, 30 Tage und 12 Monate angeben. Die Möglichkeit, Daten über 12 Monate hinweg anzuzeigen, steht nur Benutzern mit einem bezahlten Abonnement für {{site.data.keyword.prf_hubshort}} zur Verfügung. Wenn Sie Daten anhand eines Zeitraums von mehr als 24 Stunden filtern, werden die Werte im Diagramm als Durchschnittswerte angezeigt. Klicken Sie zum Anzeigen bestimmter Informationen auf das Diagramm, um die einzelnen Alerts und Warnungen genauer zu untersuchen. Sie können den Zeitraum auch mit dem Schieberegler verkürzen oder erweitern.

Mit dem Antwortzeitdiagramm können Sie die Daten von bestimmten PoP-Standorten (PoP - Point of Presence) hervorheben bzw. ausblenden. Bewegen Sie zum Hervorheben der Antwortzeitdaten für einen bestimmten Standort den Mauszeiger über den PoP-Standortnamen; klicken Sie anschließend auf das Symbol **Standort hervorheben** ![Symbol 'Standort hervorheben'](images/avmon_location_highlight.jpg). Bewegen Sie zum Ausblenden der Antwortzeitdaten für einen Standort den Mauszeiger über den PoP-Standortnamen; klicken Sie anschließend auf das Symbol **Standort ausblenden** ![Symbol 'Standort ausblenden'](images/avmon_location_remove.jpg). Klicken Sie zum Wiederherstellen von PoP-Standortdaten auf das Diagramm, klicken Sie auf **Mehr Standorte hinzufügen** ![Symbol 'Mehr Standorte hinzufügen'](images/icn_plus_20x20.jpg) oder die Registerkarte **Metrikauswahl**; klicken Sie anschließend auf den PoP-Standort, den Sie vorher entfernt haben.

### Alerts und Aktivitäten

Alerts für Warnungen und kritische Alerts sind in der Zeile 'Alerts' leicht zu erkennen. Bewegen Sie den Mauszeiger über ein **Alertsymbol** ![Symbol für kritischen Alert](images/avmon_crit_alert.png)![Symbol für Warnungsalert](images/avmon_warn_alert.png), um den Schweregrad und die Zeitmarke für diesen Alert anzuzeigen. Klicken Sie auf ein **Alertsymbol**, um Details zu dem betreffenden Alert im Bereich **Metrikfeed** anzuzeigen.

Im gleichen Diagramm können Sie auch Aktivitäten anzeigen. _Aktivitäten_ sind Aktionen, die keine benutzerdefinierten Ereignisse sind. {{site.data.keyword.Bluemix_notm}}-Aktivitäten sind Anwendungsereignisse, die in {{site.data.keyword.Bluemix_notm}} auftreten, zum Beispiel das Starten oder Stoppen einer Anwendung oder ein erneutes Staging. Pipeline-Aktivitäten sind Ereignisse, die in Ihrer {{site.data.keyword.contdelivery_short}}-Toolchain auftreten, z. B. Builds, Bereitstellungen und Tests. Klicken Sie auf eine Aktivität, um Informationen zu der Aktivität im **Metrikfeed** anzuzeigen. Sie können Informationen zu diesen Aktivitäten im Fenster 'Aktivität' anzeigen.

Um Pipeline-Aktivitäten im {{site.data.keyword.prf_hubshort}}-Dashboard anzuzeigen, müssen Sie zunächst {{site.data.keyword.contdelivery_short}} für Ihre Anwendung aktivieren und eine Toolchain konfigurieren, die eine Pipeline und den {{site.data.keyword.DRA_short}}-Service enthält. Klicken Sie im Bereich 'Zusammenfassung' oder im Bereich 'Aktivität' auf **Aufbau einer Pipeline**, um eine Toolchain für Ihre Anwendung zu erstellen. Weitere Informationen finden Sie unter [Einführung in Continuous Delivery](../ContinuousDelivery/index.html "(Wird in neuer Registerkarte oder neuem Fenster geöffnet)") und [Einführung in DevOps Insights](../DevOpsInsights/index.html#gettingstarted "(Wird in neuer Registerkarte oder neuem Fenster geöffnet)"){: new_window}.
{: tip}

Falls sich mehrere Aktivitäts- oder Alertsymbole gemeinsam in der Nähe der Zeilen für Alerts und Aktivitäten befinden, wird von einem **Nummernsymbol** die Anzahl der Alerts oder Aktivitäten zu diesem Zeitpunkt angezeigt. Bewegen Sie den Mauszeiger über ein **Nummernsymbol**, um die einzelnen Alerts bzw. Aktivitäten anzuzeigen und klicken Sie auf einen Alert bzw. eine Aktivität, um die Informationen im **Metrikfeed** anzuzeigen.

### Metrikauswahl und Metrikfeed

Um Metriken nach geografischer Region zu filtern, klicken Sie auf **Metrikauswahl**. Klicken Sie auf einen Standort, um Metriken, die an diesem Standort gemessen werden, im Diagramm hinzuzufügen oder zu entfernen. Klicken Sie auf **Mehr Standorte hinzufügen**, um die Seite 'Testbearbeitungsmodus' zu öffnen und einen PoP-Standort zu Ihrem ausgewählten Test hinzuzufügen.

![Registerkarte 'Metrikauswahl' mit PoP-Standortfilter](images/avmon_metric_sel.jpg)

Um eine Liste der Metrikdetails anzuzeigen, klicken Sie auf **Metrikfeed**. Im Metrikfeed wird eine Liste der Instanzen angezeigt, bei denen eine Metrik gegeben ist.

![Registerkarte 'Metrikfeed' mit Details eines Warnungsalerts](images/avmon_warn_met_feed.png)

Klicken Sie auf ein **Alertsymbol**, **Aktivitätssymbol** oder einen **Antwortpunkt** ![Symbol für Antwortpunkt](images/crcl_icn_white.jpg) im Diagramm, um Details dieser Metrik zum Metrikfeed hinzuzufügen.

![Details einer verfügbaren Testinstanz im Metrikfeed](images/avmon_avail_metfeed.png)

Wenn Sie das Antwortzeitdiagramm anhand eines Zeitraums von mehr als 24 Stunden filtern und auf einen **Antwortpunkt** klicken, können zusammengefasste Details für diesen Tag im Metrikfeed angezeigt werden.

![Metrikfeed mit zusammengefassten Details aller Instanzen eines Tests für einen Tag](images/avmon_avail_day_met_feed.png)

Klicken Sie auf **Zoom**, um alle Antwortzeiten, Aktivitäten und Alerts, die durch den Test für diesen Tag generiert wurden, im Antwortzeitdiagramm anzuzeigen.

Um ausführliche Informationen zu einer Alert- oder Testantwortzeit anzuzeigen, klicken Sie auf **Aufgliederung** im Metrikfeed. Klicken Sie auf **Nächstgelegener Alert**, um den nächstgelegenen Alert für diese Testinstanz im Metrikfeed anzuzeigen, sofern ein Alert aufgetreten ist. Um detaillierte Informationen zu einer Pipeline-Aktivität im {{site.data.keyword.DRA_short}}-Service anzuzeigen, klicken Sie auf **Insights anzeigen** im Metrikfeed.

## Verfügbarkeit
{: #avmon_avail_graph}

Zum Anzeigen der Verfügbarkeitsinformationen zu Ihren Anwendungen klicken Sie auf 'Verfügbarkeit'. Im Verfügbarkeitsdiagramm wird die tägliche Verfügbarkeit für jeden Bereitstellungspunkt (Point of Presence, PoP) für den ausgewählten Test angezeigt.

![Verfügbarkeitsdiagramm mit täglicher Testverfügbarkeit nach Standort für die letzten sieben Tage](images/avmon_avail_graph.png)

Mit dem Verfügbarkeitsdiagramm können die Daten von bestimmten PoP-Standorten (Points of Presence) hervorgehoben bzw. ausgeblendet werden. Bewegen Sie den Mauszeiger zum Hervorheben der Verfügbarkeitsdaten für einen bestimmten Standort über **PoP-Standortname**; klicken Sie anschließend auf das Symbol **Standort hervorheben** ![Symbol 'Standort hervorheben'](images/avmon_location_highlight.jpg). Bewegen Sie den Mauszeiger zum Ausblenden der Verfügbarkeitsdaten für einen Standort über **PoP-Standortname**; klicken Sie anschließend auf das Symbol **Standort ausblenden** ![Symbol 'Standort ausblenden'](images/avmon_location_remove.jpg). Um PoP-Standortdaten im Diagramm wiederherzustellen, klicken Sie auf die Registerkarte **Metrikauswahl**; klicken Sie anschließend auf den PoP-Standort, den Sie zuvor entfernt haben.

Bewegen Sie den Mauszeiger über einen Punkt in dem Diagramm, um die Fehlerrate und die Anzahl der Testinstanzen für einen bestimmten Tag und Standort anzuzeigen. Klicken Sie auf einen Punkt im Diagramm, um diese Informationen im Metrikfeed anzuzeigen.

![Testverfügbarkeit am PoP 'Dallas' im Metrikfeed](images/avmon_avail_metric.png)

Klicken Sie auf **Zoom**, um das Diagramm 'Verfügbarkeit' und das Diagramm 'Antwortzeit' zu filtern und Informationen für den ausgewählten Tag anzuzeigen.
