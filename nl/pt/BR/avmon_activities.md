---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}


# Atividade
{: #avmon_activities}

Visualize informações para atividades na área de janela Atividade. _Atividades_ são ações que ocorrem fora dos eventos definidos pelo usuário.
{: shortdesc}

A área de janela Atividade exibe informações sobre todas as atividades para seu aplicativo, como iniciar, parar e implementar nas últimas 24 horas.

![Área de janela Atividade no painel Monitoramento de disponibilidade.](images/avmon_activity_pane.png)

Atividades do {{site.data.keyword.Bluemix_notm}} são eventos de aplicativo que ocorrem no {{site.data.keyword.Bluemix_notm}}, como seu aplicativo parando, iniciando ou sendo remontado. Atividades do pipeline são eventos que ocorrem em seu pipeline do DevOps,
como construções, implementações e testes. O cabeçalho da tabela exibe totais separados para as atividades do {{site.data.keyword.Bluemix_notm}} e atividades do pipeline. É possível filtrar por Origem da atividade para exibir atividades do {{site.data.keyword.Bluemix_notm}} ou atividades do Pipeline clicando nos ícones do {{site.data.keyword.Bluemix_notm}} ou do pipeline no cabeçalho da área de janela Atividade.

Para visualizar atividades do Pipeline no painel {{site.data.keyword.prf_hubshort}}, deve-se primeiramente ativar o {{site.data.keyword.contdelivery_short}} para seu aplicativo e configurar uma cadeia de ferramentas que contenha um pipeline e o serviço {{site.data.keyword.DRA_short}}. Clique em **Configuração do pipeline** para criar uma cadeia de ferramentas para
o seu aplicativo. Para obter mais informações,
veja [Introdução à Entrega Contínua](../ContinuousDelivery/index.html "(aberta em uma nova guia ou janela)"){:new_window} e [Introdução ao DevOps Insights](../DevOpsInsights/index.html#gettingstarted "(aberta em uma nova guia ou janela)").
{: tip}

Se você tiver o {{site.data.keyword.contdelivery_short}} e {{site.data.keyword.DRA_short}} configurado para seu aplicativo, poderá clicar em **Visualizar insights** na coluna Evento para acessar os painéis {{site.data.keyword.DRA_short}} e visualizar detalhes adicionais sobre as suas
atividades do pipeline.

Atividades do {{site.data.keyword.Bluemix_notm}} e do pipeline também são exibidas no **Feed de métrica** e no gráfico na área de janela Tempo de resposta e disponibilidade.
