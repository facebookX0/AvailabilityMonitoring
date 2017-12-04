---

copyright: years: 2015, 2017 lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Criando um script de teste por meio de um script em um repositório GitHub
{: #avmon_git_script_test}

Crie um script de teste por meio de um script do Selenium que estiver armazenado em seu repositório GitHub. Será
possível ativar o seu script de teste para sincronizar continuamente com qualquer mudança que você fizer no seu
Script do Selenium em seu repositório GitHub.
{: shortdesc}

## Antes de Come╬ar
{: #avmon_git_prereq}

Testes de script requerem scripts do Selenium para trabalhar. Para criar um script de teste, deve-se, primeiramente, criar um script do Selenium. Para obter mais informações sobre como criar scripts Selenium, veja [Gravando scripts sintéticos](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(Abre em uma nova guia ou janela)"){: new_window}.

Para criar testes de script de scripts do Selenium que estiverem armazenados em um repositório GitHub,
deve-se concluir as etapas a seguir:

-   Ative a {{site.data.keyword.contdelivery_full}} para seu aplicativo. Para
obter mais informações, veja [Entrega Contínua](../ContinuousDelivery/index.html "(aberta emuma nova guia ou janela)"){: new_window}.

-   Autorize o {{site.data.keyword.Bluemix_notm}} para acessar o GitHub como
parte de sua cadeia de ferramentas. Para obter mais informações, veja [Configurando o GitHub](../ContinuousDelivery/toolchains_integrations.html#github "(aberto em uma nova guia ou janela)"){: new_window}.

## Sobre essa Tarefa
{: #avmon_git_about}

Se você ativar a {{site.data.keyword.contdelivery_short}} para seu aplicativo, poderá criar um teste de script que esteja sincronizado com um script do Selenium em seu repositório GitHub. Se
você criar um script do Selenium que imita um usuário de seu aplicativo, poderá então executar um
teste de script periodicamente para testar o desempenho de seu aplicativo em resposta às ações do
usuário simulado.

## Criando um teste que usa um script GitHub
{: #avmon_git_create_test}

Para criar um teste de script, conclua as etapas a seguir.

1.  Se você estiver visualizando a guia Monitoramento, clique em **Incluir novo teste**.

    ![A guia Monitoramento do aplicativo Cloud Foundry.](images/avmon_tab.png)

    Se você estiver visualizando o painel {{site.data.keyword.prf_hubshort}}, clique em **Incluir novo teste** na área de janela Testes sintéticos.

    ![O botão Incluir novo teste na área de janela Testes sintéticos.](images/syn_tests_pane.jpg)

2.  Clique em **Comportamento com script** na página Configuração de monitoramento. A página Configuração do comportamento com script é exibida. Clique em **Repositório
Git**.
3.  Insira um nome significativo para o seu teste no campo **Nome**. Inclua uma descrição do propósito de seu teste no campo
**Descrição**.
4.  Selecione um repositório GitHub disponível e insira o caminho de arquivo no script em seu repositório escolhido.
5.  Para assegurar que o seu teste use continuamente a versão mais recente de seu script
do Selenium em seu **repositório Git**, selecione **Sincronizar automaticamente com o pipeline de entrega**.
6.  Use a **Lista de bloqueio** e a **Lista de desbloqueio** para especificar para quais URLs e domínios enviar solicitações e com quais URLs e domínios contribuir para as métricas e o status de seus testes de aplicativo. Inclua URLs e domínios que você deseja incluir ou bloquear na **Lista de desbloqueio** e na **Lista de bloqueio**. Para obter mais informações sobre como bloquear e filtrar, veja [Bloqueando e filtrando com a lista de desbloqueio e a lista de bloqueio](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "Usar a lista de desbloqueio e a lista de bloqueio para determinar para quais recursos enviar solicitações e com quais recursos contribuir para as métricas e status de seus testes de aplicativo. As listas de desbloqueio e as listas de bloqueio só ficam disponíveis para testes da página da web e de comportamento com script.").
7.  Para definir as suas
configurações de teste, clique em **Avançar**. Um resumo da configuração de teste é exibido. Por exemplo, a mensagem a seguir é exibida
para as configurações padrão:

    ``O teste ocorrerá: a cada 15 minutos em 3 locais simultaneamente para determinar se o teste excederá 5 segundos``.

    O uso estimado e número estimado de testes por mês são exibidos com base em sua configuração de teste atual.

8.  Na área de janela Configurações, clique em **Editar** para exibir as configurações atuais de seu teste. É possível atualizar as configurações a seguir:
    - **Intervalo** define com que frequência o teste é executado.
    - **Frequência de teste** determina se o teste é executado em todos os locais simultaneamente ou em um local diferente a cada intervalo. Selecione **Simultâneo** para executar o seu teste em todos os locais simultaneamente ou selecione **Escalonado** para
executar o seu teste de um local selecionado diferente a cada intervalo.
    - **Limite crítico** define o tempo de resposta para alertas críticos do teste.
    - **Limite de aviso** define o tempo de resposta para alertas de aviso do teste.
    - **Locais** determina os locais em que o teste será executado.

    Se necessário, é possível inserir os valores para variáveis que estão definidas em seu script
de teste. Por exemplo, se o seu script requerer um nome de usuário e uma senha para se conectar a um site,
será possível inserir os valores para essas variáveis. É possível configurar valores diferentes para suas variáveis em locais diferentes na tabela **Variáveis de script**.

    Clique em **Salvar** para
concluir a configuração do seu teste.

9.  Clique em **Terminar**. O painel {{site.data.keyword.prf_hubshort}} exibe um resumo de todos os seus testes, um mapa e uma tabela que exibem a severidade e o local de seus alertas, todos os testes sintéticos que estão associados ao aplicativo, uma tabela de suas atividades e um gráfico de linhas que descreve o tempo de resposta e a disponibilidade de seu aplicativo e outros websites.
