---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Frecuencia de alerta
{: #avmon_alert_freq}

El panel Frecuencia de alerta contiene un mapa que muestra las alertas más recientes. Las alertas están agrupadas por ubicación y se muestran en la tabla Alertas.
{: shortdesc}

## Mapa de frecuencia de alerta
{: #avmon_alertmap}

El mapa Frecuencia de alerta muestra información resumida sobre todos los puntos de presencia
(PoPs) de sus pruebas.

Utilice la función de aumento (zoom) para aumentar cualquier área del mapa o restaurarlo a su tamaño original. Mueva el puntero del ratón sobre cada ubicación para ver su nombre y el número de alertas de aviso y críticas en dicha ubicación. Si desea filtrar las alertas que se muestran en el mapa, seleccione **Todas**, **Abiertas** o **Cerradas** en la lista desplegable **Alertas**.

![Mapa de frecuencia de alerta que muestra pruebas en cuatro puntos de presencia.](images/alert_freq_map2.png)

### Ubicación del host
El icono **Ubicación del host** ![Icono de ubicación del host.](images/icn_host_crit_whtbackground30.jpg) representa la ubicación del servidor en el que se ejecuta la aplicación que está supervisando. El color del icono **Ubicación del host** representa la gravedad de la alerta más reciente en esa ubicación: Normal ![Icono de ubicación del host con borde verde que indica que no hay alertas en esa ubicación.](images/icn_host_normal_whtbckgrnd_30x38.jpg), Aviso ![Icono de ubicación del host con borde amarillo que indica una alerta en esa ubicación.](images/icn_host_warning_whtbackground30.jpg), o Crítico ![Icono de ubicación del host con borde rojo que indica una alerta en esa ubicación.](images/icn_host_crit_whtbackground30.jpg). Un icono **Ubicación del host** animado indica que esta ubicación tiene la mayoría de las alertas con el nivel más alto de gravedad de todas las ubicaciones para sus instancias de prueba.

### Ubicaciones PoP
Los iconos de **Ubicación PoP** ![Icono de ubicación PoP.](images/icn_pop_normal_whtbckgrnd30x30.jpg) indican las ubicaciones PoP para las pruebas. El color de cada icono **Ubicación PoP** representa la gravedad de la mayoría de las alertas recientes en cada ubicación: Normal ![Icono de ubicación PoP con borde verde que indica que no hay alertas en esa ubicación.](images/icn_pop_normal_whtbckgrnd30x30.jpg), Aviso ![Icono de ubicación PoP con borde amarillo que indica una alerta en esa ubicación.](images/icn_pop_warning_whtbckgrnd30x30.jpg), o Crítico ![Icono de ubicación PoP con borde rojo que indica una alerta en esa ubicación.](images/icn_pop_crit_whtbckgrnd30x30.jpg). Un icono **Ubicación PoP** en movimiento indica la ubicación con mayor número de alertas y el nivel más alto de gravedad entre todas las ubicaciones de las instancias de la prueba.

Añada ubicaciones PoP a la prueba seleccionada pasando el cursor por encima de un icono de **Ubicación PoP inactiva** ![Ubicación PoP inactiva](images/icn_avbl_pop.jpg) y pulsando **Probar aquí**. Se muestra la página Modalidad de edición de prueba para la prueba seleccionada. Puede seleccionar una prueba en el menú desplegable **Prueba** del panel **Tiempo de respuesta** y **Disponibilidad**.

<!--
Private PoP locations are represented by **Private PoP location** icons ![Private PoP location icon that indicates 2 alerts with one or more critical alerts at that location.](images/avmon_private_pop.png).
-->
### Número de alertas
El icono **Ubicación del host** y los iconos de **Ubicación PoP** muestran el número de alertas abiertas, cerradas o todas las alertas generadas en cada ubicación. Los iconos Crítico, Aviso y Normal ![Iconos Crítico, Aviso y Normal.](images/fltr_alrts_tbl.jpg) muestran el número de alertas de cada gravedad para sus ubicaciones.

### Pruebas erróneas
Las ubicaciones donde se producen instancias de prueba erróneas se indican mediante un icono **Ubicación del host** o un icono **Ubicación PoP** con un borde roto ![Icono de ubicación PoP con borde rojo que indica 10 alertas y una o varias pruebas fallidas en esa ubicación.](images/avmon_pop_fail_32x33.png).

## Tabla de alertas
{: #avmon_alertstable}

Las alertas correspondientes a todas las ubicaciones se muestran en una tabla.

![Tabla de alertas que muestra alertas correspondientes a todas las ubicaciones PoP.](images/alert_table.jpg)

La tabla muestra la siguiente información sobre las alertas:

-   **Gravedad** describe la alerta como crítica o de aviso.
-   **Indicación de fecha y hora** muestra el momento en que se ha creado la alerta.
-   **Descripción** resume el rendimiento de la instancia de prueba.
-   **Desencadenada por** muestra el nombre de la prueba que ha desencadenado la alerta.
-   **Ubicación** indica dónde se ha producido el problema.
-   **Estado** muestra si la alerta está abierta o cerrada.

### Visualización de detalles de alerta
Cada alerta de la tabla contiene un enlace con el panel de control **Desglose**. Utilice el panel de control Desglose para que le ayude a solucionar el problema.

### Filtrado de alertas
Para filtrar alertas para una ubicación concreta, pulse un icono **Ubicación de host** o **Ubicación PoP** en el mapa. Para mostrar alertas para todas las ubicaciones, pulse en cualquier punto del mapa que no sea un icono **Ubicación de host** ni un icono **Ubicación PoP**.

Para filtrar las alertas de la tabla por gravedad, pulse el icono **Crítico**, **Aviso** o **Normal** ![Iconos Crítico, Aviso y Normal.](images/fltr_alrts_tbl.jpg). Para eliminar el filtro e incluir en la tabla alertas de cualquier gravedad, vuelva a pulsar el icono seleccionado.

### Cambiar umbrales de alerta
Las alertas se activan por los umbrales que especifica al crear una prueba. En la mayoría de los casos, se generan debido a errores de disponibilidad o tiempos de respuesta lentos. Para cambiar los valores de umbral, pulse el icono **Acciones** ![Icono Acciones.](images/actions_icn_white_smll.jpg) en la prueba que ha generado la alerta en el panel Pruebas sintéticas y pulse **Editar**.
