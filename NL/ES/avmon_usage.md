---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Uso de servicios
{: #avmon_usage}

Puede ver detalles sobre el uso de {{site.data.keyword.prf_hubshort}} en el separador **Supervisión** para su app, y en el panel de control principal de {{site.data.keyword.prf_hubshort}}.

Para ver una descripción general del uso de {{site.data.keyword.prf_hubshort}} desde la tabla **Todas las aplicaciones**, pulse el nombre de la app; a continuación, pulse el separador **Supervisión** en el panel de la app. Su porcentaje de **Uso** se muestra en un gráfico de indicador, junto con el plan que está utilizando.

Para ver una descripción general del uso del panel de control principal de {{site.data.keyword.prf_hubshort}}, pulse el icono **Configurar** ![icono Configurar](images/config_icn_white_smll.jpg). Si es un usuario del plan Lite de {{site.data.keyword.prf_hubshort}}, el uso se muestra como un gráfico de barras y como un porcentaje, junto con el número de pruebas en uso. Si es un usuario del plan de pago, el uso se muestra en puntos de datos. Puede ver los detalles de uso para cada prueba individual en el panel Pruebas sintéticas.

El uso se mide en puntos de datos. El número estimado de puntos de datos se calcula con la siguiente fórmula:

Número estimado de puntos de datos = T \* L \* (60/M \* 24 \* 30) al mes

Donde T = número de pruebas sintéticas que se han ejecutado, L = número de ubicaciones y M = intervalo entre pruebas (minutos).

Las pruebas sencillas, como las pruebas de página web y de API REST, utilizan 1 punto de datos para cada prueba. Las pruebas avanzadas, como las de scripts Selenium y de scripts de API REST, utilizan 100 puntos de datos para cada prueba.

Puede ver el uso real en el panel de control Uso en la página Cuenta de {{site.data.keyword.Bluemix_notm}}. Pulse **Cuenta**; a continuación, seleccione **Panel de control de uso** y desplácese hasta la sección **Cargos por servicio**. Pulse el icono **Flecha** correspondiente al servicio {{site.data.keyword.prf_hubshort}} para ver el número de puntos de datos que ha utilizado. Para obtener más información sobre las tarifas y los planes de uso de {{site.data.keyword.prf_hubshort}}, consulte el apartado Planes de tarifas en la página de catálogo de [Supervisión de disponibilidad](https://console.{DomainName}/catalog/services/availability-monitoring/ "(Se abre en un nuevo separador o ventana)"){: new_window}.
