---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Création d'un test d'API REST
{: #avmon_rest_api}

Créez un test d'API REST pour tester les temps de réponse et la disponibilité de votre application Web
à l'aide des méthodes HTTP suivantes : GET, POST, PUT et DELETE.
{: shortdesc}

Utilisez les tests d'API REST pour surveiller la disponibilité et les performances de votre application Web et des autres URL en réponse aux appels REST.

Pour créer une API REST, procédez comme suit.

1.  Si vous affichez l'onglet **Surveillance** pour votre application Cloud Foundry, cliquez sur **Ajouter un nouveau test**.

    ![Onglet Surveillance de votre application Cloud Foundry.](images/avmon_tab.png)

    Si vous affichez le tableau de bord {{site.data.keyword.prf_hubshort}}, cliquez sur **Ajouter un nouveau test** sur le panneau Tests synthétiques.

    ![Bouton Ajouter un nouveau test sur le panneau Tests synthétiques.](images/syn_tests_pane.jpg)

2.  Cliquez sur **Action unique** sur la page Configuration de la surveillance puis cliquez sur **API REST** sur la page Action unique.
3.  Entrez un nom significatif pour votre test dans la zone **Nom**. Ajoutez une description de l'objectif du test dans la zone **Description**.
4.  Dans la section Demande, sélectionnez le type de méthode dans la liste **Méthode** et entrez une adresse **URL** que vous souhaitez tester avec cette méthode. Vous pouvez choisir **GET**, **PUT**, **POST** ou **DELETE**. Si vous choisissez la méthode PUT ou POST, vous pouvez entrer le contenu du corps à tester dans la zone **Corps de demande (facultatif)**.

    Par exemple, le test d'API REST suivant utilise la méthode POST pour demander que votre application Web accepte les données en plus de tester la disponibilité et la performance de cette application Web.

    ![Exemple de test d'API REST utilisant la méthode de demande POST.](images/avmon_restapi_post.png)

5.  Vous pouvez configurer votre test pour inclure une valeur ou un en-tête particulier. Entrez un nom d'en-tête et une valeur d'en-tête dans les zones **En-tête**.

    Si l'application Web que vous souhaitez tester nécessite un nom d'utilisateur et un mot de passe, entrez "Authorization" dans la zone **Nom d'en-tête**. Entrez le mot "Basic", un espace et la valeur codé en base64 de votre username:password dans la zone **Valeur d'en-tête**.

    Par exemple, si votre nom d'utilisateur est Aladin et votre mot de passe est SésameOuvreToi, entrez le mot "Basic", un espace et la valeur de Aladin:SésameOuvreToi codée en base64 dans la zone **Valeur d'en-tête**.

    ![Zones d'en-tête montrant les données d'identification pour l'autorisation de test en base64.](images/avmon_apitest_auth.png)

6.  Configurez les seuils d'alerte Avertissements et Critique pour votre test dans la section Validation de réponse. Editez le contenu des zones **Valeur** et **Unité** pour chaque ligne. Les temps de réponse qui dépassent les seuils Avertissement et Critique que vous avez définis déclenchent des alertes.

    ![Section Validation de réponse avec seuils Avertissement et Critiques par défaut.](images/avmon_restapi_resp_val.png)

7.  Cliquez sur **Ajouter une condition** pour définir et ajouter des conditions de validation de réponse personnalisées. Les conditions de validation de réponses personnalisées sont évaluées globalement pour générer une alerte. Vous pouvez définir et ajouter jusqu'à six conditions personnalisées pour votre test.

    Dans {{site.data.keyword.prf_hubshort}}, chaque test peut générer un total de trois alertes au maximum. Votre test signale l'alerte avec le niveau de gravité le plus élevé jusqu'à ce que toutes les conditions causant les alertes soient résolues. Pour plus d'informations, voir [Génération d'alerte dans Availability Monitoring](avmon_alert_desc.html "Dans Availability Monitoring, les tests peuvent générer jusqu'à trois alertes au total. Votre test signale les alertes ayant le niveau de gravité le plus élevé jusqu'à ce que la condition causant l'alerte soit résolue.")
    {: tip}

    Vous pouvez valider les données suivantes :

    - **Code de réponse d'en-tête**. Sélectionnez **Code de réponse d'en-tête** pour effectuer un test pour un code de réponse HTTP ou pour une plage de codes de réponses HTTP.
    - **Propriété d'en-tête**. Sélectionnez **Propriété d'en-tête** pour effectuer un test pour une valeur et une propriété particulière de zone d'en-tête HTTP.
    - **Corps JSON**. Sélectionnez **Corps JSON** pour effectuer un test pour une propriété particulière tirée d'un corps JSON.

      Pour chaque condition, entrez une propriété à tester dans la zone **Cible**, et une valeur à tester dans la zone **Valeur**. Sélectionnez un opérateur dans le menu déroulant **Opération**. Enfin,
choisissez un gravité d'alerte pour **Avertissement** ou **Critique** pour votre condition.

    Les valeurs numériques que vous entrez dans la zone **Valeur** sont traitées en tant que nombres, par défaut, et non comme des chaînes. Quand vous entrez une condition de validation de réponse dans une zone **Valeur**, servez-vous de guillemets ("") pour différencier une chaîne d'un nombre. Par
exemple, pour tester la chaîne 123, entrez "123" dans la zone Valeur. Pour procéder à une vérification pour le nombre 400, entrez 400, sans guillemets.
    {: tip}

    ![Conditions de validation de réponse pour un test d'API REST](images/avmon_restapi_resp_val2.png)

8.  Cliquez sur la commande **Vérifier** pour créer votre test d'API REST et déterminer si votre demande de test est valide.

    {{site.data.keyword.prf_hubshort}} détermine la validité du test avec la méthode HTTP sélectionnée et les en-têtes de demande que vous avez définis pour le test. La validation de la réponse n'a pas lieu pendant la vérification du test.

    Votre test validé s'affiche dans la table Eléments vérifiés. Vous pouvez ajouter d'autres adresses URL en répétant les étapes 3 à 8.

9.  Pour configurer vos paramètres de test, cliquez sur Suivant.

    Un récapitulatif de la configuration de test est affichée. Par exemple, le message suivant affiché pour les paramètres par défaut :

    ``Test will occur: Every 15 minutes from 3 locations simultaneously to determine if
test exceeds the specified threshold.``

    Une estimation de l'utilisation et du nombre de tests par mois est affichée compte tenu de votre configuration actuelle.

10. Dans le panneau Paramètres, cliquez sur **Editer** pour afficher les paramètres en cours pour votre test. 

    Vous pouvez changer l'intervalle des tests, leur fréquence et les emplacements d'où sont envoyés les tests.

    ![Panneau Paramètres du test affichant les paramètres par défaut d'un test.](images/avmon_settings.png)

    Sélectionnez **Simultanée** pour exécuter votre test depuis tous les emplacements simultanément, ou **Echelonnée** pour l'exécuter depuis un emplacement différent à chaque intervalle. Cliquez sur **Sauvegarder** pour
finir de configurer votre test.

11. Cliquez sur **Terminer**. Le tableau de bord {{site.data.keyword.prf_hubshort}} affiche un récapitulatif de tous vos tests, une carte et une table qui
affiche le niveau de gravité et l'emplacement de vos alertes, tous les tests synthétiques associés à votre application, une table de vos activités et un graphique linéaire qui présente le temps
de réponse et la disponibilité de votre application et d'autres sites Web.
