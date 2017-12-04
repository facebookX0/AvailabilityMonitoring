---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}


# Activité
{: #avmon_activities}

Affichez des informations sur les activités dans le panneau Activité. Les _activités_ sont des actions qui se produisent en dehors des événements définis par l'utilisateur.
{: shortdesc}

Le panneau Activité affiche des informations sur toutes les activités de votre application au cours des dernières 24 heures (démarrage, arrêt ou déploiement, par exemple).

![Panneau Activité sur le tableau de bord Availability Monitoring.](images/avmon_activity_pane.png)

Les activités {{site.data.keyword.Bluemix_notm}} sont des événements d'application qui se produisent dans {{site.data.keyword.Bluemix_notm}}, comme l'arrêt de votre
application, son démarrage ou sa reconstitution, par exemple. Les activités de pipeline sont des événements qui se produisent dans votre pipeline DevOps (générations, déploiements ou tests, par exemple). L'en-tête
du tableau affiche des outils séparés pour les activités {{site.data.keyword.Bluemix_notm}} et les activités de pipeline. Vous pouvez filtrer par activité Source pour afficher les
activités {{site.data.keyword.Bluemix_notm}} ou les activités Pipeline en cliquant sur les icônes {{site.data.keyword.Bluemix_notm}} ou Pipeline sur l'en-tête du panneau
Activité.

Pour afficher Activité du pipeline dans le tableau de bord {{site.data.keyword.prf_hubshort}}, vous devez d'abord activer {{site.data.keyword.contdelivery_short}} pour
votre application puis configurer une chaîne d'outils contenant un pipeline et le service {{site.data.keyword.DRA_short}}. Cliquez sur **Configuration du pipeline**
pour créer une chaîne d'outils pour votre application. Pour obtenir plus d'informations, voir [Initiation à Continuous Delivery](../ContinuousDelivery/index.html "(ouvre un nouvel onglet ou unefenêtre)"){:new_window} et [Initiation à DevOps Insights](../DevOpsInsights/index.html#gettingstarted "(ouvre un nouvel onglet ou une fenêtre)").

{: tip}

Si {{site.data.keyword.contdelivery_short}} et {{site.data.keyword.DRA_short}} sont configurés pour votre application, vous pouvez cliquer sur **Afficher les
analyses** dans la colonne Evénement pour accéder au tableau de bord {{site.data.keyword.DRA_short}} et afficher des détails supplémentaires sur vos activités du pipeline.

{{site.data.keyword.Bluemix_notm}} et Activité du pipeline sont également affichés dans **Flux métrique** et sur le graphique du panneau Temps de réponse
et disponibilité.
