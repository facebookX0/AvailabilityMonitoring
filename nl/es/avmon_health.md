---

copyright:
  years: 2015, 2017
lastupdated: "2017-9-28"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Estado de la aplicación
{: #avmon_health}

El panel Estado de la aplicación proporciona una instantánea del rendimiento de la aplicación en función de la disponibilidad de la aplicación, la satisfacción de los usuarios con el rendimiento de la aplicación, y el rendimiento de la aplicación.
{: shortdesc}

Si {{site.data.keyword.prf_hubshort}} detecta que se ha configurado un recopilador de datos para su aplicación, el panel Estado de la aplicación estará disponible para su visualización.

**Restricción:** Inicialmente, un recopilador de datos está disponible sólo para aplicaciones Node.js. Para obtener más información sobre la configuración del recopilador de datos de Node.js, consulte [Documentación del recopilador de datos de Node.js](https://www.npmjs.com/package/ibmapm "(Se abre en un nuevo separador o ventana)"){: new_window}.

El panel muestra tres medidas; **Disponibilidad**, **Puntuación de satisfacción** y **Volumen de solicitudes**.
![Panel Estado de la aplicación que muestra el nivel de las aplicaciones de disponibilidad, satisfacción del usuario y rendimiento de transacción.](images/avmon_app_health_ui.jpg)
El cálculo de la métrica **Disponibilidad** se basa en datos de transacción de usuarios simulados desde las pruebas sintéticas. Por el contrario, las métricas **Puntuación de satisfacción** y **Volumen de solicitudes** dependen de datos de transacción de usuarios reales y simulados que proporcionan los recopiladores de datos.

Las etiquetas numéricas muestran el valor más reciente de cada métrica. Por ejemplo, el valor más reciente para **Disponibilidad** es ![El valor más reciente de la métrica Disponibilidad.](images/avmon_app_health_latest.jpg). Los gráficos de línea de serie de tiempo describen el rendimiento de la aplicación en cada métrica a lo largo del tiempo. Puede establecer el intervalo de tiempo de los gráficos de historial seleccionando las últimas **24 horas** o los últimos **7 días** en el desplegable Tiempo. A medida que pase el cursor por la línea del gráfico, se muestra el valor de cada punto de datos en una ayuda contextual, por ejemplo, ![Una ayuda contextual en el gráfico de líneas de historial.](images/avmon_app_health_hover.jpg). Al pulsar un punto de datos en el gráfico de líneas, la etiqueta numérica mostrará el valor para este punto de datos. Pulse cualquier área fuera de los gráficos de líneas para restablecer las etiquetas numéricas a sus valores más recientes. Pasar el cursor o pulsar un gráfico actualiza los otros dos gráficos del panel **Estado de la aplicación**.

Pulse ![Menú Ver contribuciones que puede expandir para ver las transacciones o las pruebas que contribuyen.](images/avmon_view_contrib.jpg) para ver las cinco transacciones o pruebas principales que han contribuido al estado actual de la aplicación.![Panel Estado de aplicación que muestra el nivel de disponibilidad, satisfacción de usuario y rendimiento de transacción de la aplicación.](images/avmon_app_health_expanded.jpg)

## Disponibilidad
{: #avmon_health_availability}
**Disponibilidad** muestra el grado en el que la aplicación está operativa. La disponibilidad se determina mediante el porcentaje de las instancias de prueba sintéticas que han pasado correctamente. Por ejemplo, si todas las pruebas sintéticas se han ejecutado correctamente durante el intervalo más reciente, el valor de Disponibilidad actual para la aplicación es 100%.

Puede configurar cómo calcula {{site.data.keyword.prf_hubshort}} la Disponibilidad desde el separador Supervisión seleccionando pruebas para su inclusión en el Cálculo de disponibilidad. Para obtener más información, consulte [Acceso a la Supervisión de disponibilidad](avmon_tab.html "Puede acceder al panel de control Supervisión de disponibilidad desde el separador **Supervisión**. El separador Supervisión para la aplicación de Cloud Foundry muestra información de resumen sobre la disponibilidad y el estado de las pruebas, y los detalles y el uso de la suscripción de servicio.").

{{site.data.keyword.prf_hubshort}} calcula el porcentaje de las instancias de prueba disponibles por hora. Pase el ratón sobre la línea en el gráfico para ver el valor de cada intervalo de hora durante las últimas 24 horas o los últimos 7 días.

Se muestran las cinco pruebas sintéticas principales que han contribuido al nivel de disponibilidad actual de su aplicación. La tabla muestra la siguiente información sobre cada una de las pruebas.

-   **Pruebas** muestra el nombre de prueba que ha asignado.
-   **Instancias** muestra el número de instancias de prueba que se han ejecutado para cada prueba.
-   **Tasa de errores** muestra el porcentaje de instancias de prueba que han fallado para cada prueba.


## Puntuación de satisfacción
{: #avmon_health_satscore}
**Puntuación de satisfacción** es un indicador de la satisfacción del usuario con la capacidad de respuesta de la aplicación. Puede establecer un valor de umbral de satisfacción (**T**) para la aplicación. Determine qué solicitudes del usuario de tiempo de respuesta deben cumplirse para que sus usuarios estén satisfechos.

Los tiempos de respuesta de la solicitud del usuario se convierten en un valor de índice entre 0,0 y 1,0, donde 1,0 es una puntuación perfecta con todos los usuarios satisfechos. Para calcular la puntuación de satisfacción, los ejemplos de usuario se categorizan como:

-   Satisfecho - las solicitudes de usuarios con un tiempo de respuesta inferior o igual al umbral de satisfacción se consideran Satisfechas.
-   Tolerado - las solicitudes de usuarios que están entre Satisfecho y Frustrado se consideran Toleradas.
-   Frustrado - las solicitudes de usuarios con un tiempo de respuesta mayor de 4**T**, o que tienen como resultado un error, se consideran Frustradas.

La puntuación de satisfacción se calculará entonces como la proporción de [solicitudes de usuarios satisfechos + (solicitudes de usuarios tolerantes /2)] / [número total de solicitudes de usuarios].

{{site.data.keyword.prf_hubshort}} calcula la puntuación de satisfacción en función de los datos de transacciones para cada intervalo de horas. Pase el cursor sobre la línea del gráfico para ver la puntuación para cada intervalo de hora durante las últimas 24 horas o los últimos 7 días.

La tabla muestra la siguiente información sobre las cinco transacciones principales que han contribuido a la puntuación de satisfacción actual de su aplicación:

-   **Transacciones** muestra el nombre de la transacción de usuario.
-   **Puntuación** muestra la puntuación de satisfacción que se calcula para la transacción individual.
-   **Insatisfacción** muestra la contribución de la transacción a los niveles de insatisfacción de los usuarios actuales. Si la satisfacción del usuario no es óptima, utilice el porcentaje de **Insatisfacción** para medir cuánto han afectado los niveles de insatisfacción a cada transacción.


## Volumen de solicitudes
{: #avmon_health_reqvol}
La métrica Volumen de solicitudes es el volumen actual de las instancias de transacción de usuario. La métrica indica el rendimiento real de la aplicación.

El tiempo de respuesta medio de la transacción para su aplicación también se muestra debajo de la etiqueta, por ejemplo, ![El tiempo de respuesta medio del valor más reciente.](images/avmon_app_health_response.jpg) y los valores medios de tiempo de respuesta se trazarán en el gráfico. Puede buscar correlaciones entre aumentos en el rendimiento y tiempos de respuesta medios aumentados.

Los datos de volumen de solicitud sin formato se agregarán y se visualizarán en el gráfico cada hora. Pase el cursor por encima de la línea del gráfico para ver el rendimiento de cada aplicación para cada intervalo de hora durante las últimas 24 horas o los últimos 7 días.

La tabla muestra la información siguiente sobre las cinco transacciones principales que más contribuyen al volumen de solicitud actual. Si la aplicación está experimentando volúmenes altos de tráfico de usuarios, utilice el **Porcentaje de total** para medir cuánto está contribuyendo cada transacción al volumen de tráfico general.

-   **Transacción** muestra el nombre de la transacción de usuario.
-   **Volumen** muestra el número de instancias de transacciones para cada transacción.
-   **Porcentaje de total** muestra el porcentaje del volumen total de solicitudes.
