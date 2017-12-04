---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Introdução ao monitoramento de disponibilidade
{: #avmon_gettingstarted}

Use o {{site.data.keyword.prf_hublong}} para
executar testes de desempenho simulados de localizações ao redor do mundo, a qualquer hora. Detecte, isole e diagnostique proativamente problemas de desempenho antes que eles afetem os seus usuários. Assegure-se de que seus aplicativos estejam disponíveis e atendam às metas de tempo de resposta
quando você realiza atualizações contínuas. Configure os coletores de dados para seus aplicativos para coletar dados de transação do usuário. Use esses dados em {{site.data.keyword.prf_hubshort}} para monitorar a responsividade e o rendimento do seu aplicativo.
{: shortdesc}

## Sobre essa Tarefa
{: #avmon_start_about}

O {{site.data.keyword.prf_hubshort}} está
disponível como um serviço no domínio DevOps no catálogo do {{site.data.keyword.Bluemix_notm}}. Ele também está
disponível por padrão no painel Aplicativo na guia **Monitoramento**. É possível iniciar o monitoramento da disponibilidade e do desempenho do seu aplicativo imediatamente. Quando
você vincular o {{site.data.keyword.prf_hubshort}} com seu aplicativo, um teste sintético
será criado automaticamente para monitorar a URL do aplicativo principal por padrão.

## Criando um teste de página da web
{: #avmon_start_procedure}

Conclua as etapas a seguir para abrir {{site.data.keyword.prf_hubshort}} para seu
aplicativo, para criar um teste de página da web para monitorar outra URL e para configurar alertas
de notificação para seus testes.

1.  Se você tiver um aplicativo Cloud Foundry que deseja monitorar, clique no nome do
aplicativo na tabela **Todos os aplicativos** no painel **Apps**.
Se você ainda não tiver um aplicativo, crie-o e o cartão do aplicativo será aberto automaticamente. Os aplicativos Cloud Foundry serão automaticamente vinculados ao {{site.data.keyword.prf_hubshort}} quando você clicar na guia Monitoramento.
2.  Para abrir o {{site.data.keyword.prf_hubshort}}, clique na
guia **Monitoramento**. A guia **Monitoramento** exibe
três medidores que mostram **Disponibilidade média do teste** nas últimas
24 horas, **Status atual do teste** e **Uso** de sua
alocação de plano atual. Clique em **Incluir novo teste** para configurar um teste de monitoramento.

    ![Guia Monitoramento de disponibilidade](images/avmon_tab.png)

    A URL do aplicativo principal é monitorada por padrão. Quaisquer outros serviços e URLs que você
monitora podem estar dentro ou fora do Bluemix e não precisam estar relacionados ao aplicativo Cloud
Foundry associado.

3.  Clique em **Ação única** na página Configuração de monitoramento; em seguida, clique em **Página da web** na página Ação única.
4.  Insira um nome significativo para o seu teste no campo **Nome**. Inclua uma descrição do propósito de seu teste no campo
**Descrição**.
5.  Insira a **URL** do aplicativo da web que você deseja testar.
6.  Configure os limites de alerta de aviso e de alerta crítico de seu teste na seção Validação de resposta. Edite o **Valor** e a
**Unidade** para cada linha. Os tempos de resposta que excedem o seu aviso e os limites críticos acionam alertas.

    ![Seção Validação de resposta com limite de aviso padrão e limite crítico padrão.](images/avmon_webpage_resp_val.png)

7.  Use a **Lista de bloqueio** e a **Lista de desbloqueio** para especificar para quais URLs e domínios enviar solicitações e com quais URLs e domínios contribuir para as métricas e o status de seus testes de aplicativo. Inclua URLs e domínios que você deseja incluir ou bloquear na **Lista de desbloqueio** e na **Lista de bloqueio**. Para obter mais informações sobre como bloquear e filtrar, veja [Bloqueando e filtrando com a lista de desbloqueio e a lista de bloqueio](avmon_whitelist_blacklist.html "Usar a lista de desbloqueio e a lista de bloqueio para determinar para quais recursos enviar solicitações e com quais recursos contribuir para as métricas e status de seus testes de aplicativo. As listas de desbloqueio e as listas de bloqueio só ficam disponíveis para testes da página da web e de comportamento com script.").
8.  Clique em **Verificar** para criar seu teste de página da web e para determinar se a sua solicitação de teste é
válida.

    O {{site.data.keyword.prf_hubshort}} determina a validade do teste enviando uma solicitação GET para sua
URL de teste. Nenhuma validação de resposta ocorre durante a verificação de teste.

    Seu teste validado será exibido na tabela Itens verificados. É possível incluir mais URLs repetindo as etapas 3 a 8.

9.  Para definir as suas configurações de teste, clique em **Avançar**.

    Um resumo da configuração de teste é exibido. Por exemplo, a mensagem a seguir é exibida
para as configurações padrão:

    `O teste ocorrerá: a cada 15 minutos em 3 locais simultaneamente para determinar se o teste excede o limite especificado.`

    O uso estimado e os testes estimados por mês são exibidos com base em sua
configuração de teste atual.

10. Na área de janela Configurações, clique em **Editar** para exibir as configurações atuais de seu teste. É possível atualizar as configurações a seguir:
    - **Intervalo** define com que frequência o teste é executado.
    - **Frequência de teste** determina se o teste é executado em todos os locais simultaneamente ou em um local diferente a cada intervalo. Selecione **Simultâneo** para executar o seu teste em todos os locais simultaneamente ou selecione **Escalonado** para
executar o seu teste de um local selecionado diferente a cada intervalo.
    - **Locais** determina os locais em que o teste será executado.

    Clique em **Salvar** para
concluir a configuração do seu teste.

11. Clique em **Terminar**. O painel {{site.data.keyword.prf_hubshort}}
exibe um resumo de seus testes totais, um mapa e uma tabela que representam a frequência e o local
de seus alertas, todos os testes sintéticos que estão associados ao seu aplicativo, uma tabela de suas atividades e um gráfico de linha que representa o tempo de resposta e a disponibilidade de seu aplicativo e outros websites. É possível criar mais
testes, conforme necessário.
12. É possível usar o serviço {{site.data.keyword.alertnotificationfull}} para configurar o recurso de monitoramento para enviar notificações quando um evento ocorre. Para
obter mais informações, veja [Ativando notificações](avmon_notifications.html "Configurar o recursode monitoramento para enviar notificações quando um evento ocorre.").


## Resultados
{: #avmon_getstarted_results}

Os resultados do teste são exibidos após o intervalo que você especificou no decorrer
de teste. O intervalo padrão é de 15 minutos.

Agora você está pronto para monitorar a disponibilidade de seus aplicativos da web. O
tempo de resposta e as informações de disponibilidade para seu aplicativo, website ou API REST
são exibidos em um gráfico de linha, juntamente com informações sobre atividades e testes recentes
na área de janela **Tempo de resposta e disponibilidade**.

Existem duas guias disponíveis para ajudar a conhecer os recursos do
{{site.data.keyword.prf_hubshort}}.

 - **Biblioteca de tutoriais de vídeo** - a biblioteca de tutoriais de
vídeo contém vídeos sobre como criar aplicativos Bluemix, criar testes de Monitoramento de
disponibilidade, criar scripts de teste com o Selenium IDE e enviar alertas para o Slack.
 - **Bem-vindo ao Monitoramento!** A guia Bem-vindo ao Monitoramento
destaca as áreas do painel e explica cada recurso do {{site.data.keyword.prf_hubshort}}.

Para abrir a guia, clique no ícone **Ajuda** ![Ícone Ajuda](images/help_icn_white_sml.jpg); em seguida, clique
na guia que você deseja visualizar.
