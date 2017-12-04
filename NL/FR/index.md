---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Initiation à Availability Monitoring
{: #avmon_gettingstarted}

Utilisez {{site.data.keyword.prf_hublong}} pour exécuter des tests de performance simulés depuis tous les emplacements possibles à travers le monde, à toute heure du jour ou de la nuit, afin de détecter, isoler et diagnostiquer proactivement les problèmes de performance avant qu'ils n'affectent vos utilisateurs. Vous pouvez ainsi vous assurer que vos applications sont disponibles et répondent aux objectifs de temps de réponse quand vous déployez des mises à jour en continu. Configurez
des collecteurs de données pour que vos applications collectent les données de transaction des utilisateurs. Utilisez ces données dans {{site.data.keyword.prf_hubshort}} pour surveiller
la réactivité et la capacité de traitement de votre application.
{: shortdesc}

## A propos de cette tâche
{: #avmon_start_about}

{{site.data.keyword.prf_hubshort}} est disponible en tant que service dans le domaine DevOps du catalogue {{site.data.keyword.Bluemix_notm}}. Il est aussi disponible par défaut dans le tableau de bord Application de l'onglet **Surveillance**. 
La surveillance de la disponibilité et des performances de votre application peut être démarrée immédiatement. Lorsque vous liez {{site.data.keyword.prf_hubshort}} à
votre application, un test synthétique est automatiquement créé pour surveiller l'URL de l'application principale par défaut.

## Création d'un test de page Web
{: #avmon_start_procedure}

Effectuez la procédure suivante pour ouvrir {{site.data.keyword.prf_hubshort}} pour votre application, pour créer un test de page Web afin de surveiller une autre adresse URL et pour
configurer des alertes de notification pour vos tests.

1.  Si vous possédez une application Cloud Foundry que vous souhaitez surveiller, cliquez sur le nom de l'application dans la table **Toutes les applications** sur
le tableau de bord **Applications**. Si vous n'avez pas encore d'application, créez-la. La carte de l'application s'ouvre automatiquement. Les applications Cloud Foundry sont
automatiquement liées à {{site.data.keyword.prf_hubshort}} lorsque vous cliquez sur l'onglet Surveillance.
2.  Pour ouvrir {{site.data.keyword.prf_hubshort}}, cliquez sur l'onglet
**Surveillance**. L'onglet **Surveillance** affiche trois jauges
qui présentent la **Disponibilité moyenne du test** lors des dernières 24 heures,
le **Statut actuel du test** et l'**Utilisation** de votre allocation de plan actuel. Cliquez sur **Ajouter un nouveau test** pour configurer un test de surveillance.

    ![Onglet Availability Monitoring](images/avmon_tab.png)

    L'URL de l'application principale est surveillée par défaut. Tous les autres services et URL que vous surveillez peuvent se trouver à l'intérieur ou l'extérieur de Bluemix et n'ont pas besoin d'être liés à l'application Cloud Foundry.

3.  Cliquez sur **Action unique** sur la page Configuration de la surveillance puis cliquez sur **Page Web** sur la page Action unique.
4.  Entrez un nom significatif pour votre test dans la zone **Nom**. Ajoutez une description de l'objectif du test dans la zone **Description**.
5.  Entrez l'**URL** de l'application Web à tester.
6.  Configurez les seuils d'alerte Avertissement et Critique pour votre test dans la section Validation de réponse. Editez le contenu des zones **Valeur** et **Unité** pour chaque ligne. Les temps de réponse qui dépassent les seuils Avertissement et Critique que vous avez définis déclenchent des alertes.

    ![Section Validation de réponse avec seuils Avertissement et Critique par défaut.](images/avmon_webpage_resp_val.png)

7.  Utilisez la **Liste noire** et la **Liste blanche** pour spécifier vers quelles URL et vers quels domaines les demandes doivent être envoyées et pour indiquer quelles URL et quels domaines contribuent à la mesure et au statut de vos tests d'applications. Ajoutez les URL et les domaines que vous souhaitez inclure ou bloquer dans la **Liste blanche** et la **Liste noire**. Pour en savoir plus sur le blocage et le filtrage, voir [Blocage et filtrage avec la liste blanche et la liste noire](avmon_whitelist_blacklist.html "Utilisez la liste blanche et la liste noire pour déterminer à quelles ressources les demandes doivent être envoyées et quelles ressources contribuent aux mesures et au statut de vos tests d'application. Les listes blanches et les listes noires sont uniquement disponibles pour les tests de page Web et les tests du comportement contrôlé par scripts.").
8.  Cliquez sur la commande **Vérifier** pour créer votre test de page Web et déterminer si votre demande de test est valide.

    {{site.data.keyword.prf_hubshort}} détermine la validité du test en envoyant une demande GET à votre URL de test. La validation de la réponse n'a pas lieu pendant la vérification du test.

    Votre test validé s'affiche dans la table Eléments vérifiés. Vous pouvez ajouter d'autres adresses URL en répétant les étapes 3 à 8.

9.  Pour configurer vos paramètres de test, cliquez sur **Suivant**.

    Un récapitulatif de la configuration de test est affichée. Le message suivant, par exemple est affiché pour les paramètres par défaut :

    `Test will occur: Every 15 minutes from 3 locations simultaneously to determine if
test exceeds the specified threshold.`

    L'utilisation estimée et le nombre de tests estimés par mois s'affichent en fonction de votre configuration de test en cours.

10. Dans le panneau Paramètres, cliquez sur **Editer** pour afficher les paramètres en cours pour votre test. Vous pouvez mettre à jour les paramètres suivants :
    - **Intervalle** définit la fréquence avec laquelle le test s'exécute.
    - **Fréquence de test** détermine si votre test s'exécute depuis tous les emplacements simultanément ou d'un emplacement différent à chaque intervalle. Sélectionnez **Simultanée** pour exécuter votre test depuis tous les emplacements simultanément, ou **Echelonnée** pour l'exécuter depuis un emplacement différent à chaque intervalle.
    - **Emplacements** détermine l'emplacement où votre test s'exécutera.

    Cliquez sur **Sauvegarder** pour
finir de configurer votre test.

11. Cliquez sur **Terminer**. Le tableau de bord {{site.data.keyword.prf_hubshort}} affiche un récapitulatif du total de vos tests, une carte et une table qui
décrivent la fréquence et l'emplacement de vos alertes, tous les tests synthétiques associés à votre application, une table de vos activités et un graphique linéaire qui présente le temps de
réponse et la disponibilité de votre application et d'autres sites Web. Vous pouvez créer d'autres tests, si nécessaire.
12. Vous pouvez utiliser le service {{site.data.keyword.alertnotificationfull}} pour configurer la fonction de surveillance de manière à envoyer des notifications lorsqu'un
événement se produit. Pour plus d'informations, voir [Activation de notifications](avmon_notifications.html "Configurer la fonction de surveillance pour envoyer des notifications lorsqu'un événement seproduit.").


## Résultats
{: #avmon_getstarted_results}

Les résultats des tests s'affichent après l'intervalle spécifié dans la zone réservée à cet effet. L'intervalle par défaut est de 15 minutes.

Vous êtes maintenant prêt à surveiller la disponibilité de vos applications Web. Les informations sur les temps de réponse et la disponibilité de votre application, du site Web ou de l'API
REST sont présentées sur un graphique linéaire, ainsi que les informations sur les activités et tests récents, sur le panneau **Temps de réponse et disponibilité**.

Deux guides sont disponibles pour vous aider à découvrir les fonctions d'{{site.data.keyword.prf_hubshort}}.

 - **Bibliothèque de tutoriels vidéo** - La bibliothèque de tutoriels vidéo contient des vidéos qui expliquent comment créer des applications Bluemix, comment créer
des tests avec Availability Monitoring, comment créer des scripts tests avec Selenium IDE et comment envoyer des alertes à Slack.
 - **Bienvenue dans la rubrique Surveillance !** Le guide Bienvenue dans la rubrique Surveillance met en évidence des zones du tableau de bord et explique chaque fonction
d'{{site.data.keyword.prf_hubshort}}.

Pour ouvrir un guide, cliquez sur l'icône **Aide** ![Icône Aide](images/help_icn_white_sml.jpg) puis cliquez sur le guide que vous souhaitez
afficher.
