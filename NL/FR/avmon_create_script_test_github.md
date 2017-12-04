---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Création d'un test de script depuis un script figurant dans un référentiel GitHub
{: #avmon_git_script_test}

Créez un test de script depuis un script Selenium qui est stocké dans votre référentiel GitHub. Vous pouvez activer votre test de script pour procéder à une synchronisation continue de tous les changements que vous effectuez dans le script Selenium de votre référentiel GitHub.
{: shortdesc}

## Avant de commencer
{: #avmon_git_prereq}

Les tests de script nécessitent des scripts Selenium pour fonctionner. Pour créer un test de script, vous devez d'abord créer un script Selenium. Pour en savoir plus sur la création des scripts Selenium, voir [Enregistrement des scripts synthétiques](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(ouvre un nouvel onglet ou une fenêtre)"){: new_window}.

Pour créer des tests de script depuis des scripts Selenium qui sont stockés dans un référentiel GitHub, vous devez effectuer les étapes ci-après :

-   Activez {{site.data.keyword.contdelivery_full}} pour votre application. Pour obtenir plus d'informations, voir [Continuous Delivery](../ContinuousDelivery/index.html "(ouvre un nouvel onglet ou une fenêtre)"){: new_window}.
-   Autorisez {{site.data.keyword.Bluemix_notm}} à accéder à GitHub en tant qu'élément de votre chaîne d'outils. Pour obtenir plus d'informations, voir [Configuration de GitHub](../ContinuousDelivery/toolchains_integrations.html#github "(ouvre un nouvel onglet ou une fenêtre)"){: new_window}.

## A propos de cette tâche
{: #avmon_git_about}

Si vous activez {{site.data.keyword.contdelivery_short}} pour votre application, vous pouvez créer un test de script qui se synchronise avec un script Selenium dans votre référentiel GitHub. Si vous créez un script Selenium qui imite un utilisateur de votre application, vous pouvez ensuite exécuter un test de script périodiquement pour tester la performance de votre application en réponse à des actions simulées d'utilisateurs.

## Création d'un test utilisant un script GitHub
{: #avmon_git_create_test}

Pour créer un test de script, procédez comme suit.

1.  Si l'onglet Surveillance est affiché, cliquez sur **Ajouter un nouveau test**.

    ![Onglet Surveillance de votre application Cloud Foundry.](images/avmon_tab.png)

    Si le tableau de bord {{site.data.keyword.prf_hubshort}} est affiché, cliquez sur **Ajouter un nouveau test** sur le panneau Tests synthétiques.

    ![Bouton Ajouter un nouveau test sur le panneau Tests synthétiques.](images/syn_tests_pane.jpg)

2.  Cliquez sur **Comportement contrôlé par scripts** sur la page Configuration de la surveillance. La page Configuration du comportement contrôlé par scripts s'affiche. Cliquez sur **Référentiel Git**.
3.  Entrez un nom significatif pour votre test dans la zone **Nom**. Ajoutez une description de l'objectif du test dans la zone **Description**.
4.  Sélectionnez un référentiel GitHub disponible et entrez le chemin d'accès au script dans le référentiel choisi.
5.  Afin de garantir que le test utilise systématiquement la version la plus récente de votre script Selenium de votre **référentiel Git**, sélectionnez **Script de synchronisation automatique avec le pipeline de livraison**.
6.  Utilisez la **Liste noire** et la **Liste blanche** pour spécifier vers quelles URL et vers quels domaines les demandes doivent être envoyées et pour indiquer quelles URL et quels domaines contribuent à la mesure et au statut de vos tests d'applications. Ajoutez les URL et les domaines que vous souhaitez inclure ou bloquer dans la **Liste blanche** et la **Liste noire**. Pour en savoir plus sur le blocage et le filtrage, voir [Blocage et filtrage avec la liste blanche et la liste noire](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "Utilisez la liste blanche et la liste noire pour déterminer à quelles ressources les demandes doivent être envoyées et quelles ressources contribuent aux mesures et au statut de vos tests d'application. Les listes blanches et les listes noires sont uniquement disponibles pour les tests de page Web et les tests du comportement contrôlé par scripts.").
7.  Pour configurer vos paramètres de test, cliquez sur **Suivant**. Un récapitulatif de la configuration de test s'affiche. Le message suivant, par exemple est affiché pour les paramètres par défaut :

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds 5 seconds``.

    Une estimation de l'utilisation et du nombre de tests par mois est affichée compte tenu de votre configuration actuelle.

8.  Dans le panneau Paramètres, cliquez sur **Editer** pour afficher les paramètres en cours pour votre test. Vous pouvez mettre à jour les paramètres suivants :
    - **Intervalle** définit la fréquence avec laquelle le test s'exécute.
    - **Fréquence de test** détermine si votre test s'exécute depuis tous les emplacements simultanément ou d'un emplacement différent à chaque intervalle. Sélectionnez **Simultanée** pour exécuter votre test depuis tous les emplacements simultanément, ou **Echelonnée** pour l'exécuter depuis un emplacement différent à chaque intervalle.
    - **Seuil critique** définit le temps de réponse pour les alertes critiques pour le test.
    - **Seuil d'avertissement** définit le temps de réponse pour les alertes d'avertissement pour le test.
    - **Emplacements** détermine l'emplacement où votre test s'exécutera.

    Si nécessaire, vous pouvez entrer les valeurs des variables qui sont définies dans votre script de test. Ainsi, si votre script requiert un nom et un mot de passe pour se connecter à un site Web, vous pouvez entrer les valeurs pour ces variables. Vous pouvez définir différentes valeurs pour vos variables dans divers emplacements de la table **Variables de script**.

    Cliquez sur **Sauvegarder** pour finir de configurer votre test.

9.  Cliquez sur **Terminer**. Le tableau de bord {{site.data.keyword.prf_hubshort}} affiche un récapitulatif de tous vos tests, une carte et une table qui affiche le niveau de gravité et l'emplacement de vos alertes, tous les tests synthétiques associés à votre application, une table de vos activités et un graphique linéaire qui présente le temps de réponse et la disponibilité de votre application et d'autres sites Web.
