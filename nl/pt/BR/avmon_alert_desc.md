---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Geração de alertas no Monitoramento de disponibilidade
{: #avmon_alert_desc}

No {{site.data.keyword.prf_hubshort}}, os testes podem gerar um total de até três alertas. Seu teste relatará o alerta com a maior severidade até que a condição que causa o alerta seja resolvida.
{: shortdesc}

Um alerta separado é criado para três situações diferentes:

-   Quando o tempo de resposta de seu aplicativo da web ou da URL exceder os limites de aviso ou críticos configurados para o seu teste. Cada teste mede o tempo de resposta por padrão e levanta um alerta com base no aviso e nos limites críticos para esse teste.
-   Quando o teste retorna um código de resposta de HTTP que indica que seu aplicativo da web ou URL está indisponível devido a um erro do cliente ou servidor. Cada teste verifica o código de resposta por padrão, para determinar se o teste é bem-sucedido ou falha.
-   Quando o seu teste determina que uma ou mais condições customizadas estão satisfeitas, um alarme é levantado com a gravidade mais alta conforme definido por uma ou mais de suas condições customizadas. O {{site.data.keyword.prf_hubshort}} considera todas as condições customizadas em conjunto ao determinar se um alarme é levantado. Esse alarme permanece até que o teste determine que nenhuma de suas condições customizadas geram mais aviso ou alertas críticos.

Quando mais de um alerta for levantado, o {{site.data.keyword.prf_hubshort}} relatará o alerta com a maior severidade enquanto os alertas estiverem presentes.

Por exemplo, se o tempo de resposta de seu teste levantar um alerta de aviso e outra condição levantar um alerta de aviso, um alerta crítico será gerado pelo seu teste e aparecerá no painel {{site.data.keyword.prf_hubshort}}. Se a condição que causar um alerta crítico não for mais verdadeira, então, a gravidade de seu alerta de teste mudará para "Aviso". Um alerta permanecerá até que nenhuma condição cause mais um alerta.
