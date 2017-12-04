---

copyright:
  years: 2015, 2017
lastupdated: "2017-9-28"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Funcionamento do aplicativo
{: #avmon_health}

A área de janela Funcionamento do aplicativo fornece uma captura instantânea do desempenho de seu aplicativo com base na disponibilidade de seu aplicativo, na satisfação dos seus usuários com o desempenho de seu aplicativo e no rendimento de seu aplicativo.
{: shortdesc}

Se o {{site.data.keyword.prf_hubshort}} detectar que um coletor de dados está configurado para seu aplicativo, a área de janela Funcionamento do aplicativo estará disponível para visualização.

**Restrição:** inicialmente, um coletor de dados está disponível somente para aplicativos Node.js. Para obter mais informações sobre como configurar o coletor de dados Node.js, veja a [documentação do coletor de dados Node.js](https://www.npmjs.com/package/ibmapm "(aberta em uma nova guia ou janela)"){: new_window}.

A área de janela exibe três métricas: **Disponibilidade**, **Pontuação de satisfação** e **Volume de solicitações**.
![Área de janela Funcionamento do aplicativo que mostra o nível de disponibilidade, a satisfação do usuário e o rendimento da transação de seus apps.](images/avmon_app_health_ui.jpg) O cálculo da métrica **Disponibilidade** é baseado em dados de transações do usuário simulado de seus testes sintéticos. Em contraste, as métricas **Pontuação de satisfação** e **Volume de solicitações** dependem de dados de transações de usuários reais e simulados fornecidos por coletores de dados.

Os rótulos numéricos mostram o valor mais recente de cada métrica. Por exemplo, o valor mais recente para **Disponibilidade** é ![O valor mais recente da métrica Disponibilidade.](images/avmon_app_health_latest.jpg). Os gráficos de linha de série temporal representam o desempenho de seu aplicativo em cada métrica ao longo do tempo. É possível configurar a amplitude de tempo dos gráficos de histórico selecionando as últimas **24 horas** ou os últimos **Sete dias** na lista suspensa Tempo. Conforme você passa o mouse sobre a linha no gráfico, o valor para cada ponto de dados será exibido em uma dica de ferramenta, por exemplo, ![Uma dica de ferramenta no gráfico de linha de histórico.](images/avmon_app_health_hover.jpg). Quando você clica em um ponto de dados no gráfico de linha, o rótulo numérico exibe o valor para esse ponto de dados. Clique em qualquer área fora dos gráficos de linha para reconfigurar os rótulos numéricos para seus valores mais recentes. Passar o mouse ou clicar em um gráfico atualiza os outros dois gráficos na área de janela **Funcionamento do aplicativo**.

Clique em ![Menu Visualizar contribuições que você pode expandir para ver contribuições de transações ou testes.](images/avmon_view_contrib.jpg) para ver as cinco principais transações ou testes que contribuíram para o funcionamento atual do aplicativo.![Área de janela Funcionamento do aplicativo que mostra o nível de disponibilidade, satisfação do usuário e rendimento de transações do seu aplicativo.](images/avmon_app_health_expanded.jpg)

## Disponibilidade
{: #avmon_health_availability}
**Disponibilidade** mostra o grau no qual seu aplicativo está operacional. Disponibilidade é determinada pela porcentagem de suas instâncias de teste sintético que foram aprovadas com êxito. Por exemplo, se todos os seus testes sintéticos foram executados com êxito durante o intervalo mais recente, o valor de Disponibilidade atual para seu aplicativo será 100%.  É possível configurar como o {{site.data.keyword.prf_hubshort}} calcula a Disponibilidade na guia Monitoramento selecionando testes para inclusão no cálculo de Disponibilidade. Para obter mais informações, veja [Acessando o Monitoramento de disponibilidade](avmon_tab.html "É possível acessar o painel Monitoramento de disponibilidade na guia **Monitoramento**. A guia Monitoramento para o seu aplicativo Cloud Foundry exibe informações resumidas sobre a disponibilidade e o status dos seus testes, além de detalhes da assinatura e do uso de seu serviço.").

{{site.data.keyword.prf_hubshort}} calcula a porcentagem de suas instâncias de teste que estão disponíveis por hora. Passe o mouse sobre a linha no gráfico para ver o valor a cada intervalo de hora durante as últimas 24 horas ou os últimos sete dias.

Os cinco principais testes sintéticos que contribuíram para o nível de disponibilidade atual do seu aplicativo são mostrados. A tabela exibe as informações a seguir sobre cada um dos testes.

-   **Testes** exibe o nome do teste que você designou.
-   **Instâncias** mostra o número de instâncias de teste que foram executadas para cada teste.
-   **Taxa de falha** exibe a porcentagem de instâncias de teste que falharam para cada teste.


## Pontuação de satisfação
{: #avmon_health_satscore}
A **Pontuação de satisfação** é um indicador da satisfação do usuário com a responsividade do seu aplicativo. É possível configurar um valor limite de satisfação (**T**) para o seu aplicativo. É possível determinar qual tempo de resposta as solicitações do usuário devem atender para que seus usuários fiquem satisfeitos.

Tempos de resposta da solicitação do usuário são convertidos para um valor de índice entre 0,0 e 1,0, com 1,0 sendo uma pontuação perfeita com todos os usuários atendidos. Para calcular a pontuação de satisfação, as amostras do usuário são categorizadas como:

-   Satisfeitas - solicitações do usuário com um tempo de resposta menor ou igual ao limite de satisfação são consideradas Satisfeitas.
-   Toleradas - as solicitações de usuários que se enquadram entre Satisfeitas e Frustradas são consideradas Toleradas.
-   Frustradas - solicitações de usuário com um tempo de resposta superior a 4**T** ou que resultam em um erro, são consideradas Frustradas.

A pontuação de satisfação é então calculada como a proporção de [solicitações de usuários satisfeitas + (solicitações de usuários com tolerância/2)] / [número total de solicitações de usuários].

{{site.data.keyword.prf_hubshort}} calcula a pontuação de satisfação com base em dados de transações para cada intervalo de hora. Passe o mouse sobre a linha no gráfico para ver a pontuação para cada intervalo de hora durante as últimas 24 horas ou os últimos sete dias.

A tabela exibe as informações a seguir sobre as cinco principais transações que contribuíram para a pontuação de satisfação atual de seu aplicativo:

-   **Transações** exibe o nome da transação do usuário.
-   **Pontuação** mostra a pontuação de satisfação que é calculada para a transação individual.
-   **Insatisfação** mostra a contribuição da transação para os níveis atuais de insatisfação do usuário. Se a satisfação do usuário não for ideal, use o a porcentagem de **Insatisfação** para medir quanto cada transação impactou os níveis de insatisfação.


## Volume de solicitações
{: #avmon_health_reqvol}
A métrica Volume de solicitações é o volume atual de instâncias de transação do usuário. A métrica indica o rendimento real de seu aplicativo.

O tempo de resposta médio da transação para seu aplicativo também é exibido sob o rótulo, por exemplo, ![O valor mais recente do tempo de resposta médio.](images/avmon_app_health_response.jpg) e os valores de tempo de resposta médio são plotados no gráfico. É possível procurar correlações entre os aumentos na taxa de transferência e o aumento dos tempos médios de resposta.

Os dados brutos de volume de solicitações são agregados e exibidos no gráfico em uma base por hora. Passe o mouse sobre a linha no gráfico para ver o rendimento para seu aplicativo para cada intervalo de hora durante as últimas 24 horas ou os últimos sete dias.

A tabela exibe as informações a seguir sobre as cinco principais transações que estão mais contribuindo para o volume de solicitações atual. Se seu aplicativo estiver experimentando altos volumes de tráfego do usuário, use a **Porcentagem do total** para medir quanto cada transação está contribuindo para o volume de tráfego geral.

-   **Transação** exibe o nome da transação do usuário.
-   **Volume** mostra o número de instâncias de transação para cada transação.
-   **Porcentagem do total** exibe a porcentagem do volume total de solicitações.
