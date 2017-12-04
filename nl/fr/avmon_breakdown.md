---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Tableau de bord Répartition
{: avmon_view_breakdown}

Le tableau de bord **Répartition** affiche des statistiques clés sur vos tests. Il récapitule également les informations de
disponibilité et de temps de réponse, les tendances dégagées de l'historique, et les données de performance des tests sur les 24
heures précédentes.
{: shortdesc}

Pour afficher une répartition détaillée d'un test, cliquez sur le test dans le panneau Tests synthétiques. Vous pouvez également ouvrir le tableau de bord Répartition en cliquant
sur **Répartition** dans la table d'alertes du panneau Fréquence des alertes.

Le tableau de bord Répartition affiche quatre panneaux :

## Récapitulatif d'application
{: #avmon_bdown_summary}

![Panneau Récapitulatif du test.](images/avmon_bdown_summ.png)

Le panneau **Récapitulatif du test** affiche les informations de test suivantes pour les dernières 24 heures :

-   **Statut actuel** affiche le statut du test.
-   **Instances de test** affiche la répartition en pourcentage d'instances de test de type normal, avertissement et critique.
-   **Temps de réponse moyen** indique le temps de réponse moyen du test.
-   **Tendances de l'historique** affiche les tendances de l'historique de votre test de performances pour les 50e, 95e et 99e percentiles,
en millisecondes.

## Instances de test
{: #avmon_bdown_instances}

![Répartition des instances de test de l'API Rest dans la table Instances de test.](images/avmon_bdown_apitest_instance.png)

La table **Instances de test** affiche des informations détaillées sur chaque instance de test, dont le statut, le temps de réponse, l'emplacement où s'exécute le test, le nombre d'erreurs et la date et l'heure de son exécution. Pour explorer en détail une instance de test, cliquez sur **Extension**. Des informations de réponse détaillée sont répertoriées pour chaque étape de l'instance de test. Vous pouvez trier les colonnes pour vous aider à identifier rapidement l'étape précise durant laquelle un ralentissement ou un échec s'est produit. L'affichage des erreurs, de la séquence de test et des temps de réponse vous permet d'identifier facilement les problèmes.

Les informations affichées dépendent du type de test synthétique qui fait l'objet de la surveillance.

### API
Lorsque vous cliquez sur **Développer** pour une instance de test d'API, un récapitulatif de haut niveau affiche les informations suivantes :

-   **Réponse** affiche le temps de réponse total pour l'instance de test, y-compris le temps occupé par la redirection.
-   **Redirection** affiche le temps total de redirection pour l'instance de test.
-   **Taille** indique la taille de l'objet.
-   **Vitesse de téléchargement** indique à quelle vitesse chaque objet a été téléchargé.
-   **Erreurs** indique le nombre d'erreurs qui se sont produites au cours de l'instance de test. Pour afficher les détails des erreurs, cliquez sur l'icône **Information**.

Une table décrit chaque étape de l'appel d'API, en indiquant le nom de l'étape, la séquence des étapes et le temps de réponse pour chaque étape. Les noms d'étapes suivants s'affichent :

-   **Recherche de nom** indique combien de temps l'instance de test a pris pour résoudre le nom de l'objet.
-   **Connexion** indique combien de temps l'instance de test a pris depuis le début de l'étape jusqu'à l'établissement d'une connexion à l'hôte
distant ou au proxy.
-   **Connexion d'application** indique combien de temps l'instance de test a pris depuis le début de l'étape jusqu'à l'établissement de la
connexion SSL avec l'hôte distant.
-   **Pré-transfert** indique combien de temps s'est écoulé dans l'instance de test depuis le début de l'étape jusqu'au
démarrage de la commande de transfert.
-   **Démarrage du transfert** indique combien de temps s'est écoulé dans l'instance de test depuis le début de l'étape jusqu'à la réception
du premier octet.
-   **Transfert** indique combien de temps l'instance de test a pris pour transférer le fichier.

### Page Web
![Répartition des instances de tests de page Web dans la table Instances de test.](images/avmon_bdown_webpage_instance.png)

Lorsque vous cliquez sur **Développer** pour une instance de test de page Web, un récapitulatif de haut niveau affiche les informations suivantes :

-   **Réponse** indique le temps de réponse de l'instance de test.
-   **Nombre total de demandes (externes)** indique le nombre total de demandes pour l'instance de test. Le nombre de demandes externes est affiché
entre parenthèses.
-   **Taille de la page** indique la taille de la page Web.
-   **Erreurs** indique le nombre d'erreurs qui se sont produites au cours de l'instance de test. Pour afficher les détails des erreurs, cliquez sur l'icône
Information.

Une table répertoriant les informations suivantes pour chaque demande soumise par le test est également affichée :

-   **Type** indique le type de la demande. Par exemple, HTML, CSS, JavaScript ou image. Les demandes externes et internes sont représentées par des
icônes.
-   **Chemin de fichier** indique l'emplacement de l'objet demandé.
-   **Taille** indique la taille de l'objet demandé.
-   **Séquence** indique la séquence des demandes soumises par le test.
-   **Durée** indique la durée de réalisation de chaque demande.
-   **Code de statut** indique le code de statut de la demande HTTP.
-   **Statut** décrit le résultat de la demande (Réussite, Inconnu ou Echoué, par exemple).

### Script
![Répartition des instances de tests de script dans la table Instances de test.](images/avmon_bdown_script_instance.png)

Lorsque vous cliquez sur **Développer** pour une instance de test de script, le temps de réponse, le nombre d'étapes du
script et le nombre d'erreurs, sont affichés. Pour afficher les détails des erreurs, cliquez sur l'icône **Information**.

Les informations suivantes sur chaque étape du script sont affichées dans une table :

-   **Nom** affiche chaque commande Selenium appelée par votre instance de test, par exemple Open, ClickAt ou VerifyBodyText.
-   **Séquence** affiche la séquence des étapes de script du début à la fin de l'instance de test.
-   **Durée** indique la durée de réalisation de chaque étape du script.
-   **Erreurs** indique le nombre d'erreurs qui se sont produites au cours de chaque étape du script.
-   **Statut** décrit le résultat de l'étape de script (Réussite, Inconnu ou Echoué, par exemple).

Vous pouvez explorer en aval et visualiser les informations sur les demandes générées par chaque étape du script.

![Répartition des détails des étapes individuelles de votre instance de test de script dans la table Instances de test.](images/avmon_bdown_script_subtrans.png)

Cliquez sur **Développer**
pour afficher une table contenant les informations suivantes :

-   **Type** indique le type de la demande. Par exemple, HTML, CSS, JavaScript ou image. Les demandes externes et internes sont représentées par des
icônes.
-   **Chemin de fichier** indique l'emplacement de l'objet demandé.
-   **Taille** indique la taille de l'objet demandé.
-   **Séquence** indique la séquence des demandes soumises par le test.
-   **Durée** indique la durée de réalisation de chaque demande.
-   **Code de statut** indique le code de statut de la demande HTTP.
-   **Statut** décrit le résultat de la demande (Réussite, Inconnu ou Echoué, par exemple).

{{site.data.keyword.prf_hubshort}} peut automatiquement effectuer une capture d'écran
si le chargement de la page Web ou une étape du script échouent. Ainsi, si l'une des étapes de votre script ouvre une page Web mais que celle-ci ne se charge pas, {{site.data.keyword.prf_hubshort}} crée automatiquement une capture d'écran. Pour
afficher une capture d'écran de la page Web ou du script, cliquez sur l'icône **Capture d'écran de l'erreur** ![Icône Capture d'écran de l'erreur](images/scrnsht_err_icn_white.jpg). Cette fonction n'est disponible que pour la surveillance des tests de page Web et des tests de script. Elle ne fonctionne pas avec la surveillance d'API
REST.

Vous pouvez également télécharger un enregistrement du trafic réseau pour une instance de test particulière  en tant que fichier .har en cliquant sur l'icône
**Télécharger** ![Icône Télécharger.](images/download_icn_white_smll.jpg). Cette
fonction est disponible pour la surveillance des tests de page Web et des test de comportement contrôlé par scripts.

## Temps de réponse et disponibilité
{: #avmon_bdown_rt_avail}
Le panneau Temps de réponse et disponibilité affiche un graphique des temps de réponse mesurés et de la disponibilité des instances de votre test durant une période définie. Pour obtenir plus d'informations, voir [Temps de réponse et disponibilité](avmon_resptime_avail.html "Utilisez le panneau Temps de réponse et disponibilité pour visualiser le temps de réponses, les tendances en terme de disponibilité, les alertes et les activités dans le temps. La corrélation des métriques, des alertes et des activités vous aident à identifier facilement un déploiement de code ou une modification sur une application spécifique lorsque vous voyez un temps de réponse affecté.").

## Activité
{: #avmon_bdown_activity}
Le panneau Activité affiche une table de toutes les activités enregistrées au cours des dernières 24 heures. Pour obtenir plus d'informations, voir [Activité](avmon_activities.html "Vous pouvez afficher des informations concernant des activités dans le panneau Activités. Les activités sont des actions qui se produisent en dehors des événements définis par l'utilisateur.").
