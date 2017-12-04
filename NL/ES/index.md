---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Iniciación a la supervisión de disponibilidad
{: #avmon_gettingstarted}

Utilice {{site.data.keyword.prf_hublong}} para ejecutar pruebas de rendimiento simuladas desde ubicaciones de todo el mundo en todo momento. Detecte, aísle y diagnostique problemas de rendimiento de forma proactiva antes de que repercutan en los usuarios. Asegúrese de que las aplicaciones estén disponibles y cumplan los objetivos de tiempo de respuesta cuando implante actualizaciones continuas. Configure recopiladores de datos para que sus aplicaciones recopilen datos de transacciones de usuarios. Utilice estos datos de {{site.data.keyword.prf_hubshort}} para supervisar la capacidad de respuesta y el rendimiento de la aplicación.
{: shortdesc}

## Acerca de esta tarea
{: #avmon_start_about}

{{site.data.keyword.prf_hubshort}} está disponible como servicio en el dominio DevOps del catálogo de {{site.data.keyword.Bluemix_notm}}. También está disponible de forma predeterminada en el separador **Supervisión** del panel de control de la aplicación. Puede empezar a supervisar la disponibilidad y el rendimiento de su aplicación de forma inmediata. Cuando enlace {{site.data.keyword.prf_hubshort}} a su aplicación, se creará automáticamente una prueba sintética para supervisar el URL de la aplicación principal de forma predeterminada.

## Creación de una prueba de página web
{: #avmon_start_procedure}

Siga estos pasos para abrir {{site.data.keyword.prf_hubshort}} para la aplicación, para crear una prueba de página web para supervisar otro URL y para configurar alertas de notificación para sus pruebas.

1.  Si dispone de una aplicación de Cloud Foundry que desea supervisar, pulse el nombre de aplicación en la tabla **Todas las aplicaciones** del panel de control **Apps**. Si no tiene una aplicación todavía, créela y la tarjeta de la aplicación se abrirá automáticamente. Las aplicaciones de Cloud Foundry están enlazadas automáticamente con {{site.data.keyword.prf_hubshort}} al pulsar el separador Supervisión.
2.  Para abrir {{site.data.keyword.prf_hubshort}}, pulse el separador **Supervisión**. El separador **Supervisión** muestra tres indicadores que muestran la **Disponibilidad de prueba media** en las últimas 24 horas, el **Estado de prueba actual** y el **Uso** de la asignación del plan actual. Pulse **Añadir prueba nueva** para configurar una prueba de supervisión.

    ![Separador Supervisión de disponibilidad](images/avmon_tab.png)

    El URL de aplicación principal se supervisa de forma predeterminada. Los otros URL y servicios que supervise pueden ser internos o externos de Bluemix y no es necesario que estén relacionados con la aplicación de Cloud Foundry asociada.

3.  Pulse **Acción única** en la página Configuración de supervisión; a continuación, pulse **Página web** en la página Acción única.
4.  Escriba un nombre significativo para la prueba en el campo **Nombre**. Añada una descripción de la finalidad de la prueba en el campo **Descripción**.
5.  Especifique el **URL** de la aplicación web que desea probar.
6.  Configure los umbrales de alerta de aviso y crítica de la prueba en la sección Validación de respuesta. Edite el **Valor** y la **Unidad** de cada fila. Los tiempos de respuesta que superan los umbrales de aviso y críticos activan alertas.

    ![Sección Validación de respuesta con umbrales de aviso y crítico predeterminados.](images/avmon_webpage_resp_val.png)

7.  Utilice la **Lista negra** y la **Lista blanca** para especificar a qué URL y dominios se enviarán solicitudes y qué URL y dominios contribuyen a las métricas y al estado de las pruebas de aplicación. Añada URL y dominios que desee incluir o bloquear en la **Lista blanca** y en la **Lista negra**. Para obtener más información sobre el bloqueo y el filtrado, consulte [Bloqueo y filtrado con la lista blanca y la lista negra](avmon_whitelist_blacklist.html "Use la lista blanca y la lista negra para determinar a qué recursos se enviarán solicitudes y qué recursos contribuyen a las métricas y al estado de las pruebas de la aplicación. Las listas blancas y las listas negras sólo están disponibles para la página web y para las pruebas de comportamiento programado.").
8.  Pulse **Verificar** para crear la prueba de página web y para determinar si la solicitud de prueba es válida.

    {{site.data.keyword.prf_hubshort}} determina la validez de la prueba enviando una solicitud GET al URL de prueba. Durante la verificación de la prueba no se realiza ninguna validación de respuesta.

    La prueba validada se muestra en la tabla Elementos verificados. Para añadir más URL, repita los pasos 3 al 8.

9.  Para configurar los valores de prueba, pulse **Siguiente**.

    Se mostrará un resumen de la configuración de prueba. Por ejemplo, se muestra el siguiente mensaje para los valores predeterminados:

    `La prueba se realizará: cada 15 minutos desde 3 ubicaciones simultáneamente para determinar si la prueba supera el umbral especificado.`

    El uso estimado y las pruebas estimadas por mes se visualizan basándose en la configuración actual de la prueba.

10. En el panel Configuración, pulse **Editar** para visualizar los valores actuales para la prueba. Puede actualizar los siguientes valores:
    - **Intervalo** define con qué frecuencia se ejecuta la prueba.
    - **Frecuencia de las pruebas** determina si la prueba se ejecuta desde todas las ubicaciones simultáneamente o desde una ubicación diferente en cada intervalo. Seleccione **Simultáneo** para ejecutar la prueba simultáneamente desde todas las ubicaciones o bien **Escalonado** para ejecutar la prueba desde una ubicación distinta seleccionada en cada intervalo.
    - **Ubicaciones** determina las ubicaciones donde se ejecutará la prueba.

    Pulse **Guardar** para terminar de configurar la prueba.

11. Pulse **Finalizar**. El panel de control de {{site.data.keyword.prf_hubshort}} muestra un resumen de las pruebas totales, un mapa y una tabla que muestran la frecuencia y la ubicación de las alertas, todas las pruebas sintéticas asociadas con su aplicación, una tabla de sus actividades, y un gráfico de líneas que muestra el tiempo de respuesta y la disponibilidad de la aplicación y de otros sitios web. Puede crear más pruebas si es necesario.
12. Puede utilizar el servicio de {{site.data.keyword.alertnotificationfull}} para configurar la característica de supervisión para enviar notificaciones cuando se produzca un suceso. Para obtener más información, consulte [Habilitación de notificaciones](avmon_notifications.html "Configurar la característica de supervisión para enviar notificaciones cuando se produzca un suceso.").

## Resultados
{: #avmon_getstarted_results}

Los resultados de la prueba se muestran después del intervalo especificado en la prueba. El intervalo predeterminado es 15 minutos.

Ya está preparado para supervisar la disponibilidad de sus aplicaciones web. La información de disponibilidad y tiempo de respuesta de la aplicación, del sitio web o de la API REST se muestran en un gráfico de líneas junto con la información de las pruebas y actividades recientes en el panel **Tiempo de respuesta y disponibilidad**.

Hay dos guías disponibles para ayudarle a obtener más información de las características de {{site.data.keyword.prf_hubshort}}.

 - **Biblioteca de guías de aprendizaje en vídeo** - La Biblioteca de guías de aprendizaje en vídeo contiene vídeos sobre cómo crear aplicaciones Bluemix, crear pruebas de Supervisión de disponibilidad, crear scripts de prueba con Selenium IDE y enviar alertas a Slack.
 - **Bienvenido a la supervisión** - La guía Bienvenido a la supervisión destaca áreas del panel de control y explica cada característica de {{site.data.keyword.prf_hubshort}}.

Para abrir una guía, pulse el icono **Ayuda** ![icono Ayuda](images/help_icn_white_sml.jpg); a continuación, pulse la guía que desee ver.
