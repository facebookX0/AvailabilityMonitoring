---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Utilisation du service
{: #avmon_usage}

Vous pouvez afficher des détails sur votre utilisation d'{{site.data.keyword.prf_hubshort}} sur l'onglet **Surveillance** de votre application et sur le tableau
de bord principal d'{{site.data.keyword.prf_hubshort}}.

Pour examiner votre utilisation d'{{site.data.keyword.prf_hubshort}}
depuis la table **Toutes les applications**, cliquez sur le nom de votre application, puis sur l'onglet
**Surveillance** dans le panneau de votre application. Votre **Utilisation**
en pourcentage est affichée dans un graphique en forme de jauge, ainsi que le plan que vous utilisez.

Pour afficher un aperçu de l'utilisation dans le tableau de bord principal d'{{site.data.keyword.prf_hubshort}}, cliquez sur l'icône **Configurer**
![Icône Configurer](images/config_icn_white_smll.jpg). Si vous utilisez le plan
{{site.data.keyword.prf_hubshort}} Lite, votre utilisation est affichée dans un graphique en barres, ainsi que le nombre de
tests en cours d'utilisation. Si vous êtes abonné au forfait payant, votre utilisation est affichée sous forme de points de données. Vous pouvez afficher les détails de l'utilisation de chaque test
individuel dans le panneau Tests synthétiques.

Votre utilisation est mesurée en points de données. Le nombre de points de données estimé est calculé au moyen de la formule suivante :

Nombre estimé de points de données = T \* L \* (60/M \* 24 \* 30) par mois

Où T = nombre de tests synthétiques qui sont exécutés, L = nombre d'emplacements, et M = intervalle entre les tests (minutes).

Les tests simples tels que les tests de page Web et d'API REST utilisent 1 point de données pour chaque test. Les tests avancés tels que les tests de scripts
Selenium et de scripts d'API REST utilisent 100 points de données pour chaque test.

Vous pouvez afficher votre utilisation actuelle sur le Tableau de bord de l'utilisation, sur la page Compte {{site.data.keyword.Bluemix_notm}}. Cliquez sur
**Compte** puis sélectionnez **Tableau de bord de l'utilisation** et faites défiler jusqu'à la section **Frais de service**. Cliquez sur l'icône **Flèche** du service {{site.data.keyword.prf_hubshort}}
pour afficher le nombre de points de données que vous avez utilisé. Pour en savoir plus sur les plans de tarification et d'utilisation d'{{site.data.keyword.prf_hubshort}}, voir
Plans de tarification sur la page du catalogue [Availability Monitoring](https://console.{DomainName}/catalog/services/availability-monitoring/ "(ouvre un nouvel onglet ou une fenêtre)"){: new_window}.
