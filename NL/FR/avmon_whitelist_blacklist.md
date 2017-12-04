---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Blocage et filtrage à l'aide de la liste blanche et de la liste noire
{: #avmon_filters}

Utilisez la liste blanche et la liste noire pour déterminer vers quelles ressources les demandes doivent être envoyées et quelles ressources contribuent aux métriques et au statut de vos
tests d'applications. Les listes blanches et les listes noires sont uniquement disponibles pour les tests de page Web et les tests de comportement contrôlés par script.
{: shortdesc}

Les zones **Liste blanche** et **Liste noire** définissent les ressources auxquelles votre test peut ou ne peut pas accéder et les ressources qui
contribuent aux métriques et au statut de vos tests. La liste blanche et la liste noire peuvent contrôler quelles dépendances et ressources contribuent aux temps de réponse de vos applications
Web testées, comme par exemple des métriques tierces. Vous pouvez configurer votre liste blanche et votre liste noire lorsque vous créez un test de page Web ou un test de comportement
contrôlé par script.

Vous pouvez utiliser la **liste blanche** pour définir les domaines et les URL autorisés puis utiliser la **liste noire** pour bloquer des éléments
spécifiques de vos emplacements autorisés.

## Syntaxe

Utilisez des virgules (,) pour séparer les éléments de la liste blanche et de la liste noire. Utilisez le caractère générique (\*) pour filtrer les éléments de chaque URL ou de chaque
domaine.

## Liste blanche

Ajoutez les URL ou les domaines que vous souhaitez inclure dans les calculs des métriques et des demandes dans la zone Liste blanche. Vous pouvez répertorier jusqu'à 10 éléments dans
votre liste blanche. La longueur de chaque élément ne peut pas être supérieure à 200 caractères. Tous les domaines et toutes les URL qui ne correspondent pas aux éléments de votre liste blanche
sont bloqués.

Par exemple :
```
ibm.com, *developerworks*, *.s81c.com/*
```
{: codeblock}

## Liste noire

Ajoutez les URL ou les domaines que vous ne souhaitez pas inclure dans les calculs des métriques et des demandes dans la zone Liste noire. Vous pouvez répertorier jusqu'à 20 éléments dans
votre liste noire. La longueur de chaque élément ne peut pas être supérieure à 200 caractères. 

Par exemple :
```
*.profile.*.cloudfront.net/*.png
```
{: codeblock}

## Comportements de filtrage et de blocage

Les tests peuvent comporter à la fois une liste blanche et une liste noire. Lorsque vous déterminez quels emplacements sont autorisés ou bloqués, la liste noire a toujours priorité sur
la liste blanche. Le tableau suivant affiche les comportements de filtrage et de blocage de tous les scénarios impliquant la liste blanche et la liste noire.

<table id="avmon_whitelist_blacklist__table_gyg_vvp_fbb">
<caption>Tableau 1. Comportements de filtrage et de blocage de la liste blanche et de la liste noire</caption>
<thead>
<tr>
<th>Liste noire</th>
<th>Liste blanche</th>
<th>Comportement</th>
<th>Raison</th>
</tr>
</thead>
<tbody>
<tr>
<td>Vide</td>
<td>Vide</td>
<td>Autoriser l'accès</td>
<td>Aucune règle de filtrage entrée.</td>
</tr>
<tr>
<td>Vide</td>
<td>L'URL ne correspond pas à l'entrée de la liste</td>
<td>Bloquer l'accès</td>
<td>L'URL ne figure pas dans la liste blanche.</td>
</tr>
<tr>
<td>Vide</td>
<td>L'URL correspond à l'entrée de la liste</td>
<td>Autoriser l'accès</td>
<td>L'URL figure dans la liste blanche. Aucune entrée de liste noire pour bloquer l'accès.</td>
</tr>
<tr>
<td>L'URL ne correspond pas à l'entrée de la liste</td>
<td>Vide</td>
<td>Autoriser l'accès</td>
<td>L'URL ne figure pas dans la liste noire. Aucune entrée de liste blanche pour bloquer l'accès.</td>
</tr>
<tr>
<td>L'URL correspond à l'entrée de la liste</td>
<td>Vide</td>
<td>Bloquer l'accès</td>
<td>L'URL figure dans la liste noire.</td>
</tr>
<tr>
<td>L'URL ne correspond pas à l'entrée de la liste</td>
<td>L'URL ne correspond pas à l'entrée de la liste</td>
<td>Bloquer l'accès</td>
<td>L'URL ne figure pas dans la liste blanche.</td>
</tr>
<tr>
<td>L'URL ne correspond pas à l'entrée de la liste</td>
<td>L'URL correspond à l'entrée de la liste</td>
<td>Autoriser l'accès</td>
<td>L'URL figure dans la liste blanche. L'URL ne figure pas dans la liste noire. </td>
</tr>
<tr>
<td>L'URL correspond à l'entrée de la liste</td>
<td>L'URL ne correspond pas à l'entrée de la liste</td>
<td>Bloquer l'accès</td>
<td>L'URL ne figure pas dans la liste blanche. L'URL figure dans la liste noire.</td>
</tr>
<tr>
<td>L'URL correspond à l'entrée de la liste</td>
<td>L'URL correspond à l'entrée de la liste</td>
<td>Bloquer l'accès</td>
<td>L'URL figure dans la liste noire. L'entrée de la liste noire a priorité sur l'entrée de la liste blanche.</td>
</tr>
</tbody>
</table>
