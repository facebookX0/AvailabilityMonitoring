---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Tests synthétiques
{: #avmon_synth_tests}

Dans le panneau Tests synthétiques, vous pouvez créer, éditer, supprimer et afficher des tests synthétiques qui surveillent la performance et la disponibilité de vos
applications. Les tests sont affichés dans une vue liste ou carte dans le panneau Tests synthétiques.
{: shortdesc}

![Panneau Tests synthétiques.](images/syn_tests_pane.jpg)

Chaque carte de test affiche des informations sur le test :

- **Disponibilité** affiche le pourcentage de disponibilité du test au cours des dernières 24 heures.
- **Statut** affiche le statut actuel du test. Le statut peut être Critique, Avertissement, Normal, Echec, Inactif ou Inconnu.
- **Temps de réponse moyen** affiche le temps de réponse moyen du test au cours des dernières 24 heures.

Vous pouvez surveiller trois types de tests différents :

- Les tests d'**API REST** indiquent le temps de réponse d'un appel REST. Tous les formats de demandes HTTP, comme GET, POST, PUT et
DELETE, sont pris en charge.
- Les tests de **page Web** indiquent le temps de réponse pour le chargement du site Web sur l'URL entrée.
- Les tests de **comportement contrôlé par script** surveillent les scripts Selenium que vous créez pour imiter les interactions d'un utilisateur avec un site Web. Ainsi, vous pouvez créer un script Selenium imitant un utilisateur qui se connecte à votre application. Vous
exécutez ce script périodiquement pour tester les performances de votre application en réponse aux actions des utilisateurs qui sont automatisées par le script. Vous
pouvez télécharger un script ou ajouter un script depuis un référentiel GitHub. Pour en savoir plus sur la création des scripts Selenium, voir
[Enregistrement des scripts
synthétiques](http://www.ibm.com/support/knowledgecenter/SSMKFH/com.ibm.apmaas.doc/install/admin_syn_record_script.htm "(ouvre un nouvel onglet ou une fenêtre)"){: new_window}.

Pour ajouter un autre test, cliquez sur **Ajouter un nouveau test**.

Pour arrêter, démarrer ou éditer un test synthétique, cliquez sur l'icône **Actions** ![Icône Actions](images/actions_icn_white_smll.jpg)
puis cliquez sur l'action souhaitée. Pour afficher les détails de la répartition du test, cliquez sur le test.

Pour afficher l'utilisation spécifique de chaque test synthétique, cliquez sur l'icône **Coût** ![Icône Coût](images/cost_icn_white_smll.jpg). Si
vous êtes abonné au forfait payant, votre utilisation s'affiche en points de données.
