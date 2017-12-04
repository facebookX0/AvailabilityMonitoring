---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}


# Actividad
{: #avmon_activities}

Ver información para actividades en el panel Actividad. Las _actividades_ son acciones que se producen fuera de los sucesos definidos por el usuario.
{: shortdesc}

El panel Actividad muestra información sobre todas las actividades de la aplicación, como por ejemplo el inicio, la detención y el despliegue, para las últimas 24 horas.

![Panel Actividad en el panel de control Supervisión de disponibilidad.](images/avmon_activity_pane.png)

Las actividades de {{site.data.keyword.Bluemix_notm}} son sucesos de aplicación que tienen lugar en {{site.data.keyword.Bluemix_notm}}, como por ejemplo detener, iniciar o volver a transferir aplicación. Las actividades de conducto son sucesos que se producen en el conducto DevOps, como compilaciones, despliegues y pruebas. La cabecera de tabla muestra distintos totales para actividades de {{site.data.keyword.Bluemix_notm}} y actividades de conducto (Pipeline). Puede filtrar por origen de actividad para visualizar actividades de {{site.data.keyword.Bluemix_notm}} o actividades de conducto (Pipeline) pulsando {{site.data.keyword.Bluemix_notm}} o iconos de conducto (Pipeline) en la cabecera del panel Actividad.

Para ver actividades de conducto (Pipeline) en el panel de control de {{site.data.keyword.prf_hubshort}}, debe habilitar en primer lugar {{site.data.keyword.contdelivery_short}} para su aplicación, y configurar una cadena de herramientas que contenga un conducto y el servicio de {{site.data.keyword.DRA_short}}. Pulse **Configuración de conducto** para crear una cadena de herramientas para la aplicación. Para obtener más información, consulte [Iniciación a la entrega continua](../ContinuousDelivery/index.html "(Se abre en un nuevo separador o ventana)"){:new_window} e [Iniciación a DevOps Insights](../DevOpsInsights/index.html#gettingstarted "(Se abre en un nuevo separador o ventana)").
{: tip}

Si ha configurado {{site.data.keyword.contdelivery_short}} y {{site.data.keyword.DRA_short}} para su aplicación, puede pulsar **Ver Insights** en la columna de sucesos para acceder a los paneles de control de {{site.data.keyword.DRA_short}} y ver más detalles sobre sus actividades de conducto.

Las actividades de {{site.data.keyword.Bluemix_notm}} y de conducto también se muestran en el **Canal de información de métricas** y en el gráfico del panel Tiempo de respuesta y Disponibilidad.
