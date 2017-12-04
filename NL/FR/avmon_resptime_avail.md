---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Temps de réponse et disponibilité
{: #avmon_resptime_avail}

Utilisez le panneau Temps de réponse et disponibilité pour visualiser le temps de réponse, les tendances de disponibilité, les alertes et les activités dans le temps. La corrélation
des métriques, des alertes et des activités vous aide à identifier facilement un déploiement de code ou un changement spécifique au niveau d'une application lorsque vous remarquez qu'un temps de
réponse est affecté.
{: shortdesc}

## Temps de réponse
{: #avmon_resptime_graph}

Les informations sur les temps de réponse s'affichent sur un graphique linéaire. Pour les afficher, cliquez sur l'onglet **Temps de réponse**.

![Graphique des temps de réponse d'un test au cours des dernières 24 heures.](images/avmon_rt_gr.jpg)

Les temps de réponse mesurés par
{{site.data.keyword.prf_hubshort}} sont légèrement supérieurs aux temps de réponse
perçus par les utilisateurs. {{site.data.keyword.prf_hubshort}}
imite un comportement utilisateur réel, ce qui alourdit la mesure du temps de réponse. La surcharge est due aux facteurs suivants :
  - {{site.data.keyword.prf_hubshort}} crée une nouvelle instance Firefox
pour chaque test afin d'empêcher les lectures antérieures d'influencer le test en cours. Les utilisateurs réels peuvent
connaître des temps de réponse plus courts en raison du cache du navigateur.
  - {{site.data.keyword.prf_hubshort}} installe le plug-in de pilote Web de Firefox avant chaque test.
{: tip}

Les temps de réponse individuels des tests sont représentés par une icône **Point de réponse** ![Icône Point deréponse](images/crcl_icn_white.jpg) sur le graphique linéaire. Les différentes couleurs correspondent aux différents emplacements géographiques dans lesquels l'application est exécutée. L'axe des Y du graphique utilise des icônes d'alerte pour identifier les plages de seuils Avertissement et Critique. L'icône

jaune **Avertissement** ![Icône d'avertissement jaune](images/alrt_icn_white_smll.jpg) représente la plage du seuil
d'avertissement et l'icône rouge
**Critique** ![Icône rouge Critique](images/wrng_icn_white_smll.jpg) représente la plage du seuil critique. Cliquez sur l'icône jaune
**Avertissement** ![Icône jaune Avertissement](images/alrt_icn_white_smll.jpg) ou sur l'icône rouge **Critique**
![Icône rouge Critique](images/wrng_icn_white_smll.jpg) pour identifier facilement les instances de test qui apparaissent dans les plages du seuil d'avertissement et
du seuil critique. Pour afficher les détails d'une instance de test spécifique, cliquez sur l'icône **Point de réponse**
![Icône Point de réponse](images/crcl_icn_white.jpg) sur le graphique.

### Filtres

Choisissez un test dans le menu déroulant **Test**. Vous pouvez filtrer les données sur 3 heures, 24 heures, 7 jours, 30 jours et 12 mois. La possibilité de visualiser les données sur
12 mois n'est disponible qu'aux utilisateurs avec abonnement payant à {{site.data.keyword.prf_hubshort}}. Quand vous procédez à un filtrage pour une plage de temps supérieure à 24 heures, une moyenne des valeurs s'affichant dans le graphique est effectuée. Pour afficher des informations plus spécifiques, cliquez sur le graphique pour explorer en détail les alertes et avertissements individuels. Vous pouvez aussi utiliser le curseur pour restreindre ou étendre la plage de temps.

Le graphique Temps de réponse permet de mettre en évidence et de masquer les données des emplacements de point de présence particuliers. Pour mettre en évidence les données de temps de réponse pour un
emplacement particulier, survolez le nom de l'emplacement de point de présence puis cliquez sur l'icône **Mise en évidence de l'emplacement**
![Icône Mise en évidence de l'emplacement](images/avmon_location_highlight.jpg). Pour masquer les données de temps de réponse pour un emplacement, survolez le nom de
l'emplacement de point de présence puis cliquez sur l'icône **Masquer l'emplacement** ![Icône Masquer l'emplacement](images/avmon_location_remove.jpg). Pour
restaurer les données de l'emplacement de point de présence dans le graphique, cliquez sur l'icône **Ajouter d'autres emplacements**
![Icône Ajouter d'autres emplacements](images/icn_plus_20x20.jpg) ou sur l'onglet **Sélection de métrique** puis cliquez sur l'emplacement de point
de présence supprimé auparavant.

### Alertes et activités

Vous pouvez facilement identifier les alertes Critique et Avertissement dans la ligne Alertes. Survolez une **icône d'alerte**
![icône d'alerte critique](images/avmon_crit_alert.png)![icône d'alerte d'avertissement](images/avmon_warn_alert.png) pour identifier
le niveau de gravité et l'horodatage de cette alerte. Cliquez sur une **icône d'alerte** pour afficher des détails sur cette alerte dans **Flux métrique**.

Vous pouvez aussi visualiser des activités sur le même graphique. Les _activités_ sont des actions qui se produisent, sans être des événements définis par l'utilisateur. Les
activités {{site.data.keyword.Bluemix_notm}} sont des événements d'application qui se produisent dans {{site.data.keyword.Bluemix_notm}}, comme l'arrêt de votre application, son
démarrage ou sa reconstitution, par exemple. Les activités de pipeline sont des événements qui se produisent dans votre chaîne d'outils {{site.data.keyword.contdelivery_short}}
(générations, déploiements et tests, par exemple). Cliquez sur une activité pour afficher des informations relatives à cette activité dans **Flux métrique**. Vous pouvez
afficher des informations sur ces activités dans le panneau Activité.

Pour afficher Activité du pipeline dans le tableau de bord {{site.data.keyword.prf_hubshort}}, vous devez d'abord activer {{site.data.keyword.contdelivery_short}} pour
votre application puis configurer une chaîne d'outils contenant un pipeline et le service {{site.data.keyword.DRA_short}}. Cliquez sur **Configuration du pipeline**
sur le panneau Récapitulatif ou sur le panneau Activité pour créer une chaîne d'outils pour votre application. Pour obtenir plus d'informations, voir
[Initiation à Continuous Delivery](../ContinuousDelivery/index.html "(ouvre un nouvel onglet ou une fenêtre)") et
[Initiation à DevOps Insights](../DevOpsInsights/index.html#gettingstarted "(ouvre un nouvel onglet ou une fenêtre)"){: new_window}.
{: tip}

Si plusieurs activités ou icônes d'alerte sont présentes ensemble sur les lignes Alertes et Activités, une **icône de nombre** affiche le nombre d'alertes ou d'activités
présentes à ce moment. Survolez une **icône de nombre** pour afficher les alertes ou les activités individuelles et cliquez sur une alerte ou sur une activité pour afficher
des informations dans **Flux métrique**.

### Sélection de métrique et Flux métrique

Pour filtrer d'après des métriques définies par région géographique, cliquez sur **Sélection de métrique**. Cliquez sur un emplacement pour ajouter ou retirer des métriques qui sont mesurées à cet emplacement depuis le graphique. Cliquez sur **Ajouter plus d'emplacements** pour
ouvrir la page Tester le mode édition et ajouter un emplacement de point de présence au test sélectionné.

![Onglet Sélection métrique affichant les filtres des emplacements de point de présence.](images/avmon_metric_sel.jpg)

Pour afficher une liste des détails relatifs aux métriques, cliquez sur **Flux métrique**. Flux métrique affiche une liste des instances sur lesquelles une métrique est
satisfaite.

![Onglet Flux métrique affichant les détails d'une alerte d'avertissement.](images/avmon_warn_met_feed.png)

Cliquez sur une **icône d'alerte**, une **icône d'activité** ou un **point de réponse**
![Icône Point de réponse](images/crcl_icn_white.jpg) sur le graphique pour ajouter les détails de cette métrique dans Flux métrique.

![Détails d'une instance de test disponible dans Flux métrique.](images/avmon_avail_metfeed.png)

Si vous filtrez le graphique Temps de réponse sur une plage de temps supérieure à 24 heures et cliquez sur un **point de réponse**, les informations cumulées
correspondant à cette journée s'affichent dans Flux métrique.

![Flux métrique montrant des informations cumulées de toutes les instances de votre test pour une journée.](images/avmon_avail_day_met_feed.png)

Cliquez sur **Zoom** pour afficher dans le graphique Temps de réponse l'ensemble des temps de réponse, des activités et des alertes qui ont été générés par un test au cours de cette journée.

Pour afficher des informations détaillées sur une alerte ou sur un temps de réponse de test, cliquez sur **Répartition** dans Flux métrique. Cliquez sur
**Alerte la plus proche** pour afficher l'alerte la plus proche de cette instance de test dans Flux métrique, si une alerte s'est produite. Pour afficher des informations
détaillées sur une activité de pipeline dans le service {{site.data.keyword.DRA_short}}, cliquez sur **Afficher les analyses** dans Flux métrique.

## Disponibilité
{: #avmon_avail_graph}

Pour afficher des informations sur la disponibilité de vos applications, cliquez sur Disponibilité. Le graphique Disponibilité affiche la disponibilité quotidienne de chaque point de présence (ou POP, pour Point of Presence) pour le test sélectionné.

![Graphique de disponibilité affichant la disponibilité des tests quotidiens par emplacement au cours des 7 derniers jours.](images/avmon_avail_graph.png)

Le graphique Disponibilité permet de mettre en évidence et de masquer les données d'emplacements de point de présence particuliers. Pour mettre en évidence les données de disponibilité pour un emplacement
particulier, survolez le **nom de l'emplacement du point de présence** puis cliquez sur l'icône **Mise en évidence de l'emplacement**
![Icône Mise en évidence de l'emplacement](images/avmon_location_highlight.jpg). Pour masquer les données de disponibilité d'un emplacement, survolez le **nom
de l'emplacement de point de présence** puis cliquez sur l'icône **Masquer l'emplacement** ![Icône Masquerl'emplacement](images/avmon_location_remove.jpg). Pour restaurer les données de l'emplacement de point de présence dans le graphique, cliquez sur l'onglet **Sélection de métrique**, puis sur

l'emplacement de point de présence retiré auparavant.

Survolez un point du graphique pour afficher le taux d'échec et le nombre d'instances de test pour un jour et un emplacement particulier. Cliquez sur un point du graphique pour
afficher ces informations dans Flux métrique.

![Disponibilité de test au point de présence de Dallas dans Flux métrique.](images/avmon_avail_metric.png)

Cliquez sur **Zoom** pour filtrer le graphique Disponibilité et le graphique Temps de réponse pour afficher des informations pour le jour sélectionné.
