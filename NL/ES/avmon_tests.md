---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Pruebas sintéticas
{: #avmon_synth_tests}

En el panel Pruebas sintéticas, puede crear, editar, suprimir y ver pruebas sintéticas que supervisan el rendimiento y la disponibilidad de las aplicaciones. Las pruebas se muestran en una lista o vista de tarjeta en el panel Pruebas sintéticas.
{: shortdesc}

![El panel Pruebas sintéticas.](images/syn_tests_pane.jpg)

Cada tarjeta de prueba muestra información sobre la prueba:

- **Disponibilidad** muestra el porcentaje de disponibilidad de la prueba en las últimas 24 horas.
- **Estado** muestra el estado actual de la prueba. El estado puede ser Crítico, Aviso, Normal, Error, Inactivo o Desconocido.
- **Respuesta media** muestra el tiempo de respuesta medio de la prueba en las últimas 24 horas.

Puede supervisar tres tipos distintos de pruebas:

- Las pruebas de **API REST** informan del tiempo de respuesta de una llamada REST. Se admiten todos los formatos de solicitud HTTP, como GET, POST, PUT y DELETE.
- Las pruebas de **Página web** informan del tiempo de respuesta para cargar el sitio web en el URL que ha especificado.
- Las pruebas de **Comportamiento programado** supervisan los scripts Selenium que crea para imitar las interacciones de un usuario con un sitio web. Por ejemplo, puede crear un script de Selenium que imite a un usuario que está iniciando sesión en la aplicación. Ejecute este script periódicamente para probar el rendimiento de la aplicación en respuesta a las acciones del usuario que automatiza el script. Puede cargar un script o añadir un script desde un repositorio de GitHub. Para obtener más información sobre la creación de scripts de Selenium, consulte [Grabación de scripts sintéticos](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(Se abre en un nuevo separador o ventana)"){: new_window}.

Para añadir otra prueba, pulse **Añadir prueba nueva**.

Para detener, iniciar, suprimir o editar una prueba sintética, pulse el icono **Acciones** ![icono Acciones](images/actions_icn_white_smll.jpg) y pulse la acción que desee. Para ver los detalles de Desglose de la prueba, pulse la prueba.

Para ver el uso específico de cada prueba sintética, pulse el icono **Coste** ![icono Coste](images/cost_icn_white_smll.jpg). Si está suscrito al plan de pago, el uso se muestra en puntos de datos.
