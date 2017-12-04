---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}


# Génération d'alerte dans Availability Monitoring
{: #avmon_alert_desc}

Dans {{site.data.keyword.prf_hubshort}}, les tests peuvent générer jusqu'à trois alertes au total. Votre test signale l'alerte avec le niveau de gravité le plus élevé jusqu'à ce
que la condition causant l'alerte soit résolue.
{: shortdesc}

Une alerte séparée est émise pour trois situations différentes :

-   Lorsque le temps de réponse de votre application Web ou adresse URL dépasse le seuil d'avertissement ou le seuil critique défini pour votre test. Chaque test mesure le temps de réponse par défaut et émet une alerte reposant sur les seuils Avertissement et Critique pour ce test.
-   Lorsque votre test renvoie un code de réponse HTTP indiquant que votre application Web ou votre adresse URL n'est pas disponible en raison d'une erreur au niveau du client ou du
serveur. Chaque test vérifie le code de réponse par défaut pour déterminer si le test a abouti ou échoué.
-   Quand votre test détermine qu'une ou plusieurs conditions personnalisées sont satisfaites, une alarme est émise avec le niveau de gravité le plus élevé, comme défini dans ces conditions. {{site.data.keyword.prf_hubshort}} considère toutes les conditions personnalisées globalement quand il détermine si une alarme est émise. Cette alarme subsiste jusqu'à ce que votre test détermine qu'aucune des conditions personnalisées ne génère plus aucune alerte Avertissement ou Critique.

Si plus d'une alerte est générée, {{site.data.keyword.prf_hubshort}} signalera l'alerte avec le niveau de gravité le plus élevé tant qu'une alerte existera.

Par exemple, si votre temps de réponse de test génère une alerte d'avertissement et une autre condition génère une alerte d'avertissement, une alerte critique est générée par votre test et
apparaît sur le tableau de bord {{site.data.keyword.prf_hubshort}}. Si la condition qui cause une alerte critique cesse d'exister, le niveau de gravité de votre alerte de test
passe à "Avertissement". Une alerte persiste jusqu'à ce que toutes les conditions causant l'alerte cessent d'exister.
