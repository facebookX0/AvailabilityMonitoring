---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Création d'un test de page Web
{: #avmon_webpage_test}

Créez un test de page Web pour tester la disponibilité de votre application Web et surveiller la durée d'ouverture de cette page.
{: shortdesc}

## A propos de cette tâche
{: #avmon_webpage_about}

Les tests de page Web indiquent le temps de réponse de chargement de l'URL de votre application Web. Créez un test de page Web pour surveiller la disponibilité et le temps de réponse de votre application Web.

## Création et configuration de votre test de page Web
{: #avmon_create_web_test}

Pour créer un test de page Web, procédez comme suit.

1.  Si l'onglet Surveillance est affiché, cliquez sur **Ajouter un nouveau test**.

    ![Onglet Surveillance de votre application Cloud Foundry.](images/avmon_tab.png)

    Si vous affichez le tableau de bord {{site.data.keyword.prf_hubshort}}, cliquez sur **Ajouter un nouveau test** sur le panneau Tests synthétiques.

    ![Bouton Ajouter un nouveau test sur le panneau Tests synthétiques.](images/syn_tests_pane.jpg)

2.  Cliquez sur **Action unique** sur la page Configuration de la surveillance puis cliquez sur **Page Web** sur la page Action unique.
3.  Entrez un nom significatif pour votre test dans la zone **Nom**. Ajoutez une description de l'objectif du test dans la zone **Description**.
4.  Entrez l'**URL** de l'application Web à tester.
5.  Configurez les seuils d'alerte Avertissements et Critique pour votre test dans la section Validation de réponse. Editez le contenu des zones **Valeur** et **Unité** pour chaque ligne. Les temps de réponse qui dépassent les seuils Avertissement et Critique que vous avez définis déclenchent des alertes.

    ![Section Validation de réponse avec seuils Avertissement et Critiques par défaut.](images/avmon_webpage_resp_val.png)

6.  Utilisez la **Liste noire** et la **Liste blanche** pour spécifier vers quelles URL et vers quels domaines les demandes doivent être envoyées et pour indiquer quelles URL et quels domaines contribuent à la mesure et au statut de vos tests d'applications. Ajoutez les URL et les domaines que vous souhaitez inclure ou bloquer dans la **Liste blanche** et la **Liste noire**. Pour en savoir plus sur le blocage et le filtrage, voir [Blocage et filtrage avec la liste blanche et la liste noire](avmon_whitelist_blacklist.html#avmon_whitelist_blacklist "Utilisez la liste blanche et la liste noire pour déterminer à quelles ressources les demandes doivent être envoyées et quelles ressources contribuent aux mesures et au statut de vos tests d'application. Les listes blanches et les listes noires sont uniquement disponibles pour les tests de page Web et les tests du comportement contrôlé par scripts.").
7.  Cliquez sur la commande **Vérifier** pour créer votre test de page Web et déterminer si votre demande de test est valide.

    {{site.data.keyword.prf_hubshort}} détermine la validité du test en envoyant une demande GET à votre URL de test. La validation de la réponse n'a pas lieu pendant la vérification du test.

    Votre test validé s'affiche dans la table Eléments vérifiés. Vous pouvez ajouter d'autres adresses URL en répétant les étapes 3 à 7.

8.  Pour configurer vos paramètres de test, cliquez sur **Suivant**. Un récapitulatif de la configuration de test est affichée. Le message suivant, par exemple est affiché pour les paramètres par défaut :

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if test exceeds the specified threshold``.

    Une estimation de l'utilisation et du nombre de tests par mois est affichée compte tenu de votre configuration actuelle.

9.  Dans le panneau Paramètres, cliquez sur **Editer** pour afficher les paramètres en cours pour votre test. Vous pouvez mettre à jour les paramètres suivants :
    - **Intervalle** définit la fréquence avec laquelle le test s'exécute.
    - **Fréquence de test** détermine si votre test s'exécute depuis tous les emplacements simultanément ou d'un emplacement différent à chaque intervalle. Sélectionnez **Simultanée** pour exécuter votre test depuis tous les emplacements simultanément, ou **Echelonnée** pour l'exécuter depuis un emplacement différent à chaque intervalle.
    - **Emplacements** détermine l'emplacement où votre test s'exécutera.

    Cliquez sur **Sauvegarder** pour finir de configurer votre test.

10. Cliquez sur **Terminer**. Le tableau de bord {{site.data.keyword.prf_hubshort}} affiche un récapitulatif de tous vos tests, une carte et une table qui affiche le niveau de gravité et l'emplacement de vos alertes, tous les tests synthétiques associés à votre application, une table de vos activités et un graphique linéaire qui présente le temps de réponse et la disponibilité de votre application et d'autres sites Web.
