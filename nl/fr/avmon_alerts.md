---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Fréquence des alertes
{: #avmon_alert_freq}

Le panneau Fréquence des alertes contient une carte qui affiche les alertes les plus récentes. Les alertes sont regroupées par emplacement et répertoriées sur la table Alertes.
{: shortdesc}

## Carte Fréquence des alertes
{: #avmon_alertmap}

La carte Fréquence des alertes affiche un aperçu rapide de tous les points de présence de vos tests.

Utilisez la fonction de zoom pour agrandir une zone quelconque de la carte ou restaurer sa taille d'origine. Survolez chaque emplacement pour visualiser le nom de cet
emplacement et le nombre d'alertes de niveau avertissement ou critique à cet emplacement. Vous pouvez filtrer les alertes affichées sur la carte
en sélectionnant **Toutes**, **Ouvertes** ou **Fermées** dans la liste déroulante
**Alertes**.

![La carte Fréquence des alertes qui s'affiche effectue des tests à quatre points de présence.](images/alert_freq_map2.png)

### Emplacement hôte
L'icône **Emplacement hôte** ![Icône Emplacement hôte.](images/icn_host_crit_whtbackground30.jpg) représente l'emplacement du
serveur où
l'application que vous surveillez s'exécute. La couleur de l'icône **Emplacement hôte** représente la gravité d'alerte la plus récente à cet emplacement : Normal
![Icône Emplacement hôte avec un bord vert indiquant qu'aucune alerte n'existe à cet emplacement.](images/icn_host_normal_whtbckgrnd_30x38.jpg), Avertissement
![Icône Emplacement hôte avec un bord jaune indiquant qu'une alerte existe à cet emplacement.](images/icn_host_warning_whtbackground30.jpg) ou Critique
![Icône Emplacement hôte avec un bord rouge indiquant plusieurs alertes à cet emplacement.](images/icn_host_crit_whtbackground30.jpg). Une icône animée
**Emplacement hôte** indique que cet emplacement a le plus grand nombre d'alertes avec le plus haut niveau de gravité de tous les emplacements pour vos instances de test.

### Emplacements de point de présence (PoP)
Les icônes **Emplacement de point de présence** ![Icône Emplacement de point de présence.](images/icn_pop_normal_whtbckgrnd30x30.jpg)
indiquent les emplacements de point de présence de vos tests. La couleur de chaque icône **Emplacement de point de présence** représente la gravité de l'alerte la plus
récente à chaque emplacement : Normal ![Icône Emplacement de point de présence avec bord vert indiquant qu'aucune alerte n'existe àcet emplacement.](images/icn_pop_normal_whtbckgrnd30x30.jpg), Avertissement ![Icône Emplacement de point de présence avec bord jaune indiquant qu'une alerte existe à
cet emplacement.](images/icn_pop_warning_whtbckgrnd30x30.jpg) ou Critique ![Icône Emplacement de point de présence avec bord rouge indiquant plusieurs alertes à cet
emplacement.](images/icn_pop_crit_whtbckgrnd30x30.jpg). Une icône d'**emplacement POP** indique que cet emplacement a le plus grand nombre d'alertes avec le plus haut niveau de gravité de tous les

emplacements pour vos instances de test.

Ajoutez des emplacements de points de présence au test sélectionné en survolant une icône d'**emplacement de point de présence inactif**
![Emplacement de point de présence inactif](images/icn_avbl_pop.jpg) et en cliquant sur **Tester ici**. La page Tester le mode édition s'affiche
pour le test sélectionné. Vous pouvez sélectionner un test dans le menu déroulant **Test** du panneau **Temps de réponse** et **Disponibilité**.

<!--
Private PoP locations are represented by **Private PoP location** icons ![Private PoP location icon that indicates 2 alerts with one or more critical alerts at that location.](images/avmon_private_pop.png).
-->
### Nombre d'alertes
L'icône **Emplacement hôte** et les icônes **Emplacements de point de présence** affichent le nombre d'alertes ouvertes, fermées ou totales générées à
chaque emplacement. Les icônes Critique, Avertissement et Normal ![Icônes Critique, Avertissement et Normal.](images/fltr_alrts_tbl.jpg) affichent le nombre
d'alertes appartenant à chaque niveau de gravité pour vos emplacements.

### Tests ayant échoué
Les emplacements où les instances de test ont échoué sont indiqués par une icône **Emplacement hôte** ou **Emplacement de point de présence**
avec un bord cassé ![Icône Emplacement de point de présence avec bord rouge indiquant que 10 alertes ont été générées et qu'un ou plusieurs testsont échoué à cet emplacement.](images/avmon_pop_fail_32x33.png).


## Table Alertes
{: #avmon_alertstable}

Les alertes de tous les emplacements sont affichées dans une table.

![Table d'alertes affichant les alertes de tous les emplacements de point de présence.](images/alert_table.jpg)

Cette table contient les informations suivantes sur vos alertes :

-   **Gravité** indique si l'alerte est de niveau critique ou avertissement.
-   **Horodatage** indique l'heure de création de l'alerte.
-   **Description** récapitule les performances de votre instance de test.
-   **Déclenchée par** indique le nom du test qui a déclenché l'alerte.
-   **Emplacement** signale où s'est produit le problème.
-   **Etat** indique si l'alerte est ouverte ou fermée.

### Affichage des détails d'alerte
Chaque alerte dans la table comporte un lien vers le tableau de bord **Répartition**. Utilisez le tableau de bord Répartition pour identifier et résoudre le problème.

### Filtrage des alertes
Pour filtrer des alertes pour un emplacement particulier, cliquez sur une icône **Emplacement hôte** ou **Emplacement de point de présence** sur la
carte. Pour afficher les alertes de tous les emplacements, cliquez sur n'importe quel emplacement de la carte qui ne soit pas une icône **Emplacement hôte** ou
**Emplacement de point de présence**.

Pour filtrer les alertes par niveau de gravité dans la table, cliquez sur l'icône **Critique**, **Avertissement** ou **Normal**
![Icônes Critique, Avertissement et Normal.](images/fltr_alrts_tbl.jpg). Pour supprimer le filtre et
inclure les alertes de tous les niveaux de gravité dans la table, cliquez à nouveau sur l'icône que vous aviez sélectionnée.

### Modification des seuils d'alerte
Les alertes sont déclenchées par les seuils que vous spécifiez lorsque vous créez un test. Dans la plupart des cas, elles sont générées suite à des problèmes de disponibilité ou de lenteur
des temps de réponse. Pour modifier les paramètres de seuil, cliquez sur l'icône **Actions** ![Icône Actions.](images/actions_icn_white_smll.jpg) sur le test ayant généré
l'alerte dans le panneau Tests synthétiques puis cliquez sur **Editer**.
