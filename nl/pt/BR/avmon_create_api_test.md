---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Criando um teste de API de REST
{: #avmon_rest_api}

Crie um teste de API REST para testar o tempo de resposta e a disponibilidade de seu aplicativo da web usando os métodos de HTTP a seguir: GET, POST, PUT e DELETE
{: shortdesc}

Use testes de API REST para monitorar a disponibilidade e o desempenho de seu aplicativo da web e outras URLs em resposta a chamadas REST.

Para criar um teste de API de REST, conclua as etapas a seguir.

1.  Se você estiver visualizando a guia **Monitoramento** para seu aplicativo Cloud Foundry, clique em **Incluir novo teste**.

    ![A guia Monitoramento do aplicativo Cloud Foundry.](images/avmon_tab.png)

    Se você estiver visualizando o painel {{site.data.keyword.prf_hubshort}}, clique em **Incluir novo teste** na área de janela Testes sintéticos.

    ![O botão Incluir novo teste na área de janela Testes sintéticos.](images/syn_tests_pane.jpg)

2.  Clique em **Ação** na página Configuração de monitoramento; em seguida, clique em **API REST** na página Ação única.
3.  Insira um nome significativo para o seu teste no campo **Nome**. Inclua uma descrição do propósito de seu teste no campo **Descrição**.
4.  Na seção Solicitação, selecione o tipo de método na lista **Método** e insira uma **URL** que deseja testar com esse método. É possível escolher **GET**, **PUT**, **POST** ou **DELETE**. Se você escolher o método PUT ou POST, será possível inserir o conteúdo do corpo para testar no campo **Solicitar corpo (opcional)**.

    Por exemplo, o teste de API de REST a seguir usa o método POST para solicitar que seu aplicativo da web aceite dados, além de testar a disponibilidade e o desempenho desse aplicativo da web.

    ![Exemplo de um teste de API de REST que usa o método de solicitação POST.](images/avmon_restapi_post.png)

5.  É possível configurar o seu teste para incluir um determinado cabeçalho e valor. Insira um nome de cabeçalho e valor de cabeçalho nos campos de **Cabeçalho**.

    Se o aplicativo da web que você deseja testar exigir um login de usuário e uma senha, insira "Autorização" no campo **Nome do cabeçalho**. Insira a palavra "Básico", um caractere de espaço e o valor codificado base64 de seu nome de usuário:senha no campo **Valor do cabeçalho**.

    Por exemplo, se o seu nome for Aladdin e sua senha for OpenSesame, então, insira a palavra "Básico", um caractere de espaço e o valor codificado base64 para Aladdin:OpenSesame no campo **Valor do cabeçalho**.

    ![Campos de cabeçalho que representando credenciais de autorização de teste em base64.](images/avmon_apitest_auth.png)

6.  Configure os limites de alerta de aviso e de alerta crítico de seu teste na seção Validação de resposta. Edite o **Valor** e a **Unidade** para cada linha. Os tempos de resposta que excedem o seu aviso e os limites críticos acionam alertas.

    ![Seção Validação de resposta com limite de aviso padrão e limite crítico padrão.](images/avmon_restapi_resp_val.png)

7.  Clique em **Incluir condição** para definir e incluir condições de validação de resposta customizadas. As condições de validação de resposta customizadas são avaliadas em conjunto para gerar um alerta. É possível definir e incluir até seis condições customizadas para o seu teste.

    Em {{site.data.keyword.prf_hubshort}}, cada teste pode gerar até um total de três alertas. Seu teste relata o alerta com a maior severidade até que todas as condições que causem alertas sejam resolvidas. Para obter mais informações, veja [Geração de alertas em Monitoramento de disponibilidade](avmon_alert_desc.html "Em Monitoramento de disponibilidade, os testes podem gerar um total de até três alertas. Seu teste relatará o alerta com a maior severidade até que a condição que está causando o alerta seja resolvida.")
    {: tip}

    É possível validar os dados a seguir:

    - **Código de resposta do cabeçalho**. Selecione **Código de resposta de cabeçalho** para testar um código de resposta ou um intervalo de códigos de resposta de HTTP.
    - **Propriedade do cabeçalho**. Selecione **Propriedade de cabeçalho** para testar para uma propriedade e valor específicos do campo de cabeçalho de HTTP.
    - **Json de corpo**. Selecione **JSON de corpo** para testar para uma propriedade específica de um corpo do JSON.

      Para cada condição, insira uma propriedade para a qual testar no campo de **Destino** e um valor a ser testado no campo de **Valor**. Selecione um operador no menu suspenso **Operação**. Finalmente, escolha uma severidade do alerta de **Aviso** ou **Crítico** para sua condição.

    Os valores numéricos que você insere no campo de **Valor** são tratados como números, e não sequências, por padrão. Ao inserir um **Valor** para uma condição de validação de resposta, use aspas "" para distinguir entre uma sequência e um número. Por exemplo, para testar para a sequência 123, insira "123" no campo Valor. Para verificar o número 400, insira 400 sem quaisquer aspas. {: tip}

    ![Condições de validação de resposta para um teste de API de REST](images/avmon_restapi_resp_val2.png)

8.  Clique em **Verificar** para criar o seu teste de API de REST e para determinar se a sua solicitação de teste é válida.

    O {{site.data.keyword.prf_hubshort}} determina a validade de teste usando o método HTTP selecionado e qualquer cabeçalho de solicitação que você tenha definido para o teste. Nenhuma validação de resposta ocorre durante a verificação de teste.

    Seu teste validado será exibido na tabela Itens verificados. É possível incluir mais URLs repetindo as etapas 3 a 8.

9.  Para definir as suas configurações de teste, clique em Avançar.

    Um resumo da configuração de teste é exibido. Por exemplo, a mensagem a seguir é exibida para as configurações padrão:

    ``O teste ocorrerá: a cada 15 minutos em 3 locais simultaneamente para determinar se o teste excede o limite especificado.``

    O uso estimado e número estimado de testes por mês são exibidos com base em sua configuração de teste atual.

10. Na área de janela Configurações, clique em **Editar** para exibir as configurações atuais de seu teste.

    É possível mudar o intervalo e a frequência dos testes e os locais dos quais os testes são enviados.

    ![Área de janela Configurações de teste exibindo as configurações padrão para um teste.](images/avmon_settings.png)

    Selecione **Simultâneo** para executar o seu teste em todos os locais simultaneamente ou selecione **Escalonado** para executar o seu teste de um local selecionado diferente a cada intervalo. Clique em **Salvar** para concluir a configuração do seu teste.

11. Clique em **Terminar**. O painel {{site.data.keyword.prf_hubshort}} exibe um resumo de todos os seus testes, um mapa e uma tabela que exibem a severidade e o local de seus alertas, todos os testes sintéticos que estão associados ao aplicativo, uma tabela de suas atividades e um gráfico de linhas que descreve o tempo de resposta e a disponibilidade de seu aplicativo e outros websites.
