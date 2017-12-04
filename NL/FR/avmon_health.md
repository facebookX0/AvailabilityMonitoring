---

copyright:
  years: 2015, 2017
lastupdated: "2017-9-28"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Santé de l'application
{: #avmon_health}

Le panneau Santé de l'application offre une image instantanée de la performance de votre application basée sur la disponibilité de votre application, sur la satisfaction des utilisateurs avec les performances de votre application et sur la capacité de traitement de votre application.
{: shortdesc}

Si {{site.data.keyword.prf_hubshort}} détecte qu'un collecteur de données est configuré pour votre application, le panneau Santé de l'application s'affiche.

**Limitation :** dans un premier temps, un collecteur de données est uniquement disponible pour les applications Node.js. Pour en savoir plus sur la configuration du collecteur de données Node.js, voir la [documentation du collecteur de données Node.js](https://www.npmjs.com/package/ibmapm "(ouvre un nouvel onglet ou une fenêtre)"){: new_window}.

Le panneau affiche trois métriques : **Disponibilité**, **Score de satisfaction** et **Volume des demandes**. ![Panneau Santé de l'application montrant le niveau de disponibilité, la satisfaction des utilisateurs et la capacité de traitement des transactions de vos applications.](images/avmon_app_health_ui.jpg) Le calcul de la métrique **Disponibilité** est basé sur les données de transaction d'utilisateurs simulées par vos tests synthétiques. Les métriques **Score de satisfaction** et **Volume des demandes**, par contre, reposent sur des données de transaction d'utilisateurs à la fois réelles et simulées, fournies par les collecteurs de données.

Les étiquettes numériques montrent la dernière valeur de chaque métrique. Par exemple, la dernière valeur de **Disponibilité** est ![Dernière valeur de la métrique Disponibilité.](images/avmon_app_health_latest.jpg). Les graphiques de série temporelle montrent la performance de votre application pour chaque métrique dans le temps. Vous pouvez définir l'intervalle de temps des graphiques historiques en sélectionnant les dernières **24 heures** ou les **7 derniers jours** dans la liste déroulante. Lorsque vous survolez la ligne du graphique, la valeur de chaque point de données s'affiche dans une infobulle, par exemple, ![Infobulle sur le graphique linéaire de l'historique.](images/avmon_app_health_hover.jpg). Lorsque vous cliquez sur un point de données du graphique linéaire, l'étiquette numérique affiche la valeur correspondant à ce point de données. Cliquez à n'importe quel endroit en dehors des graphiques linéaires pour afficher les dernières valeurs des étiquettes numériques. Survoler ou cliquer sur un graphique met à jour les deux autres graphiques du panneau **Santé de l'application**.

Cliquez sur ![Menu d'affichage des contributions que vous pouvez développer pour voir les transactions ou les tests à forte contribution.](images/avmon_view_contrib.jpg) pour voir les cinq transactions ou tests ayant le plus contribué à la santé actuelle de l'application.![Panneau Santé d'application montrant le niveau de disponibilité, la satisfaction des utilisateurs et la capacité de transaction de votre application.](images/avmon_app_health_expanded.jpg)

## Disponibilité
{: #avmon_health_availability}
La métrique **Disponibilité** montre le niveau d'opérationnalité de votre application. La disponibilité est déterminée par le pourcentage d'instances de test synthétiques ayant abouti de manière satisfaisante. Par exemple, si tous vos tests synthétiques ont été satisfaisants au cours du dernier intervalle, la valeur de Disponibilité en cours pour votre application est de 100 %.

Vous pouvez configurer la manière dont {{site.data.keyword.prf_hubshort}} calcule la disponibilité dans l'onglet Surveillance en sélectionnant les tests à inclure dans le calcul de la disponibilité. Pour plus d'informations, voir [Accès à Availability Monitoring](avmon_tab.html "Vous pouvez accéder au tableau de bord Availability Monitoring dans l'onglet **Surveillance**. L'onglet Surveillance de votre application Cloud Foundry affiche des informations récapitulatives sur la disponibilité et le statut de vos tests, ainsi que des détails sur votre abonnement auservice et sur l'utilisation du service.").


{{site.data.keyword.prf_hubshort}} calcule le pourcentage des instances de test disponibles par heure. Survolez la ligne du graphique pour voir la valeur de chaque intervalle
horaire au cours des dernières 24 heures ou des 7 derniers jours.

Les cinq tests synthétiques ayant le plus contribué au niveau de disponibilité actuel de votre application s'affichent. Le tableau affiche les informations suivantes sur chaque test.

-   **Tests** affiche les noms des tests assignés.
-   **Instances** affiche le nombre d'instances de test exécutées pour chaque test.
-   **Taux d'échec** affiche le pourcentage d'instances de test ayant échoué pour chaque test.


## Score de satisfaction
{: #avmon_health_satscore}
Le **score de satisfaction** indique la satisfaction des utilisateurs quant à la réactivité de votre application. Vous définissez un seuil de satisfaction
(**T**) pour votre application. Vous déterminez ensuite quel temps de réponse les demandes des utilisateurs doivent prendre pour que vos utilisateurs soient satisfaits.

Les temps de réponse des utilisateurs sont convertis en une valeur d'index comprise entre 0,0 et 1,0 (1,0 étant un score parfait où tous les utilisateurs sont satisfaits). Pour calculer
le score de satisfaction, les échantillons d'utilisateurs sont catégorisés comme suit :

-   Satisfaits - les demandes d'utilisateurs avec un temps de réponse inférieur ou égal au seuil de satisfaction défini sont considérées comme satisfaites.
-   Tolérés - les demandes d'utilisateurs qui se situent entre Satisfaits et Frustrés sont considérées comme tolérées.
-   Frustrés - les demandes d'utilisateurs avec un temps de réponse supérieur à 4**T** ou générant une erreur sont considérés comme frustrées.

Le score de satisfaction est ensuite calculé comme le rapport des [demandes d'utilisateurs satisfaites + (demandes d'utilisateurs tolérées /2)] / [nombre total de demandes
d'utilisateurs].

{{site.data.keyword.prf_hubshort}} calcule le score de satisfaction en fonction des données de transaction de chaque intervalle horaire. Survolez la ligne du graphique pour voir
le score de chaque intervalle horaire au cours des dernières 24 heures ou des 7 derniers jours.

Le tableau affiche les informations suivantes sur les cinq transactions ayant le plus contribué au score de satisfaction de votre application :

-   **Transactions** affiche le nom des transactions d'utilisateurs.
-   **Score** affiche le score de satisfaction qui est calculé pour la transaction individuelle.
-   **Insatisfaction** affiche la contribution de la transaction aux niveaux d'insatisfaction actuels. Si la satisfaction des utilisateurs n'est pas optimale, utilisez
le pourcentage d'**insatisfaction** pour évaluer dans quelle mesure chaque transaction a impacté les niveaux d'insatisfaction.


## Volume des demandes
{: #avmon_health_reqvol}
La métrique Volume des demandes reflète le volume actuel des instances de transactions d'utilisateurs. La métrique indique la capacité de traitement actuelle de votre application.

Le temps de réponse de transaction moyen de votre application s'affiche également sous l'étiquette, par exemple ![Temps de réponsemoyen de la dernière valeur.](images/avmon_app_health_response.jpg) et les temps de réponse moyens sont tracés sur le graphique. Vous pouvez rechercher les corrélations entre les augmentations de la capacité de traitement et

les augmentations du temps de réponse moyen.

Les données brutes du volume des demandes sont collectées et affichées sur le graphique toutes les heures. Survolez la ligne du graphique pour voir la capacité de traitement de votre
application à chaque intervalle horaire au cours des dernières 24 heures ou des 7 derniers jours.

Le tableau affiche les informations suivantes sur les cinq transactions contribuant le plus au volume des demandes en cours. Si votre application fait face à des volumes de trafic
utilisateur élevés, utilisez le **Pourcentage de la taille totale** pour évaluer dans quelle mesure chaque transaction contribue au volume de trafic total.

-   **Transaction** affiche le nom de la transaction d'utilisateur.
-   **Volume** montre le nombre d'instances de transaction de chaque transaction.
-   **Pourcentage de la taille totale** affiche le pourcentage du volume total des demandes.
