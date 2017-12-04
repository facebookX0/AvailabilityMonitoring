---

copyright: years: 2015, 2017 lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Uso de serviço
{: #avmon_usage}

É possível visualizar detalhes sobre seu uso do {{site.data.keyword.prf_hubshort}} na guia**Monitoramento** para seu app e no painel principal do {{site.data.keyword.prf_hubshort}}

Para ver uma visão geral de seu uso do {{site.data.keyword.prf_hubshort}} na tabela**Todos os aplicativos**, clique no nome do seu app; em seguida, clique na guia **Monitoramento** na área de janela do seu app. A porcentagem de **Uso**
é exibida em um gráfico de calibrador, juntamente com o plano que você está usando.

Para ver uma visão geral de seu uso no painel {{site.data.keyword.prf_hubshort}} principal,
clique no ícone **Configurar** ![Ícone Configurar](images/config_icn_white_smll.jpg). Se você for um usuário do plano Lite do {{site.data.keyword.prf_hubshort}},
seu uso será exibido com um gráfico de barras e como uma porcentagem, junto com o número de testes em uso. Se você for um usuário do plano Pago, seu uso será exibido nos pontos de dados. É possível visualizar os detalhes de uso para cada teste individual na área de janela Testes sintéticos.

Seu uso é medido em pontos de dados. O número estimado de pontos de dados é calculado por meio da fórmula a seguir:

Número estimado de pontos de dados = T \ * L \ * (60/M \ * 24 \ * 30) por mês

Em que T = número de testes sintéticos que são executados, L = número de locais e
M = intervalo entre os testes (minutos).

Testes simples, tais como testes de página da web e de API de REST usam um ponto de dados
para cada teste. Testes avançados, tais como scripts Selenium e scripts API de REST usam
100 pontos de dados para cada teste.

É possível visualizar seu uso real no painel de uso na página Conta do {{site.data.keyword.Bluemix_notm}}. Clique em **Conta**; em
seguida, selecione **Painel** e role para baixo para a seção **Encargos
de serviço**. Clique no ícone de **Seta** para o
serviço {{site.data.keyword.prf_hubshort}} para
visualizar quantos pontos de dados você usou. Para obter mais informações sobre planos de precificação e uso do {{site.data.keyword.prf_hubshort}}, veja Planos de precificação na página do catálogo [Monitoramento de disponibilidade](https://console.{DomainName}/catalog/services/availability-monitoring/ "(aberta em uma nova guia ou janela)"){: new_window}.
