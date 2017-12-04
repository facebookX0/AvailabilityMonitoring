---

copyright: years: 2015, 2017 lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Bloqueando e filtrando com a lista de desbloqueio e a lista de bloqueio
{: #avmon_filters}

Use a lista de desbloqueio e a lista de bloqueio para determinar para quais recursos enviar solicitações e quais recursos contribuem para as métricas e o status de seus testes de aplicativos. As listas de desbloqueio e as listas de bloqueio estão disponíveis somente para testes de página da web e de comportamento em script.
{: shortdesc}

Os campos **Lista de desbloqueio** e **Lista de bloqueio** definem os recursos que seu teste pode ou não pode acessar e os recursos que contribuem para as métricas e o status de seus testes. A lista de desbloqueio e a lista de bloqueio podem controlar quais dependências e recursos contribuem com os tempos de resposta de seus aplicativos da web testados, tais como métricas de terceiros. É possível configurar suas listas de desbloqueio e de bloqueio quando você criar um teste de página da web ou de comportamento em script.

É possível usar a **Lista de desbloqueio** para definir domínios e URLs permitidos; em seguida, use a **Lista de bloqueio** para bloquear elementos específicos de seus locais permitidos.

## Sintaxe

Use vírgulas (,) para separar itens na Lista de bloqueio e na Lista de desbloqueio. Use o símbolo curinga (\*) para filtrar elementos de cada URL ou domínio.

## Lista de desbloqueio

Inclua URLs ou domínios que você deseja incluir na solicitação e nos cálculos de métricas no campo Lista de desbloqueio. É possível listar até 10 itens em sua Lista de desbloqueio. Cada comprimento de item não pode exceder 200 caracteres. Todos os domínios e URLs que não corresponderem aos itens em sua Lista de desbloqueio serão bloqueados.

Por exemplo:
```
ibm.com, *developerworks*, *.s81c.com/*
```
{: codeblock}

## Lista de bloqueio

Inclua URLs ou domínios que você deseja bloquear das solicitações e dos cálculos de métricas no
campo Lista de bloqueio. É possível listar até 20 itens em sua Lista de bloqueio. Cada comprimento de item não pode exceder 200 caracteres.

Por exemplo:
```
*.profile.*.cloudfront.net/*.png
```
{: codeblock}

## Comportamento de filtragem e bloqueio

Os testes podem ter uma Lista de desbloqueio e uma Lista de bloqueio. Ao determinar quais locais
são permitidos ou bloqueados, a Lista de bloqueio sempre substituirá a Lista de desbloqueio. A tabela
a seguir exibe o comportamento de filtragem e bloqueio para todos os cenários que envolvem a Lista de
desbloqueio e a Lista de bloqueio.

<table id="avmon_whitelist_blacklist__table_gyg_vvp_fbb">
<caption>Tabela 1. Comportamento de filtragem e bloqueio para a Lista de desbloqueio e a Lista de bloqueio</caption>
<thead>
<tr>
<th>Lista de bloqueio</th>
<th>Lista de desbloqueio</th>
<th>Comportamento</th>
<th>Motivo</th>
</tr>
</thead>
<tbody>
<tr>
<td>Empty</td>
<td>Empty</td>
<td>Permitir acesso</td>
<td>Não foram inseridas regras de filtragem.</td>
</tr>
<tr>
<td>Empty</td>
<td>A URL não corresponde à entrada da lista</td>
<td>Bloquear acesso</td>
<td>A URL não está na lista de desbloqueio.</td>
</tr>
<tr>
<td>Empty</td>
<td>A URL corresponde à entrada da lista</td>
<td>Permitir acesso</td>
<td>A URL está na lista de desbloqueio. Nenhuma entrada da lista de bloqueio para bloquear o acesso.</td>
</tr>
<tr>
<td>A URL não corresponde à entrada da lista</td>
<td>Empty</td>
<td>Permitir acesso</td>
<td>A URL não está na lista de bloqueio. Nenhuma entrada da lista de desbloqueio para bloquear o acesso.</td>
</tr>
<tr>
<td>A URL corresponde à entrada da lista</td>
<td>Empty</td>
<td>Bloquear acesso</td>
<td>A URL está na lista de bloqueio.</td>
</tr>
<tr>
<td>A URL não corresponde à entrada da lista</td>
<td>A URL não corresponde à entrada da lista</td>
<td>Bloquear acesso</td>
<td>A URL não está na lista de desbloqueio.</td>
</tr>
<tr>
<td>A URL não corresponde à entrada da lista</td>
<td>A URL corresponde à entrada da lista</td>
<td>Permitir acesso</td>
<td>A URL está na lista de desbloqueio. A URL não está na lista de bloqueio.</td>
</tr>
<tr>
<td>A URL corresponde à entrada da lista</td>
<td>A URL não corresponde à entrada da lista</td>
<td>Bloquear acesso</td>
<td>A URL não está na lista de desbloqueio. A URL está na lista de bloqueio.</td>
</tr>
<tr>
<td>A URL corresponde à entrada da lista</td>
<td>A URL corresponde à entrada da lista</td>
<td>Bloquear acesso</td>
<td>A URL está na lista de bloqueio. A entrada da lista de bloqueio substitui a entrada da lista de desbloqueio.</td>
</tr>
</tbody>
</table>
