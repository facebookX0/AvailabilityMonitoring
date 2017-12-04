---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Tempo de Resposta e Disponibilidade
{: #avmon_resptime_avail}

Use a área de janela Tempo de resposta e disponibilidade para ajudá-lo a visualizar o tempo de resposta, as tendências de disponibilidade, os alertas e as atividades ao longo do tempo. A correlação de métricas, os alertas e as atividades o ajudam a isolar facilmente uma mudança de aplicativo específica
ou uma implementação de código quando você vê um tempo de resposta afetado.
{: shortdesc}

## do Aplicativo
{: #avmon_resptime_graph}

As informações de tempo de resposta são exibidas em um gráfico de linhas. Para visualizá-las,
clique na guia **Tempo de resposta**.

![Gráfico de tempos de resposta para um teste nas 24 horas anteriores.](images/avmon_rt_gr.jpg)

Os tempos de resposta que são medidos por
{{site.data.keyword.prf_hubshort}} são um pouco maiores do que
os tempos de resposta que os usuários têm. O {{site.data.keyword.prf_hubshort}}
simula o comportamento do usuário real, que inclui sobrecarga para a medida de tempo de resposta. A sobrecarga
deve-se aos fatores a seguir:
  - O {{site.data.keyword.prf_hubshort}} cria uma nova instância
do Firefox para cada teste para evitar que as reproduções prévias influenciem o teste atual. Os usuários
finais reais podem ter tempos de resposta mais rápidos em virtude do armazenamento em cache do navegador.
  - O {{site.data.keyword.prf_hubshort}} instala o plug-in do driver
da web do Firefox antes de cada teste.
{: tip}

Tempos de resposta individuais para testes são representados por um ícone **Ponto de resposta** ![Ícone de Ponto de resposta](images/crcl_icn_white.jpg)
no gráfico de linha. Diferentes cores indicam diferentes localizações geográficas nas quais o aplicativo está em execução. O eixo y do gráfico usa ícones de alerta para identificar os intervalos de limites de aviso e críticos. O ícone amarelo **aviso** ![Ícone amarelo deaviso](images/alrt_icn_white_smll.jpg) representa o intervalo de limites de aviso e o ícone vermelho **crítico**

![Ícone vermelho crítico](images/wrng_icn_white_smll.jpg) representa o intervalo de limites críticos. Clique no ícone amarelo **aviso** ![Ícone amarelo de aviso](images/alrt_icn_white_smll.jpg) ou o ícone vermelho **crítico** ![Ícone vermelho crítico](images/wrng_icn_white_smll.jpg) para identificar facilmente as instâncias de teste que aparecem nos
intervalos de limites de aviso e críticos. Para visualizar os detalhes para uma instância de teste específica, clique no ícone **Ponto de resposta** ![Ícone de Ponto de resposta](images/crcl_icn_white.jpg) no gráfico.

### Filtros de parte

Escolha um teste no menu suspenso **Teste**. É possível filtrar dados para 3 horas, 24 horas, 7 dias, 30 dias e 12
meses. A capacidade de
visualizar dados de mais de 12 meses está disponível apenas para usuários com assinaturas pagas
para o {{site.data.keyword.prf_hubshort}}. Ao filtrar por um intervalo de tempo maior que 24 horas, os valores
que são exibidos no gráfico são medidos. Para visualizar
informações mais específicas, clique no gráfico para realizar drill down nos alertas e avisos
individuais. Também é possível usar a régua de controle para restringir ou expandir o intervalo
de tempo.

Com o gráfico Tempo de resposta, é possível
destacar e ocultar os dados de locais de PoP específicos. Para destacar dados de tempo de resposta
para um local específico, passe o mouse sobre o nome do local de PoP; em seguida, clique no ícone
**Destacar local** ![Ícone Destacar local](images/avmon_location_highlight.jpg). Para ocultar dados de tempo de resposta para um local, passe o mouse
sobre o nome do local de PoP; em seguida, clique no ícone **Ocultar local** ![Ícone Ocultar local](images/avmon_location_remove.jpg). Para
restaurar dados do local de PoP para o gráfico, clique em **Incluir mais locais** ![Ícone Incluir mais locais](images/icn_plus_20x20.jpg) ou na guia **Seleção de métrica**; em seguida, clique no local de PoP que foi removido anteriormente.

### Alertas e atividades

É possível identificar facilmente alertas de aviso e críticos na linha Alertas. Passe o
mouse sobre um **ícone de alerta** ![Ícone de alerta crítico](images/avmon_crit_alert.png)![Ícone de alerta de aviso](images/avmon_warn_alert.png)
para identificar a severidade e o registro de data e hora para esse alerta. Clique em um
**ícone de alerta** para exibir detalhes para esse alerta no **Feed de métrica**.

Também é possível visualizar atividades no mesmo gráfico. _Atividades_ são ações que ocorrem e que não são eventos definidos pelo usuário. Atividades do {{site.data.keyword.Bluemix_notm}} são eventos de aplicativo que ocorrem no {{site.data.keyword.Bluemix_notm}}, como seu aplicativo parando, iniciando ou sendo remontado. Atividades do pipeline são eventos que ocorrem em sua cadeia de ferramentas {{site.data.keyword.contdelivery_short}}, tais como construções, implementações
e testes. Clique em uma
atividade para exibir informações sobre essa atividade no **Feed de métrica**. É possível visualizar informações sobre essas atividades na área de janela Atividade.

Para visualizar atividades do Pipeline no painel {{site.data.keyword.prf_hubshort}}, deve-se primeiramente ativar o {{site.data.keyword.contdelivery_short}} para seu aplicativo e configurar uma cadeia de ferramentas que contenha um pipeline e o serviço {{site.data.keyword.DRA_short}}. Clique em **Configuração do pipeline** na área de janela Resumo ou na área de janela
Atividade para criar uma cadeia de ferramentas para o seu aplicativo. Para obter mais informações,
veja [Introdução à Entrega Contínua](../ContinuousDelivery/index.html "(aberta em uma nova guia ou janela)") e [Introdução ao DevOps Insights](../DevOpsInsights/index.html#gettingstarted "(aberta em uma nova guia ou janela)"){: new_window}.
{: tip}

Se houver mais de um ícone de atividade ou alerta próximos nas linhas Alertas e Atividade, um **ícone de número** exibirá o número de alertas ou atividades nesse momento.
Passe o mouse sobre um **ícone de número** para exibir os alertas individuais ou atividades e clique em um alerta ou em uma atividade para visualizar informações no **Feed
de métrica**.

### Seleção de métrica e Feed de métricas

Para filtrar para métricas por região geográfica, clique em **Seleção de métrica**. Clique em
um local para incluir ou remover métricas que são medidas nesse local por meio do gráfico. Clique em **Incluir mais locais** para abrir a página Testar modo de edição e incluir um local de PoP em seu teste selecionado.

![Guia de seleção de métricas que exibe filtros de local de PoP.](images/avmon_metric_sel.jpg)

Para visualizar uma lista de detalhes de métrica, clique em **Feed de métrica**. O Feed de métricas exibe uma lista das instâncias nas quais uma métrica é preenchida.

![Guia de seleção de métricas que exibe detalhes de alerta de aviso.](images/avmon_warn_met_feed.png)

Clique em um **ícone de alerta**, **ícone de atividade** ou **ponto de resposta** ![Ícone de Ponto de resposta](images/crcl_icn_white.jpg) no gráfico para incluir os detalhes dessa métrica no Feed de métricas.

![Detalhes de uma instância de teste disponível no Feed de métricas.](images/avmon_avail_metfeed.png)

Se você filtrar o gráfico Tempo de resposta para um intervalo de tempo maior que 24 horas
e clicar em um **Ponto de resposta**, poderá ver detalhes agregados para esse dia no Feed de métricas.

![Feed de métricas mostrando detalhes agregados de todas as instâncias do seu teste para um dia.](images/avmon_avail_day_met_feed.png)

Clique em **Zoom** para visualizar todos os tempos de resposta, as atividades e os alertas que foram gerados pelo teste para esse dia no gráfico Tempo de resposta.

Para visualizar informações detalhadas sobre um alerta ou tempo de resposta de alerta,
clique em **Detalhamento** no Feed de métricas. Clique em **Alerta mais próximo** para visualizar o alerta mais próximo a essa instância de teste no Feed
de métricas, se um alerta ocorreu. Para visualizar informações detalhadas sobre uma atividade do
pipeline no serviço {{site.data.keyword.DRA_short}}, clique em **Visualizar
insights** no Feed de métricas.

## Disponibilidade
{: #avmon_avail_graph}

Para visualizar as informações de disponibilidade para seus aplicativos, clique em Disponibilidade. O gráfico Disponibilidade mostra a disponibilidade diária de cada ponto de presença (PoP) para o teste selecionado.

![Gráfico de disponibilidade que exibe a disponibilidade diária de teste por localidade nos sete dias anteriores.](images/avmon_avail_graph.png)

Com o gráfico Disponibilidade, é possível destacar
e ocultar os dados de locais de PoP específicos. Para destacar os dados de disponibilidade para
um local específico, passe o mouse sobre o **Nome do local de PoP**; em seguida,
clique no ícone **Destacar local** ![Ícone Destacar local](images/avmon_location_highlight.jpg). Para
ocultar dados de disponibilidade para um local, passe o mouse sobre o **Nome do local
de PoP**; em seguida, clique no ícone **Ocultar local**
![Ícone Ocultar local](images/avmon_location_remove.jpg). Para restaurar dados da localização de PoP para o gráfico, clique na guia **Seleção de
métrica**; em seguida, clique na localização do PoP que você removeu anteriormente.

Passe o mouse sobre um ponto gráfico para exibir a taxa de falha e o número de instâncias de teste para um
dia e local específicos. Clique em um ponto de gráfico para exibir essas informações no Feed de métricas.

![Disponibilidade de teste no PoP de Dallasexibido no Feed de métricas.](images/avmon_avail_metric.png)


Clique em **Zoom** para filtrar o gráfico Disponibilidade e o gráfico
Tempo de Resposta para exibir informações para o dia selecionado.
