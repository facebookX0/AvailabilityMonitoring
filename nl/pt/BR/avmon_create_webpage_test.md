---

copyright: years: 2015, 2017 lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Criando um teste de página da web
{: #avmon_webpage_test}

Crie um teste de página da web para testar a disponibilidade de seu aplicativo da web
e para monitorar quanto tempo essa página leva para ser aberta.
{: shortdesc}

## Sobre essa Tarefa
{: #avmon_webpage_about}

Os testes da página da web relatam o tempo de resposta para carregar a URL de seu
aplicativo da web. Crie um teste de página da web para monitorar a disponibilidade e o tempo
de resposta de seu aplicativo da web.

## Criando e configurando seu teste de página da web
{: #avmon_create_web_test}

Para criar um teste de página da web, conclua as etapas a seguir.

1.  Se você estiver visualizando a guia Monitoramento, clique em **Incluir novo teste**.

    ![A guia Monitoramento do aplicativo Cloud Foundry.](images/avmon_tab.png)

    Se você estiver visualizando o painel {{site.data.keyword.prf_hubshort}}, clique em **Incluir novo teste** na área de janela Testes sintéticos.

    ![O botão Incluir novo teste na área de janela Testes sintéticos.](images/syn_tests_pane.jpg)

2.  Clique em **Ação única** na página Configuração de monitoramento; em seguida, clique em **Página da web** na página Ação única.
3.  Insira um nome significativo para o seu teste no campo **Nome**. Inclua uma descrição do propósito de seu teste no campo
**Descrição**.
4.  Insira a **URL** do aplicativo da web que você deseja testar.
5.  Configure os limites de alerta de aviso e de alerta crítico de seu teste na seção Validação de resposta. Edite o **Valor** e a
**Unidade** para cada linha. Os tempos de resposta que excedem o seu aviso e os limites críticos acionam alertas.

    ![Seção Validação de resposta com limite de aviso padrão e limite crítico padrão.](images/avmon_webpage_resp_val.png)

6.  Use a **Lista de bloqueio** e a **Lista de desbloqueio** para especificar para quais URLs e domínios enviar solicitações e com quais URLs e domínios contribuir para as métricas e o status de seus testes de aplicativo. Inclua URLs e domínios que você deseja incluir ou bloquear na **Lista de desbloqueio** e na **Lista de bloqueio**. Para obter mais informações sobre como bloquear e filtrar, veja [Bloqueando e filtrando com a lista de desbloqueio e a lista de bloqueio](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "Usar a lista de desbloqueio e a lista de bloqueio para determinar para quais recursos enviar solicitações e com quais recursos contribuir para as métricas e status de seus testes de aplicativo. As listas de desbloqueio e as listas de bloqueio só ficam disponíveis para testes da página da web e de comportamento com script.").
7.  Clique em **Verificar** para criar seu teste de página da web e para determinar se a sua solicitação de teste é
válida.

    O {{site.data.keyword.prf_hubshort}} determina a validade do teste enviando uma solicitação GET para sua
URL de teste. Nenhuma validação de resposta ocorre durante a verificação de teste.

    Seu teste validado será exibido na tabela Itens verificados. É possível incluir mais
URLs repetindo as etapas 3 a 7.

8.  Para definir as suas
configurações de teste, clique em **Avançar**. Um resumo da configuração de teste é exibido. Por exemplo, a mensagem a seguir é exibida
para as configurações padrão:

    ``O teste ocorrerá: A cada 15 minutos em três locais simultaneamente para determinar se o teste excede o limite especificado``.

    O uso estimado e número estimado de testes por mês são exibidos com base em sua configuração de teste atual.

9.  Na área de janela Configurações, clique em **Editar** para exibir as configurações atuais de seu teste. É possível atualizar as configurações a seguir:
    - **Intervalo** define com que frequência o teste é executado.
    - **Frequência de teste** determina se o teste é executado em todos os locais simultaneamente ou em um local diferente a cada intervalo. Selecione **Simultâneo** para executar o seu teste em todos os locais simultaneamente ou selecione **Escalonado** para
executar o seu teste de um local selecionado diferente a cada intervalo.
    - **Locais** determina os locais em que o teste será executado.

    Clique em **Salvar** para
concluir a configuração do seu teste.

10. Clique em **Terminar**. O painel {{site.data.keyword.prf_hubshort}} exibe um resumo de todos os seus testes, um mapa e uma tabela que exibem a severidade e o local de seus alertas, todos os testes sintéticos que estão associados ao aplicativo, uma tabela de suas atividades e um gráfico de linhas que descreve o tempo de resposta e a disponibilidade de seu aplicativo e outros websites.
