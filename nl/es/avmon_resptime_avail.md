---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Tiempo de respuesta y disponibilidad
{: #avmon_resptime_avail}

Utilice el panel Tiempo de respuesta y Disponibilidad para visualizar tiempos de respuesta, tendencias de disponibilidad, alertas y actividades a lo largo del tiempo. La correlación de métricas, alertas y actividades le ayuda a aislar fácilmente un cambio de aplicación o un despliegue de código específico cuando vea un tiempo de respuesta afectado.
{: shortdesc}

## Tiempo de respuesta
{: #avmon_resptime_graph}

La información de tiempo de respuesta se muestra en un gráfico de líneas. Para verlo, pulse el separador **Tiempo de respuesta**.

![Gráfico de tiempos de respuesta de una prueba correspondiente a las últimas 24 horas.](images/avmon_rt_gr.jpg)

Los tiempos de respuesta que se miden mediante {{site.data.keyword.prf_hubshort}} son ligeramente superiores que los tiempos de respuesta que experimentan los usuarios. {{site.data.keyword.prf_hubshort}} simula el comportamiento de usuario real, que añade sobrecarga a la medición del tiempo de respuesta. La sobrecarga se debe a los siguientes factores:
  - {{site.data.keyword.prf_hubshort}} crea una nueva instancia de Firefox para cada prueba para impedir que las reproducciones anteriores afecten a la prueba actual. Los usuarios finales reales podrían experimentar tiempos de respuesta más rápidos debido al almacenamiento en caché del navegador.
  - {{site.data.keyword.prf_hubshort}} instala el plug-in de controlador web de Firefox antes de cada prueba.
{: tip}

Los tiempos de respuesta individuales de las pruebas se representan mediante un icono **Punto de respuesta** ![icono Punto de respuesta](images/crcl_icn_white.jpg) en el gráfico de líneas. Los diferentes colores indican distintas ubicaciones geográficas donde se ejecuta la aplicación. El eje y del gráfico utiliza iconos de alerta para identificar los intervalos de umbral aviso y crítico. El icono de
**aviso** amarillo ![Icono de aviso amarillo](images/alrt_icn_white_smll.jpg) representa el rango de umbral de aviso, y el icono **crítico** rojo ![Icono crítico rojo](images/wrng_icn_white_smll.jpg) representa el rango de umbral crítico. Pulse el icono de **aviso** amarillo ![Icono de aviso amarillo](images/alrt_icn_white_smll.jpg) o el icono **crítico** rojo ![Icono crítico rojo](images/wrng_icn_white_smll.jpg) para identificar fácilmente instancias de prueba que aparecen en los rangos de umbrales de aviso y críticos. Para ver los detalles para una instancia de prueba específica, pulse el icono **Punto de respuesta** ![icono Punto de respuesta](images/crcl_icn_white.jpg) en el gráfico.

### Filtros

Seleccione una prueba en el menú desplegable **Prueba**. Puede filtrar datos correspondientes a 3 horas, 24 horas, 7 días, 30 días y 12 meses. La posibilidad de ver datos correspondientes a 12 meses solo está disponible para los usuarios con suscripciones de pago a {{site.data.keyword.prf_hubshort}}. Al filtrar por un intervalo de tiempo mayor que 24 horas, los valores mostrados en el gráfico son promedios. Para ver información más específica, pulse el gráfico para ver detalles de alertas y avisos individuales. También puede utilizar el control deslizante para ampliar o reducir el intervalo de tiempo.

Con el gráfico Tiempo de respuesta, puede resaltar y ocultar los datos de determinadas ubicaciones PoP. Para resaltar los datos de tiempo de respuesta de una ubicación determinada, pase el puntero del ratón sobre el nombre de ubicación PoP; a continuación, pulse el icono **Resaltar ubicación** ![icono Resaltar ubicación](images/avmon_location_highlight.jpg). Para ocultar los datos de tiempo de respuesta de una ubicación, pase el puntero del ratón sobre el nombre de ubicación PoP; a continuación, pulse el icono **Ocultar ubicación** ![icono Ocultar ubicación](images/avmon_location_remove.jpg). Para restaurar los datos de ubicación PoP en el gráfico, pulse **Añadir más ubicaciones** ![icono Añadir más ubicaciones](images/icn_plus_20x20.jpg) o el separador **Selección de métrica**; a continuación, pulse la ubicación PoP que ha eliminado anteriormente.

### Alertas y actividades

Puede identificar fácilmente alertas de aviso y críticas en la fila Alertas. Mueva el puntero del ratón sobre un **icono de alerta** ![Icono de alerta crítica](images/avmon_crit_alert.png)![Icono de alerta de aviso](images/avmon_warn_alert.png) para identificar la gravedad y el indicador de fecha y hora de la alerta. Pulse un **icono de alerta** para ver detalles de dicha alerta en el campo **Canal de información de métricas**.

También puede ver actividades en el mismo gráfico. Las _actividades_ son acciones que se producen y que no son sucesos definidos por el usuario. Las actividades de {{site.data.keyword.Bluemix_notm}} son sucesos de aplicación que tienen lugar en {{site.data.keyword.Bluemix_notm}}, como por ejemplo detener, iniciar o volver a transferir aplicación. Las actividades de conducto son sucesos que se producen en la cadena de herramientas de {{site.data.keyword.contdelivery_short}}, como compilaciones, despliegues y pruebas. Pulse una actividad para ver información sobre dicha actividad en el **Canal de información de métricas**. Puede ver información sobre dichas actividades en el panel Actividad.

Para ver actividades de conducto (Pipeline) en el panel de control de {{site.data.keyword.prf_hubshort}}, debe habilitar en primer lugar {{site.data.keyword.contdelivery_short}} para su aplicación, y configurar una cadena de herramientas que contenga un conducto y el servicio de {{site.data.keyword.DRA_short}}. Pulse **Configuración de conducto** en el panel Resumen o en el panel Actividad para crear una cadena de herramientas para la aplicación. Para obtener más información, consulte [Iniciación a la entrega continua](../ContinuousDelivery/index.html "(Se abre en un nuevo separador o ventana)") e [Iniciación a DevOps Insights](../DevOpsInsights/index.html#gettingstarted "(Se abre en un nuevo separador o ventana)"){: new_window}.
{: tip}

Si hay más de un icono de actividad o de alerta juntos en las filas Alertas y Actividad, un **icono de número** mostrará el número de alertas o actividades en ese momento. Pase el puntero sobre un **icono de número** para mostrar las alertas o las actividades individuales, y pulse una alerta o actividad para ver información en el **Canal de información de métricas**.

### Selección de métricas y Canal de información de métricas

Para filtrar métricas por región geográfica,
pulse **Selección de métrica**. Pulse una ubicación para añadir o eliminar del gráfico métricas que se midan en la ubicación. Pulse **Añadir más ubicaciones** para abrir la página Modalidad de edición de prueba y añadir una ubicación de PoP a la prueba
seleccionada.

![Separador de selección de métricas que muestra filtros de ubicaciones PoP.](images/avmon_metric_sel.jpg)

Para ver una lista de detalles de métricas, pulse **Canal de información de métricas**. El panel Canal de información de métricas muestra una lista de las instancias en las que se ha realizado una métrica.

![Separador de canal de información de métricas que muestra detalles de una alerta de aviso.](images/avmon_warn_met_feed.png)

Pulse un **icono de alerta**, **icono de actividad** o **punto de respuesta** ![icono Punto de respuesta](images/crcl_icn_white.jpg) en el gráfico para añadir los detalles de dicha métrica al Canal de información de métricas.

![Detalles de una instancia de prueba disponible en el canal de información de métricas.](images/avmon_avail_metfeed.png)

Si filtra el gráfico Tiempo de respuesta por un intervalo de tiempo mayor que 24 y pulsa un **punto de respuesta**, puede ver los detalles agregados de ese día en el Canal de información de métricas.

![Canal de información de métricas que muestra los detalles agregados de todas las instancias de la prueba durante un día.](images/avmon_avail_day_met_feed.png)

Pulse **Zoom** para ver todos los tiempos de respuesta, actividades y alertas que se han generado durante ese día en el gráfico Tiempo de respuesta.

Para ver información detallada sobre un tiempo de respuesta de alerta o de prueba, pulse **Desglose** en el Canal de información de métricas. Pulse **Alerta más cercana** para ver la alerta más cercana a esta instancia de prueba en el Canal de información de métricas, en el caso de que se haya producido una alerta. Para ver información detallada sobre una actividad de interconexión en el servicio de {{site.data.keyword.DRA_short}}, pulse **Ver Insights** en el Canal de información de métricas.

## Disponibilidad
{: #avmon_avail_graph}

Para ver la información de disponibilidad de las aplicaciones, pulse Disponibilidad. El gráfico Disponibilidad muestra la disponibilidad diaria de cada punto de presencia (PoP) de cada prueba seleccionada.

![Gráfico de disponibilidad que muestra la disponibilidad diaria de una prueba por ubicación durante los 7 días anteriores.](images/avmon_avail_graph.png)

Con el gráfico Disponibilidad, puede resaltar y ocultar los datos de determinadas ubicaciones PoP. Para resaltar los datos de disponibilidad de una ubicación determinada, pase el puntero del ratón sobre el **nombre de ubicación PoP**; a continuación, pulse el icono **Resaltar ubicación** ![icono Resaltar ubicación](images/avmon_location_highlight.jpg). Para ocultar datos de disponibilidad para una ubicación, pase el puntero del ratón sobre el **nombre de ubicación PoP**; a continuación, pulse el icono **Ocultar ubicación** ![icono Ocultar ubicación](images/avmon_location_remove.jpg). Para restaurar los datos de ubicación PoP en el gráfico, pulse el separador **Selección de métrica**; a continuación, pulse la ubicación PoP que anteriormente ha eliminado.

Mueva el puntero del ratón sobre un punto del gráfico para ver la tasa de errores y el número de instancias de prueba correspondientes a un determinado día y ubicación. Pulse un punto del gráfico para ver esta información en el Canal de información de métricas.

![Disponibilidad de prueba en el PoP Dallas que se muestra en el Canal de información de métricas.](images/avmon_avail_metric.png)

Pulse **Zoom** para filtrar el gráfico Disponibilidad y el gráfico Tiempo de respuesta para visualizar información para el día seleccionado.
