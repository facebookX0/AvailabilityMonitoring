---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Frequência do alerta
{: #avmon_alert_freq}

O painel Frequência de alertas contém um mapa que exibe os alertas mais recentes. Os alertas são agrupados por local e listados na tabela Alertas.
{: shortdesc}

## Mapa de frequência de alerta
{: #avmon_alertmap}

O mapa Frequência de alertas exibe informações em uma visão rápida para todos os pontos de presença (PoPs) para os seus testes.

Use a função de zoom para ampliar qualquer área do mapa ou para restaurá-lo para o seu tamanho original. Passe o mouse sobre cada local para visualizar o nome desse local e o número de avisos e alertas críticos nesse local. É possível filtrar os alertas que são exibidos no mapa selecionando **Todos**, **Abertos** ou **Fechados** na lista suspensa **Alertas**.

![Mapa Frequência de alertas que exibe testes em quatro pontos de presença.](images/alert_freq_map2.png)

### Local do host
O ícone **Local do host** ![Ícone Local do host.](images/icn_host_crit_whtbackground30.jpg) representa o local do servidor no qual o aplicativo que você está monitorando está em execução. A cor do ícone **Local do host** representa a severidade do alerta mais recente nesse local: Normal ![Ícone de local do host com borda verde que indica que não há alertas nesse local.](images/icn_host_normal_whtbckgrnd_30x38.jpg), Aviso ![Ícone de local do host com borda amarela que indica um alerta nesse local.](images/icn_host_warning_whtbackground30.jpg) ou Crítico ![Ícone de local do host com borda vermelha que indica um alerta nesse local.](images/icn_host_crit_whtbackground30.jpg). Um ícone **Local do host** animado indica que esse local tem a maioria dos alertas com o nível mais alto de severidade de todos os locais para as suas instâncias de teste.

### Locais de PoP
Ícones de **Local de PoP** ![Ícone de local de PoP.](images/icn_pop_normal_whtbckgrnd30x30.jpg) indicam os locais de PoP para seus testes. A cor de cada ícone de **Local de PoP** representa a severidade do alerta mais recente em cada local: Normal ![Ícone de local do PoP com borda verde que indica que não há alertas nesse local.](images/icn_pop_normal_whtbckgrnd30x30.jpg), Aviso ![Ícone de local PoP com borda amarela que indica um alerta nesse local.](images/icn_pop_warning_whtbckgrnd30x30.jpg) ou Crítico ![Ícone de local PoP com borda vermelha que indica um alerta nesse local.](images/icn_pop_crit_whtbckgrnd30x30.jpg). Um ícone de **Local de PoP** animado indica que esse local tem a maioria dos alertas com o nível mais alto de severidade de todos os locais para as suas instâncias de teste.

Inclua locais de PoP em seu teste selecionado passando o mouse sobre um ícone **Local de PoP inativo** ![Local de PoP inativo](images/icn_avbl_pop.jpg) e clicando em **Testar aqui**. A página Modo de edição de teste é exibida para seu teste selecionado. É possível selecionar um teste no menu suspenso **Teste** na área de janela **Tempo de resposta** e **Disponibilidade**.

<!--
Private PoP locations are represented by **Private PoP location** icons ![Private PoP location icon that indicates 2 alerts with one or more critical alerts at that location.](images/avmon_private_pop.png).
-->
### Número de alertas
O ícone **Local do host** e os ícones **Local de PoP** exibem o número de alertas abertos e fechados ou todos que são gerados em cada local. Os ícones Crítico, Aviso e Normal ![Ícones Crítico, Aviso e Normal.](images/fltr_alrts_tbl.jpg) exibem o número de alertas de cada severidade para seus locais.

### Testes com falha
Os cocais em que as instâncias de teste com falha ocorreram são indicados por um ícone **Local de host** ou por um ícone **Local de PoP** com uma borda quebrada ![Ícone de local de PoP com borda vermelha que indica 10 alertas e um ou mais testes com falha nesse local.](images/avmon_pop_fail_32x33.png)

## Tabela Alertas
{: #avmon_alertstable}

Os alertas para todos os locais são exibidos em uma tabela.

![Tabela de Alertas que mostra alertas para todos os locais de PoP.](images/alert_table.jpg)

A tabela exibe as informações a seguir sobre seus alertas:

-   **Severidade** descreve o alerta como crítico ou aviso.
-   **Registro de data e hora** mostra o horário em que o alerta é criado.
-   **Descrição** resume o desempenho de sua instância de teste.
-   **Acionado por** mostra o nome do teste que acionou o alerta.
-   **Local** indica onde o problema ocorreu.
-   **Estado** mostra se o alerta está aberto ou fechado.

### Visualizando Detalhes de Alerta
Cada alerta na tabela contém um link para o painel **Detalhamento**. Use o painel Detalhamento para ajudá-lo a resolver o problema.

### Filtrando alertas
Para filtrar alertas para um local específico, clique em um ícone **Local de host** ou no ícone **Local de PoP** no mapa. Para mostrar alertas para todos os locais, clique em qualquer lugar no mapa que não seja um ícone **Local de host** nem um ícone **Local de PoP**.

Para filtrar os alertas na tabela por severidade, clique no ícone **Crítico**, **Aviso** ou **Normal** ![Ícones Crítico, Aviso e Normal.](images/fltr_alrts_tbl.jpg). Para remover o filtro e incluir alertas de cada severidade na tabela, clique novamente no ícone selecionado.

### Mudando os limites de alerta
Os alertas são acionados por limites que você especifica ao criar um teste. Na maioria dos casos, eles são gerados devido a falhas de disponibilidade ou tempos de resposta lentos. Para mudar as configurações de limite, clique no ícone **Ações** ![Ícone Ações.](images/actions_icn_white_smll.jpg) no teste que gerou o alerta na área de janela Testes sintéticos e clique em **Editar**.
