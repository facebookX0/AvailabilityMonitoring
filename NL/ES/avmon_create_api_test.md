---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Creación de una prueba de API REST
{: #avmon_rest_api}

Cree una prueba de API REST para probar el tiempo de respuesta y la disponibilidad de la aplicación web utilizando los siguientes métodos HTTP: GET,
POST, PUT y DELETE.
{: shortdesc}

Utilice las pruebas de API REST para supervisar la
disponibilidad y el rendimiento de la aplicación web y otros URL en respuesta a llamadas REST.

Para crear una prueba de API REST, siga los pasos siguientes.

1.  Si está viendo el separador **Supervisión** para la aplicación Cloud Foundry, pulse **Añadir prueba nueva**.

    ![El separador Supervisión para su aplicación Cloud Foundry.](images/avmon_tab.png)

    Si está viendo el panel de control de {{site.data.keyword.prf_hubshort}}, pulse **Añadir nueva prueba** en el panel Pruebas sintéticas.

    ![El botón Añadir nueva prueba en el panel Pruebas sintéticas.](images/syn_tests_pane.jpg)

2.  Pulse **Acción única** en la página Configuración de supervisión; a continuación, pulse **API REST** en la página Acción única.
3.  Escriba un nombre significativo para la prueba en el campo **Nombre**. Añada una descripción de la finalidad de la prueba en el campo **Descripción**.
4.  En la sección Solicitud, seleccione el tipo de método en la lista **Método** y escriba el **URL** que desee probar con este método. Puede elegir entre **GET**, **PUT**,
**POST** o **DELETE**. Si elige el método PUT o POST, puede especificar el contenido del cuerpo que desea probar en el campo **Cuerpo de solicitud (opcional)**.

    Por ejemplo, la siguiente API REST utiliza el método POST para solicitar que la aplicación web acepte datos además de probar la disponibilidad y el rendimiento de dicha aplicación web.

    ![Ejemplo de prueba de API REST que utiliza el método de solicitud POST.](images/avmon_restapi_post.png)

5.  Puede configurar la prueba de modo que incluya una determinada cabecera y valor. Escriba un nombre de cabecera y un valor de cabecera en los campos **Cabecera**.

    Si la aplicación web que desea probar necesita un inicio de sesión de usuario y una contraseña, escriba "Autorización" en el campo **Nombre de cabecera**. Especifique la palabra "Basic", un carácter de espacio y el valor codificado base64 del nombreusuario:contraseña en el campo **Valor de cabecera**.

    Por ejemplo, si su nombre de usuario es Aladdin y la contraseña es OpenSesame, escriba la palabra "Basic", un carácter de espacio y el valor codificado base64 de Aladdin:OpenSesame en el campo **Valor de cabecera**.

    ![Campos de cabecera que muestran credenciales de autorización de prueba en base64.](images/avmon_apitest_auth.png)

6.  Configure los umbrales de alerta de aviso y crítica de la prueba en la sección Validación de respuesta. Edite el **Valor** y la **Unidad** de cada fila. Los tiempos de respuesta que superan los umbrales de aviso y críticos activan alertas.

    ![Sección Validación de respuesta con umbrales de aviso y crítico predeterminados.](images/avmon_restapi_resp_val.png)

7.  Pulse **Añadir condición** para definir y añadir condiciones personalizadas de validación de respuestas. Las condiciones personalizadas de validación de respuestas se evalúan de forma agregada para generar una alerta. Puede definir y añadir un máximo de seis condiciones personalizadas para una prueba.

    En {{site.data.keyword.prf_hubshort}}, cada prueba puede generar un máximo total de tres alertas. La prueba informa de la alerta con la mayor gravedad hasta que todas las condiciones que causan alertas se resuelvan. Para obtener más información, consulte [Generación de alertas en la Supervisión de disponibilidad](avmon_alert_desc.html "En Supervisión de disponibilidad, las pruebas pueden generar hasta un total de tres alertas. La prueba informa de la alerta con la mayor gravedad hasta que la condición que causa la alerta se resuelva.")
    {: tip}

    Puede validar los siguientes datos:

    - **Código de respuesta de cabecera**. Seleccione **Código de respuesta de cabecera** para probar un código de respuesta HTTP o un rango de códigos.
    - **Propiedad de cabecera**. Seleccione **Propiedad de cabecera** para probar una determinada propiedad y valor del campo de cabecera de HTTP.
    - **Json de cuerpo**. Seleccione **JSON de cuerpo** para probar una determinada propiedad de un cuerpo de JSON.

      Para cada condición, especifique la propiedad que desea probar en el campo **Destino** y el valor que desea probar en el campo **Valor**. Seleccione un operador en el menú desplegable **Operación**. Finalmente, elija una Gravedad de alerta de **Aviso** o **Crítica** para la condición.

    Los valores numéricos que especifique en el campo **Valor** se tratan de forma predeterminada como números, no como series. Cuando especifique un **Valor** para una condición de validación de respuesta, utilice
comillas dobles "" para distinguir entre una serie y un número. Por ejemplo, para probar la serie 123, especifique "123" en el campo Valor. Para comprobar el número
400, escriba 400 sin comillas.
    {: tip}

    ![Condiciones de validación de respuesta para una prueba de API REST](images/avmon_restapi_resp_val2.png)

8.  Pulse **Verificar** para crear la prueba de la API REST y para determinar si la solicitud de prueba es válida.

    {{site.data.keyword.prf_hubshort}} determina la validez de la prueba utilizando el método HTTP seleccionado y cualquier cabecera que haya definido para la prueba. Durante la verificación de la prueba no se realiza ninguna validación de respuesta.

    La prueba validada se muestra en la tabla Elementos verificados. Para añadir más URL, repita los pasos 3 al 8.

9.  Para configurar los valores de prueba, pulse Siguiente.

    Se mostrará un resumen de la configuración de prueba. Por ejemplo, se muestra el siguiente mensaje para los valores predeterminados:

    ``La prueba se realizará: cada 15 minutos desde 3 ubicaciones simultáneamente para determinar si la prueba supera el umbral especificado.``

    El uso estimado y el número de pruebas estimadas por mes se muestran en función de la configuración actual de la prueba.

10. En el panel Configuración, pulse **Editar** para visualizar los valores actuales para la prueba.

    Puede modificar el intervalo de las pruebas, la frecuencia de las pruebas y las ubicaciones desde donde se envían las pruebas.

    ![Panel Valores de prueba que muestra los valores predeterminados para una prueba.](images/avmon_settings.png)

    Seleccione **Simultáneo** para ejecutar la prueba simultáneamente desde todas las ubicaciones o bien **Escalonado** para ejecutar la prueba desde una ubicación distinta seleccionada en cada intervalo. Pulse **Guardar** para terminar de configurar la prueba.

11. Pulse **Finalizar**. El panel de control {{site.data.keyword.prf_hubshort}} muestra un resumen de todas las pruebas, un mapa y una tabla que muestran la gravedad y la ubicación de las alertas, todas las pruebas sintéticas asociadas con su aplicación, una tabla de sus actividades, y un gráfico de líneas que muestra el tiempo de respuesta y la disponibilidad de la aplicación y otros sitios web.
