# Incident du 29 avril 2021

## Incident de production du 29 avril 2021

Dans la matinée du 29 avril, nous avons eu deux incidents simultanés qui ont rendu l’accès du site très difficile, voire impossible, pour les usagers et pour les agents.

### Chronologie

(Heure française, UTC+1)

* **9 h 21** livraison d'une mise à jour technique ([https://github.com/betagouv/rdv-solidarites.fr/pull/1387](https://github.com/betagouv/rdv-solidarites.fr/pull/1387))
* **9 h 38** livraison de la fonctionnalité d'agenda inter-organisation ([https://github.com/betagouv/rdv-solidarites.fr/pull/1241](https://github.com/betagouv/rdv-solidarites.fr/pull/1241))
* **9 h 55** première vague d'erreurs technique remonté par notre système de surveillance
* **10 h 13** Alertes d'un outil surveillant la présence en ligne de RDV-Solidarités : le service n'est plus accessible
* **10 h 30** Plusieurs emails de la part de référentes pour nous alerter à propos de très gros ralentissement de RDV-Solidarités
* **10 h 35** Démarrage de serveurs supplémentaire pour essayer de résorber les problèmes, le temps de trouver une solution
* **10 h 52** Livraison d'une annulation de la mise à jour technique
* **11 h 05** Signalement que les ralentissements sont toujours très ressenti sur le service
* **11 h 29** Livraison d'une annulation de la fonctionnalité d'agenda inter-organisation.

### Impacts

Il ne s'agit pas de perte de données.

Nous avons eu deux problèmes en même temps :

* La mise à jour technique impactant l'interface graphique et l'affichage d'information. Certaines pages ne devaient pas s'afficher correctement à différents endroits du service
* L'agenda inter-organisation impactant les performances coté serveur. Le calcul et la construction des pages d'agenda prenant beaucoup de temps, la machine ne pouvait plus répondre aux autres demandes des utilisateurs.

En ajoutant des serveurs, nous avons pu résorber un peu la gêne sur les temps de réponses, mais ce n'était pas suffisant.

#### Chiffres

Comme on peut le voir, il y a eu une très forte augmentation du **temps de réponse** par rapport à la moyenne

![](../../../.gitbook/assets/dae92eae8a9e16e76957686e3dd84d050ebd92e6.png)

Les **processeurs des serveurs** ont également été très sollicités

![](../../../.gitbook/assets/a3e18fc7c7373fda7027bbed5355d1cc1473c502.png)

Nous avions cependant autant de **demande** que d'habitude (aucun écart entre ce matin et cette après-midi). On peut voir apparaitre des points rouges qui correspondent à des demandes que nous n'avons pas pu satisfaire correctement. Les points vers et bleu correspondent à nos interventions diverses.

![](../../../.gitbook/assets/ec24a09ab646509eb707e33d2d23fc1017ee9d23.png)

### Conséquences

La **mise à jour technique** ne concernait pas de correction de faille de sécurité. Il n'y a donc aucune conséquence à attendre pour refaire cette mise à jour plus tard, après avoir vérifié élément par élément.

Pour l'**agenda inter-organisation**, nous allons reprendre le code pour améliorer les performances, en vérifiant point par point. Une nouvelle livraison sera planifiée dès que possible.

### Conclusion

Nous avons **réagi assez rapidement** malgré le fait que nous ayons eu à faire deux annulations.

Un point de progression serait d'être plus vigilant aux signaux faibles suite à une livraison. Une augmentation trop forte du **temps de réponse** nous aurais permis sans doute de réagir avant même les premières alertes.

Nous pourrions mettre en place des outils pour cela. Mais comme dit Nicolas, nous en avons déjà des outils, nos yeux. Il s'agit surtout de les laisser ouverts sur les bonnes pages :smile:

### Mise à jour du 6 mai.

Nous avons fait quelques corrections et repoussé l'agenda inter-organisation en production. Certaines lenteurs sont encore présentes. C'est beaucoup mieux que la dernière fois, mais ça ne suffit pas.

![](../../../.gitbook/assets/8e1b4ba0684b2d5983d8b522ed5c7b041eb2735f.png)

Nous sommes en train de travailler sur une correction. Tout devrait rentrer dans l'ordre d'ici à ce soir.
