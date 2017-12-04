---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Creación de una prueba de script a partir de un script cargado
{: #avmon_upload_script_test}

Cargue un script de Selenium para crear una prueba de script que pruebe la disponibilidad y el rendimiento de la aplicación web en respuesta al
comportamiento simulado de los usuarios.
{: shortdesc}

## Antes de empezar
{: #avmon_script_prereq}

Las pruebas de script requieren que los scripts Selenium funcionen. Para crear una prueba de script, primero debe crear
un script Selenium. Para obtener más información sobre la creación de scripts de Selenium, consulte [Grabación de scripts sintéticos](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(Se abre en un nuevo separador o ventana)"){: new_window}.

## Acerca de esta tarea
{: #avmon_script_about}

Cree una prueba de script para supervisar un script Selenium que simula las interacciones de los usuarios con la aplicación web. Si crea un script Selenium que imita a un usuario que se registra en la aplicación, puede ejecutar a continuación una prueba de script periódicamente para probar el rendimiento de la aplicación en respuesta a las acciones de usuario simulado.

## Creación de una prueba con un script cargado
{: #avmon_script_create_test}

Para crear una prueba de script, siga los pasos siguientes.

1.  Si está viendo el separador Supervisión, pulse **Añadir prueba nueva**.

    ![El separador Supervisión para su aplicación Cloud Foundry.](images/avmon_tab.png)

    Si está viendo el panel de control de {{site.data.keyword.prf_hubshort}}, pulse **Añadir nueva prueba** en el panel Pruebas sintéticas.

    ![El botón Añadir nueva prueba en el panel Pruebas sintéticas.](images/syn_tests_pane.jpg)

2.  Pulse **Comportamiento programado** en la página Configuración de supervisión. Se visualizará la página Configuración de comportamiento programado. Pulse **Cargar archivo**.

    Si vuelve a editar este script más adelante, puede descargar el archivo de script cargado. Pulse el icono **Descargar** ![icono Descargar](images/download_icn_white_smll.jpg) para descargar el script.

3.  Escriba un nombre significativo para la prueba en el campo **Nombre**. Añada una descripción de la finalidad de la prueba en el campo **Descripción**.
4.  Pulse **Examinar** para buscar y cargar un archivo script.
5.  Utilice la **Lista negra** y la **Lista blanca** para especificar a qué URL y dominios se enviarán solicitudes y qué URL y dominios contribuyen a las métricas y al estado de las pruebas de aplicación. Añada URL y dominios que desee incluir o bloquear en la **Lista blanca** y en la **Lista negra**. Para obtener más información sobre el bloqueo y el filtrado, consulte [Bloqueo y filtrado con la lista blanca y la lista negra](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "Use la lista blanca y la lista negra para determinar a qué recursos se enviarán solicitudes y qué recursos contribuyen a las métricas y al estado de las pruebas de la aplicación. Las listas blancas y las listas negras sólo están disponibles para la página web y para las pruebas de comportamiento programado.").
6.  Para configurar los valores de prueba, pulse **Siguiente**. Se mostrará un resumen de la configuración de prueba. Por ejemplo, se muestra el siguiente mensaje para los valores predeterminados:

    ``La prueba se realizará: cada 15 minutos desde 3 ubicaciones simultáneamente para determinar si la prueba supera los 5 segundos``.

    El uso estimado y el número de pruebas estimadas por mes se muestran en función de la configuración actual de la prueba.

7.  En el panel Configuración, pulse **Editar** para visualizar los valores actuales para la prueba. Puede actualizar los siguientes valores:
    - **Intervalo** define con qué frecuencia se ejecuta la prueba.
    - **Frecuencia de las pruebas** determina si la prueba se ejecuta desde todas las ubicaciones simultáneamente o desde una ubicación diferente en cada intervalo. Seleccione **Simultáneo** para ejecutar la prueba simultáneamente desde todas las ubicaciones o bien **Escalonado** para ejecutar la prueba desde una ubicación distinta seleccionada en cada intervalo.
    - **Umbral crítico** define el tiempo de respuesta para alertas críticas para la prueba.
    - **Umbral de aviso** define el tiempo de respuesta para las alertas de aviso para la prueba.
    - **Ubicaciones** determina las ubicaciones donde se ejecutará la prueba.

    Si es necesario, puede escribir los valores de las variables definidas en el script de prueba. Por ejemplo, si el script necesita un nombre de usuario y una contraseña para conectar con un sitio web, puede escribir los valores para dichas variables. Puede definir distintos valores para las variables en distintas ubicaciones en la tabla **Variables de script** table.

    Pulse **Guardar** para terminar de configurar la prueba.

8.  Pulse **Finalizar**. El panel de control {{site.data.keyword.prf_hubshort}} muestra un resumen de todas las pruebas, un mapa y una tabla que muestran la gravedad y la ubicación de las alertas, todas las pruebas sintéticas asociadas con su aplicación, una tabla de sus actividades, y un gráfico de líneas que muestra el tiempo de respuesta y la disponibilidad de la aplicación y otros sitios web.
