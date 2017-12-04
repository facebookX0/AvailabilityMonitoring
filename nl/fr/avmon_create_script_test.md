---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Création d'un test de script depuis un script téléchargé
{: #avmon_upload_script_test}

Téléchargez un script Selenium pour créer un test de script qui teste la disponibilité et les performances de votre application Web en réponse au comportement simulé de l'utilisateur.
{: shortdesc}

## Avant de commencer
{: #avmon_script_prereq}

Les tests de script nécessitent des scripts Selenium pour fonctionner. Pour créer un test de script, vous devez d'abord créer un script Selenium. Pour en savoir plus sur la création des scripts Selenium, voir [Enregistrement des scripts synthétiques](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(ouvre un nouvel onglet ou une fenêtre)"){: new_window}.

## A propos de cette tâche
{: #avmon_script_about}

Créez un test de script permettant de surveiller un script Selenium qui simule les interactions de vos utilisateurs avec votre application Web. Si vous créez un script Selenium imitant un
utilisateur qui se connecte à votre application, vous pouvez alors exécuter périodiquement un test de script pour tester les performances de votre application en réponse aux actions utilisateurs
simulées. 

## Création d'un test avec un script téléchargé
{: #avmon_script_create_test}

Pour créer un test de script, procédez comme suit.

1.  Si l'onglet Surveillance est affiché, cliquez sur **Ajouter un nouveau test**.

    ![Onglet Surveillance de votre application Cloud Foundry.](images/avmon_tab.png)

    Si vous affichez le tableau de bord {{site.data.keyword.prf_hubshort}}, cliquez sur **Ajouter un nouveau test** sur le panneau Tests synthétiques.

    ![Bouton Ajouter un nouveau test sur le panneau Tests synthétiques.](images/syn_tests_pane.jpg)

2.  Cliquez sur **Comportement contrôlé par scripts** sur la page Configuration de la surveillance. La page Configuration du comportement contrôlé par scripts s'affiche. Cliquez sur **Importer le fichier**.

    Pour éditer à nouveau ce test ultérieurement, vous pouvez télécharger le fichier script que vous aviez transféré. Cliquez sur l'icône **Télécharger** ![Icône Télécharger](images/download_icn_white_smll.jpg) pour télécharger votre script.

3.  Entrez un nom significatif pour votre test dans la zone **Nom**. Ajoutez une description de l'objectif du test dans la zone **Description**.
4.  Cliquez sur **Parcourir** pour localiser et télécharger un fichier de script.
5.  Utilisez la **Liste noire** et la **Liste blanche** pour spécifier vers quelles URL et vers quels domaines les demandes doivent être envoyées et pour indiquer quelles URL et quels domaines contribuent à la mesure et au statut de vos tests d'applications. Ajoutez les URL et les domaines que vous souhaitez inclure ou bloquer dans la **Liste blanche** et la **Liste noire**. Pour en savoir plus sur le blocage et le filtrage, voir [Blocage et filtrage avec la liste blanche et la liste noire](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "Utilisez la liste blanche et la liste noire pour déterminer à quelles ressources les demandes doivent être envoyées et quelles ressources contribuent aux mesures et au statut de vos tests d'application. Les listes blanches et les listes noires sont uniquement disponibles pour les tests de page Web et les tests du comportement contrôlé par scripts.").
6.  Pour configurer vos paramètres de test, cliquez sur **Suivant**. Un récapitulatif de la configuration de test est affichée. Le message suivant, par exemple est affiché pour les paramètres par défaut :

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds 5 seconds``.

    Une estimation de l'utilisation et du nombre de tests par mois est affichée compte tenu de votre configuration actuelle.

7.  Dans le panneau Paramètres, cliquez sur **Editer** pour afficher les paramètres en cours pour votre test. Vous pouvez mettre à jour les paramètres suivants :
    - **Intervalle** définit la fréquence avec laquelle le test s'exécute.
    - **Fréquence de test** détermine si votre test s'exécute depuis tous les emplacements simultanément ou d'un emplacement différent à chaque intervalle. Sélectionnez **Simultanée** pour exécuter votre test depuis tous les emplacements simultanément, ou **Echelonnée** pour l'exécuter depuis un emplacement différent à chaque intervalle.
    - **Seuil critique** définit le temps de réponse pour les alertes critiques pour le test.
    - **Seuil d'avertissement** définit le temps de réponse pour les alertes d'avertissement pour le test.
    - **Emplacements** détermine l'emplacement où votre test s'exécutera.

    Si nécessaire, vous pouvez entrer les valeurs des variables qui sont définies dans votre script de test. Ainsi, si votre script requiert un nom et un mot de passe pour se connecter à un site Web, vous pouvez entrer les valeurs pour ces variables. Vous pouvez définir différentes valeurs pour vos variables dans divers emplacements de la table **Variables de script**.

    Cliquez sur **Sauvegarder** pour finir de configurer votre test.

8.  Cliquez sur **Terminer**. Le tableau de bord {{site.data.keyword.prf_hubshort}} affiche un récapitulatif de tous vos tests, une carte et une table qui affiche le niveau de gravité et l'emplacement de vos alertes, tous les tests synthétiques associés à votre application, une table de vos activités et un graphique linéaire qui présente le temps de réponse et la disponibilité de votre application et d'autres sites Web.
