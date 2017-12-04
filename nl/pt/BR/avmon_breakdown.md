---

copyright: years: 2015, 2017 lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Painel Detalhamento
{: avmon_view_breakdown}

O painel **Detalhamento** exibe informações estatísticas chave para os seus testes. O painel também resume informações de disponibilidade e de tempo de resposta, tendências históricas e dados de desempenho de teste nas últimas 24 horas.
{: shortdesc}

Para visualizar os detalhes de um teste, clique no teste na área de janela Testes sintéticos. Também é possível abrir o painel Detalhamento clicando em **Detalhes** na tabela Alerta na área de janela Frequência de alertas.

O painel Detalhamento exibe quatro áreas de janela:

## Resumo do teste
{: #avmon_bdown_summary}

![Área de janela Resumo do teste.](images/avmon_bdown_summ.png)

A área de janela **Resumo do teste** exibe as informações de teste a seguir para as últimas 24 horas:

-   **Status atual** exibe o status de teste.
-   **Instâncias de teste** exibe um detalhamento de porcentagem de instâncias de teste normais, de aviso e críticas.
-   **Tempo médio de resposta** exibe o tempo médio de resposta do teste.
-   **Tendências históricas** exibe as tendências históricas do desempenho do seu teste para o 50º, 95º e 99º percentis em segundos ou milissegundos.

## Instâncias de Teste
{: #avmon_bdown_instances}

![Detalhamento da instância de teste da API Rest na tabela Instâncias de teste.](images/avmon_bdown_apitest_instance.png)

A tabela **Instâncias de teste** exibe informações detalhadas sobre cada instância de teste, incluindo o status, o tempo de resposta, o local onde o teste foi executado, o número de erros e o registro de data de hora de quando o teste foi executado. Para realizar drill down em uma instância de teste, clique em **Expandir**. As informações de resposta detalhadas são listadas para cada etapa na instância de teste. É possível classificar quaisquer colunas para ajudá-lo a identificar rapidamente a etapa exata em que uma lentidão ou falha ocorreu. A visualização dos erros, a sequência de teste e o tempo de resposta ajudam a identificar problemas facilmente.

As informações que são exibidas dependem do tipo de teste Sintético que está sendo monitorado:

### API do
Quando você clicar em **Expandir** para uma instância de teste de API, um resumo de alto nível dos detalhes a seguir será exibido:

-   **Resposta** exibe o tempo de resposta total para a instância de teste, incluindo o tempo de redirecionamento.
-   **Redirecionamento** exibe o tempo de redirecionamento total para a instância de teste.
-   **Tamanho** exibe o tamanho do objeto.
-   **Velocidade de download** exibe a velocidade na qual cada objeto é transferido por download.
-   **Erros** exibe o número de erros que ocorreram durante a instância de teste. Para visualizar os detalhes do erro, clique no ícone **Informações**.

Uma tabela exibe cada etapa na chamada API, juntamente com o nome da etapa, a sequência de etapas e o tempo de resposta para cada etapa. Os nomes de etapa a seguir são exibidos:

-   **Consulta de nome** representa o tempo que a instância de teste levou para resolver o nome do objeto.
-   **Conectar** representa o tempo que a instância de teste levou desde o início da etapa até a conclusão de uma conexão com o host remoto ou proxy.
-   **Conexão do app** representa o tempo que a instância de teste levou desde o início da etapa até a conclusão da conexão SSL com o host remoto.
-   **Pré-transferência** representa o tempo que a instância de teste levou desde o início da etapa até pouco antes do início do comando de transferência de arquivos.
-   **Iniciar transferência** representa o tempo que a instância de teste levou desde o início da etapa até o primeiro byte ser recebido.
-   **Transferência** representa o tempo que a instância de teste levou para transferir o arquivo.

### Página da Web
![Detalhamento da instância de teste na tabela Instâncias de teste.](images/avmon_bdown_webpage_instance.png)

Quando você clicar em **Expandir** para uma instância de teste da página da web, um resumo de alto nível dos detalhes a seguir será exibido:

-   **Resposta** indica o tempo de resposta para a instância de teste.
-   **Total de solicitações (externas) ** exibe o número total de solicitações para a instância de teste. O número de solicitações externas está entre parênteses.
-   **Tamanho da página** exibe o tamanho da página da web.
-   **Erros** exibe o número de erros que ocorreram durante a instância de teste. Para visualizar os detalhes do erro, clique no ícone Informações.

Uma tabela que lista os detalhes a seguir para cada solicitação que é feita pelo teste também será exibida:

-   **Tipo** exibe o tipo de solicitação, por exemplo, HTML, CSS, JavaScript ou imagem. Solicitações externas e internas são representadas por ícones.
-   **Caminho do arquivo** descreve o local do objeto solicitado.
-   **Tamanho** exibe o tamanho do objeto solicitado.
-   **Sequência** exibe a sequência de solicitações que são feitas pelo teste.
-   **Tempo** exibe o tempo que cada solicitação leva.
-   **Código de status** exibe o código de status da solicitação HTTP.
-   **Status** descreve o resultado da solicitação, por exemplo, Concluído, Desconhecido ou Com falha.

### Script
![Detalhamento da instância de teste de script na tabela Instâncias de teste.](images/avmon_bdown_script_instance.png)

Quando você clicar em **Expandir** para uma instância de teste de script, o tempo de resposta, o número de etapas do script e o número de erros serão exibidos. Para visualizar os detalhes do erro, clique no ícone **Informações**.

Os detalhes a seguir para cada etapa de script serão exibidos em uma tabela:

-   **Nome** exibe cada comando do Selenium que é chamado por sua instância de teste, por exemplo, Open, ClickAt ou VerifyBodyText.
-   **Sequência** exibe a sequência de etapas do script desde o início até o fim da instância de teste.
-   **Tempo** exibe o tempo que cada etapa do script leva.
-   **Erros** exibe o número de erros que ocorreram durante cada etapa do script.
-   **Status** descreve o resultado da etapa de script, por exemplo, Concluído, Desconhecido ou Com falha.

É possível realizar drill down e visualizar detalhes sobre as solicitações que são geradas por cada etapa do script.

![Detalhamento das etapas individuais para sua instância de teste de script na tabela Instâncias de teste.](images/avmon_bdown_script_subtrans.png)

Clique em **Expandir** para visualizar uma tabela que contém os detalhes a seguir:

-   **Tipo** exibe o tipo de solicitação, por exemplo, HTML, CSS, JavaScript ou imagem. Solicitações externas e internas são representadas por ícones.
-   **Caminho do arquivo** descreve o local do objeto solicitado.
-   **Tamanho** exibe o tamanho do objeto solicitado.
-   **Sequência** exibe a sequência de solicitações que são feitas pelo teste.
-   **Tempo** exibe o tempo que cada solicitação leva.
-   **Código de status** exibe o código de status da solicitação HTTP.
-   **Status** descreve o resultado da solicitação, por exemplo, Concluído, Desconhecido ou Com falha.

O {{site.data.keyword.prf_hubshort}} poderá criar automaticamente uma captura de tela se a página da web falhar ao carregar ou se uma etapa no script falhar. Por exemplo, se uma das etapas em seu script abrir uma página da web, mas ela não for carregada, o {{site.data.keyword.prf_hubshort}} automaticamente criará uma captura de tela. Para visualizar uma captura de tela da página da web ou do script, clique no ícone
**Captura de tela de erro** ![Ícone de captura de tela de erro](images/scrnsht_err_icn_white.jpg). Esse recurso está disponível somente para monitoramento de páginas da web e de testes com script. Ele não funciona com o monitoramento de API de REST.

Também é possível fazer download de um registro do tráfego de rede para uma instância de teste específica como um arquivo .har clicando no ícone **Download** ![Ícone Download.](images/download_icn_white_smll.jpg). Esse recurso está disponível para monitoramento de página da web e de teste de comportamento em script.

## Tempo de Resposta e Disponibilidade
{: #avmon_bdown_rt_avail}
A área de janela Tempo de resposta e disponibilidade exibe um gráfico dos tempos de resposta medidos e da disponibilidade para as instâncias de seu teste durante um período definido. Para obter mais informações, veja [Tempo de resposta e disponibilidade](avmon_resptime_avail.html "Use a área de janela Tempo de resposta e disponibilidade para ajudá-lo a visualizar o tempo de resposta, as tendências de disponibilidade, os alertas e as atividades ao longo do tempo. A correlação de métricas, alertas e atividades ajudam a isolar facilmente uma mudança de aplicativo específica ou implementação de código quando você vê um tempo de resposta afetado.").

## Atividade
{: #avmon_bdown_activity}
A área de janela Atividade exibe uma tabela de todas as atividades nas últimas 24 horas. Para obter mais informações, veja [Atividade](avmon_activities.html "É possível visualizar informações para atividades na área de janela Atividade. As atividades são ações que ocorrem fora dos eventos definidos pelo usuário.").
