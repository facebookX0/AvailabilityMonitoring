---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Generación de alertas en la Supervisión de disponibilidad
{: #avmon_alert_desc}

En {{site.data.keyword.prf_hubshort}}, las pruebas pueden generar hasta un total de tres alertas. La prueba informa de la prueba con la gravedad más alta hasta que se resuelva la condición que causa la alerta.
{: shortdesc}

Se genera una alerta separada para tres situaciones diferentes:

-   Cuando el tiempo de respuesta de la aplicación web o URL supera los umbrales de aviso o críticos establecidos para su prueba. Cada prueba mide el tiempo de respuesta de forma predeterminada y genera una alerta en función de los umbrales de aviso o crítico definidos para dicha prueba.
-   Cuando la prueba devuelve un código de respuesta HTTP que indica que la aplicación web o URL no está disponible debido a un error de cliente o de servidor. Cada prueba comprueba de forma predeterminada el código de respuesta para determinar si la prueba se ha ejecutado correctamente o ha fallado.
-   Si la prueba determina que se han satisfecho una o varias condiciones personalizadas, se genera una alerta con la gravedad más alta definida por una o varias de las condiciones personalizadas. {{site.data.keyword.prf_hubshort}} tiene en cuenta todas las condiciones personalizadas de forma agregada cuando determina si se genera una alarma. Esta alarma permanece hasta que la prueba determina que ninguna de las condiciones personalizadas genera alertas de aviso o crítica.

Cuando se alcanza más de una alerta, {{site.data.keyword.prf_hubshort}} informará de la alerta con la mayor gravedad mientras haya alertas presentes.

Por ejemplo, si el tiempo de respuesta de prueba genera una alerta de aviso y otra condición genera una alerta de aviso, su prueba generará una alerta crítica y aparecerá en el panel de control de {{site.data.keyword.prf_hubshort}}. Si la condición que provoca una alerta crítica deja de producirse, la gravedad de la alerta de prueba pasa a ser "Aviso". La alerta permanece hasta que ninguna de las condiciones genera una alerta.
