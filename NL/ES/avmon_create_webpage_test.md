---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Creación de una prueba de página web
{: #avmon_webpage_test}

Cree una prueba de página web para probar la disponibilidad de la aplicación web y supervisar cuánto tiempo tarda en abrirse esta página.
{: shortdesc}

## Acerca de esta tarea
{: #avmon_webpage_about}

Las pruebas de página web notifican el
tiempo de respuesta necesario para
cargar el URL de la aplicación web. Cree una prueba de página web para probar la disponibilidad y el tiempo de respuesta de la aplicación web.

## Creación y configuración de la prueba de página web
{: #avmon_create_web_test}

Para crear una prueba de página web, siga los pasos siguientes.

1.  Si está viendo el separador Supervisión, pulse **Añadir prueba nueva**.

    ![El separador Supervisión para su aplicación Cloud Foundry.](images/avmon_tab.png)

    Si está viendo el panel de control de {{site.data.keyword.prf_hubshort}}, pulse **Añadir nueva prueba** en el panel Pruebas sintéticas.

    ![El botón Añadir nueva prueba en el panel Pruebas sintéticas.](images/syn_tests_pane.jpg)

2.  Pulse **Acción única** en la página Configuración de supervisión; a continuación, pulse **Página web** en la página Acción única.
3.  Escriba un nombre significativo para la prueba en el campo **Nombre**. Añada una descripción de la finalidad de la prueba en el campo **Descripción**.
4.  Especifique el **URL** de la aplicación web que desea probar.
5.  Configure los umbrales de alerta de aviso y crítica de la prueba en la sección Validación de respuesta. Edite el **Valor** y la **Unidad** de cada fila. Los tiempos de respuesta que superan los umbrales de aviso y críticos activan alertas.

    ![Sección Validación de respuesta con umbrales de aviso y crítico predeterminados.](images/avmon_webpage_resp_val.png)

6.  Utilice la **Lista negra** y la **Lista blanca** para especificar a qué URL y dominios se enviarán solicitudes y qué URL y dominios contribuyen a las métricas y al estado de las pruebas de aplicación. Añada URL y dominios que desee incluir o bloquear en la **Lista blanca** y en la **Lista negra**. Para obtener más información sobre el bloqueo y el filtrado, consulte [Bloqueo y filtrado con la lista blanca y la lista negra](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "Use la lista blanca y la lista negra para determinar a qué recursos se enviarán solicitudes y qué recursos contribuyen a las métricas y al estado de las pruebas de la aplicación. Las listas blancas y las listas negras sólo están disponibles para la página web y para las pruebas de comportamiento programado.").
7.  Pulse **Verificar** para crear la prueba de página web y para determinar si la solicitud de prueba es válida.

    {{site.data.keyword.prf_hubshort}} determina la validez de la prueba enviando una solicitud GET al URL de prueba. Durante la verificación de la prueba no se realiza ninguna validación de respuesta.

    La prueba validada se muestra en la tabla Elementos verificados. Puede añadir más URL repitiendo los pasos 3 al 7.

8.  Para configurar los valores de prueba, pulse **Siguiente**. Se mostrará un resumen de la configuración de prueba. Por ejemplo, se muestra el siguiente mensaje para los valores predeterminados:

    ``La prueba se realizará: cada 15 minutos desde 3 ubicaciones simultáneamente para determinar si la prueba supera el umbral especificado``.

    El uso estimado y el número de pruebas estimadas por mes se muestran en función de la configuración actual de la prueba.

9.  En el panel Configuración, pulse **Editar** para visualizar los valores actuales para la prueba. Puede actualizar los siguientes valores:
    - **Intervalo** define con qué frecuencia se ejecuta la prueba.
    - **Frecuencia de las pruebas** determina si la prueba se ejecuta desde todas las ubicaciones simultáneamente o desde una ubicación diferente en cada intervalo. Seleccione **Simultáneo** para ejecutar la prueba simultáneamente desde todas las ubicaciones o bien **Escalonado** para ejecutar la prueba desde una ubicación distinta seleccionada en cada intervalo.
    - **Ubicaciones** determina las ubicaciones donde se ejecutará la prueba.

    Pulse **Guardar** para terminar de configurar la prueba.

10. Pulse **Finalizar**. El panel de control {{site.data.keyword.prf_hubshort}} muestra un resumen de todas las pruebas, un mapa y una tabla que muestran la gravedad y la ubicación de las alertas, todas las pruebas sintéticas asociadas con su aplicación, una tabla de sus actividades, y un gráfico de líneas que muestra el tiempo de respuesta y la disponibilidad de la aplicación y otros sitios web.
