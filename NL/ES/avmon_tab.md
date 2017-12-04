---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Acceso a la Supervisión de disponibilidad
{: #avmon_tab}

Puede acceder al panel de control de {{site.data.keyword.prf_hubshort}} desde el separador **Supervisión**. El separador **Supervisión** de la aplicación Cloud Foundry muestra información de resumen sobre la disponibilidad y el estado de las pruebas y detalles y uso de su suscripción de servicio.
{: shortdesc}

Para acceder a {{site.data.keyword.prf_hubshort}}, siga estos pasos:

1.  Pulse el nombre de una aplicación Cloud Foundry en el panel de control **Apps**.
2.  Pulse el separador **Supervisión**.

El separador **Supervisión** muestra tres indicadores que muestran la **Disponibilidad de prueba media** en las últimas 24 horas, el **Estado de prueba actual** de todas las pruebas y el **Uso de servicio** de la asignación del plan actual.

![Separador Supervisión de disponibilidad](images/avmon_tab.png)

Puede configurar el modo en que {{site.data.keyword.prf_hubshort}} calcula la **Disponibilidad media de prueba** seleccionando pruebas para incluirlas en el Cálculo de disponibilidad. Pulse el icono de **flecha** ![icono de flecha](images/arrow_dwn_icn_white.jpg) del indicador **Disponibilidad media de prueba** para ver las tarjetas de prueba; a continuación, pulse **Cálculo de disponibilidad**. Pulse una tarjeta para añadirla o eliminarla del cálculo. Las tarjetas excluidas quedan borrosas. Cuando termine, pulse **He terminado**. El indicador **Disponibilidad media de prueba** se renueva.

Para ver el estado de todas las pruebas, pulse el icono de **flecha** ![icono de flecha](images/arrow_dwn_icn_white.jpg) del indicador **Estado de prueba actual**. Se muestran las tarjetas correspondientes a las pruebas.

Para acceder al panel de control de {{site.data.keyword.prf_hubshort}}, pulse **Ver detalles de supervisión**. En el panel de control {{site.data.keyword.prf_hubshort}}, puede supervisar la disponibilidad de la aplicación en función de las pruebas sintéticas. También puede supervisar la capacidad de respuesta y el rendimiento de la aplicación en función de los datos de transacción de usuario que se proporcionan en los recopiladores de datos.

Para ver y editar las pruebas en el panel Pruebas sintéticas, pulse **Ver todas las pruebas**. Para crear una prueba, pulse **Añadir prueba nueva**.

Para descargar un informe de archivo .csv de la disponibilidad mensual, semanal y diaria y los promedios de tiempo de respuesta para la aplicación, pulse el icono **Descargar** ![icono Descargar](images/download_icn_white_smll.jpg).
