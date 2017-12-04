---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Panel de control Desglose
{: avmon_view_breakdown}

El panel de control **Desglose** muestra información sobre estadísticas clave de las pruebas. El panel de control también contiene un resumen de la información sobre disponibilidad y tiempo de respuesta, tendencias históricas y datos de rendimiento de pruebas realizadas durante las últimas 24 horas.
{: shortdesc}

Para ver un desglose detallado de una prueba, pulse sobre la prueba en el panel Pruebas sintéticas. También puede abrir el panel de control Desglose pulsando **Desglose** en la tabla Alerta del panel Frecuencia de alerta.

El panel de control Desglose muestra cuatro paneles:

## Resumen de prueba
{: #avmon_bdown_summary}

![Panel Resumen de prueba.](images/avmon_bdown_summ.png)

El panel **Resumen de prueba** muestra la información de prueba siguiente de las últimas 24 horas:

-   **Estado actual** muestra el estado de prueba.
-   **Instancias de prueba** muestra el desglose de los porcentajes de las instancias de prueba críticas, de aviso y normales.
-   **Tiempo de respuesta medio** muestra el tiempo de respuesta medio de la prueba.
-   **Tendencias históricas** muestra las tendencias históricas del rendimiento de la prueba para los percentiles 50, 95 y 99 en segundos o milisegundos.

## Instancias de prueba
{: #avmon_bdown_instances}

![Desglose de la instancia de prueba de API Rest de la tabla Instancias de prueba.](images/avmon_bdown_apitest_instance.png)

En la tabla **Instancias de prueba** se muestra información detallada sobre cada instancia de prueba, incluidos el estado, el tiempo de respuesta, la ubicación donde se ha ejecutado la prueba, el número de errores y la indicación de fecha y hora en la que se ha ejecutado la prueba. Para obtener más detalles de una instancia de prueba, pulse **Expandir**. Se lista la información de respuesta detallada para cada paso de la instancia de prueba. Puede ordenar las columnas e identificar con rapidez el paso concreto en el que se ha producido el error o la ralentización. Visualizar los errores, la secuencia de prueba y el tiempo de respuesta ayuda a identificar problemas.

La información que se muestra dependerá del tipo de prueba sintética que se esté supervisando:

### API
Si pulsa **Expandir** para una instancia de prueba de API, se muestra un resumen de nivel superior con los siguientes detalles:

-   **Respuesta** muestra el tiempo total de respuesta para la instancia de prueba, incluido el tiempo de redirección.
-   **Redirección** muestra el tiempo total de redirección para la instancia de prueba.
-   **Tamaño** muestra el tamaño del objeto.
-   **Velocidad de descarga** muestra la velocidad a la que se descarga cada objeto.
-   **Errores** muestra el número de errores que se han producido durante la instancia de prueba. Para ver los detalles de un error, pulse el icono **Información**.

Una tabla muestra cada paso de la llamada de API, junto con el nombre del paso, la secuencia de pasos y el tiempo de respuesta de cada paso. Se muestran los siguientes nombres de pasos:

-   **Búsqueda de nombre** representa el tiempo que la instancia de prueba ha empleado en resolver el nombre del objeto.
-   **Conexión** representa el tiempo que la instancia de prueba ha tardado desde el inicio del paso hasta que se ha establecido una conexión con el proxy o host remoto.
-   **Conexión de app** representa el tiempo que la instancia de prueba ha tardado desde el inicio del paso hasta que se ha establecido una conexión SSL con el host remoto.
-   **Previo a transferencia** representa el tiempo que la instancia de prueba ha tardado desde el inicio del paso hasta justo antes de que comenzara el mandato de transferencia de archivos.
-   **Inicio de transferencia** representa el tiempo que la instancia de prueba ha tardado desde el inicio del paso hasta el primer byte recibido.
-   **Transferencia** representa el tiempo que la instancia de prueba ha empleado en transferir el archivo.

### Página web
![Desglose de instancia de prueba de página web de la tabla Instancias de prueba.](images/avmon_bdown_webpage_instance.png)

Si pulsa **Expandir** para una instancia de prueba de página web, se muestra un resumen de nivel superior con los siguientes detalles:

-   **Respuesta** muestra el tiempo de respuesta de la instancia de prueba.
-   **Solicitudes totales (externas)** muestra el número total de solicitudes para la instancia de prueba. El número de solicitudes externas está entre paréntesis.
-   **Tamaño de página** muestra el tamaño de la página web.
-   **Errores** muestra el número de errores que se han producido durante la instancia de prueba. Para ver los detalles de un error, pulse el icono Información.

También se muestra una tabla con los siguientes detalles de cada solicitud realizada por la prueba:

-   **Tipo** muestra el tipo de solicitud, como por ejemplo HTML, CSS, JavaScript o imagen. Las solicitudes externas e internas se indican con iconos.
-   **Vía de acceso al archivo** describe la ubicación del objeto solicitado.
-   **Tamaño** muestra el tamaño del objeto solicitado.
-   **Secuencia** muestra la secuencia de solicitudes realizadas por la prueba.
-   **Tiempo** muestra el tiempo que tarda cada solicitud.
-   **Código de estado** muestra el código de estado de la solicitud HTTP.
-   **Estado** describe el resultado de la solicitud, como por ejemplo Completado, Desconocido o Erróneo.

### Script
![Desglose de instancia de prueba de script de la tabla Instancias de prueba.](images/avmon_bdown_script_instance.png)

Si pulsa **Expandir** para una instancia de prueba de script, se muestra el tiempo de respuesta, el número de pasos del script y el número de errores. Para ver los detalles de un error, pulse el icono **Información**.

En la tabla se muestran los siguientes detalles de cada paso del script:

-   **Nombre** muestra cada mandato de Selenium que ha llamado la instancia de prueba, por ejemplo Open, ClickAt o VerifyBodyText.
-   **Secuencia** muestra la secuencia de pasos del script desde el principio hasta el final de la instancia de prueba.
-   **Tiempo** muestra el tiempo que tarda cada paso del script.
-   **Errores** muestra el número de errores que se han producido durante cada paso del script.
-   **Estado** describe el resultado del paso de script, como por ejemplo Completado, Desconocido o Erróneo.

Puede profundizar y ver detalles sobre las solicitudes que genera cada paso del script.

![Desglose de los detalles de un paso individual de la instancia de prueba de script de la tabla Instancias de prueba.](images/avmon_bdown_script_subtrans.png)

Pulse **Expandir** para ver una tabla que contiene los siguientes detalles:

-   **Tipo** muestra el tipo de solicitud, como por ejemplo HTML, CSS, JavaScript o imagen. Las solicitudes externas e internas se indican con iconos.
-   **Vía de acceso al archivo** describe la ubicación del objeto solicitado.
-   **Tamaño** muestra el tamaño del objeto solicitado.
-   **Secuencia** muestra la secuencia de solicitudes realizadas por la prueba.
-   **Tiempo** muestra el tiempo que tarda cada solicitud.
-   **Código de estado** muestra el código de estado de la solicitud HTTP.
-   **Estado** describe el resultado de la solicitud, como por ejemplo Completado, Desconocido o Erróneo.

{{site.data.keyword.prf_hubshort}} puede crear una captura de pantalla automáticamente si no se puede cargar la página web o si falla un paso del script. Por ejemplo, si uno de los pasos del script abre una página web pero esta no se carga, {{site.data.keyword.prf_hubshort}} creará una captura de pantalla automáticamente. Para ver una captura de pantalla de la página web o script, pulse el icono **Error de captura de pantalla** ![Icono Error de captura de pantalla](images/scrnsht_err_icn_white.jpg). Esta característica solo está disponible para la supervisión de páginas web y de pruebas realizadas mediante script. No funciona con la supervisión de API REST.

También puede descargar un registro del tráfico de red para una instancia de prueba determinada como archivo .har pulsando el icono **Descargar** ![Icono Descargar.](images/download_icn_white_smll.jpg). Esta característica está disponible para la supervisión de páginas web y de pruebas realizadas mediante script.

## Tiempo de respuesta y disponibilidad
{: #avmon_bdown_rt_avail}
El panel Tiempo de respuesta y disponibilidad muestra un gráfico de tiempos de respuesta y disponibilidad medidos para las instancias de la prueba durante un periodo definido. Para obtener más información, consulte [Tiempo de respuesta y Disponibilidad](avmon_resptime_avail.html "Utilice el panel Tiempo de respuesta y Disponibilidad para ayudarle a visualizar el tiempo de respuesta, las tendencias de disponibilidad, las alertas y las actividades a lo largo del tiempo. La correlación de métricas, alertas y actividades le ayuda a aislar fácilmente un cambio de aplicación o despliegue de código específico cuando vea un tiempo de respuesta afectado.").

## Actividad
{: #avmon_bdown_activity}
El panel Actividad muestra una tabla de todas las actividades durante las últimas 24 horas. Para obtener más información, consulte [Actividad](avmon_activities.html "Puede ver información para las actividades en el panel Actividad. Las Actividades son acciones que se producen fuera de los sucesos definidos por el usuario.").
