---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Testes sintéticos
{: #avmon_synth_tests}

Na área de janela Testes sintéticos, é possível criar, editar, excluir e visualizar
testes sintéticos que monitoram o desempenho e a disponibilidade de seus aplicativos. Os testes
são exibidos em uma visualização de lista ou de cartões na área de janela Testes sintéticos.
{: shortdesc}

![A área de janela Testes sintéticos.](images/syn_tests_pane.jpg)

Cada cartão de teste exibe informações sobre o teste:

- **Disponibilidade** exibe a disponibilidade de porcentagem do teste
nas últimas 24 horas.
- **Status** exibe o status atual do teste. O status pode ser Crítico, Aviso, Normal, Falha, Inativo ou Desconhecido.
- **Tempo de resposta** exibe o tempo médio de resposta do teste nas últimas 24 horas.

É possível monitorar três tipos diferentes de teste:

- Testes de **API de REST** relatam o tempo de resposta de uma chamada REST. Todos os formatos de solicitação de HTTP, tais
como GET, POST, PUT e DELETE são suportados.
- Testes de **Página da web** relatam o tempo de resposta para carregar o website na URL que você insere.
- Testes de **Comportamento em script** monitoram scripts do Selenium que
você cria para imitar as interações de um usuário com um website. Por exemplo, é possível criar um script Selenium que imita um usuário que está efetuando
login no seu aplicativo. Você executa esse script periodicamente para testar o desempenho de seu
aplicativo em resposta às ações do usuário que são automatizadas pelo script. É possível fazer upload de um script ou incluir um script a partir de um repositório GitHub. Para obter mais informações sobre como criar scripts Selenium, veja [Gravando scripts sintéticos](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(Abre em uma nova guia ou janela)"){: new_window}.

Para incluir outro teste, clique em **Incluir novo teste**.

Para parar, iniciar, excluir ou editar um teste sintético, clique no ícone **Ações** ![Ícone Ações](images/actions_icn_white_smll.jpg) e clique na ação que você desejar. Para visualizar os detalhes do teste, clique no teste.

Para visualizar o uso de cada teste sintético, clique no ícone **Custo** ![Ícone Custo](images/cost_icn_white_smll.jpg). Se você estiver inscrito
no plano pago, seu uso será exibido nos pontos de dados.
