# Réunion référentes du 28 septembre 2021

### Démo

* [Ajout du nom de la commune dans les exports de RDV #1638](https://github.com/betagouv/rdv-solidarites.fr/issues/1638)
* [Trouver un créneau côté agent depuis un smartphone #1674](https://github.com/betagouv/rdv-solidarites.fr/issues/1674)
* BUG [Afficher la liste des motifs déjà configuré dans le tunnel de prise de RDV de l'organisation MDPH #1734](https://github.com/betagouv/rdv-solidarites.fr/issues/1734)
* [Ajouter une zone de pagination en bas de l'index des motifs #1726](https://github.com/betagouv/rdv-solidarites.fr/issues/1726)
* [Lien depuis configuration de motifs vers la sectorisation #1347](https://github.com/betagouv/rdv-solidarites.fr/issues/1347)

### Sectorisation

La Drôme aura besoin d'une sectorisation à la rue.

Christelle rappel qu'il y a des soucis

* d'ergonomie côté configuration agent est améliorable : navigation pendant la création et les mises à jours, clareté des informations motif-secteur-agent/organisation...
* Disfonctionnement coté usager : usager pouvant prendre un créneau sur un lieu avec un agent qu'il ne devrait pas...

Sectorisation lié à l'ouverture à l'usager.

Les Côtes-d'Armor (22) ont commencés cet été.

### Conseiller numérique

C'est en route. Il y a des réunions mise en place entre les Conseillers numérique et RDV-Solidarités. Ça avance.

Début d'étude de RDV-Solidarités dans le 64. Réflexion sur le motif.

> Les conseillers numérique sont appelé à faire des rendez-vous collectif. -- Christelle (64)

Nécessaire de travailler sur le sujet dans RDV-Solidarités

Utilisation décentralisé de RDV-Solidarités pour pouvoir prendre rendez-vous sur tout le territoire ? Lié à [https://www.solidarite-numerique.fr/](https://www.solidarite-numerique.fr). Questionnement en cours. Question du chevauchement de territoire : si les conseillers numériques sont sur un territoire france entière, comment ça se passe dans les départements ? C'est la problématique opposé des territoires plus petit : si Caen souhaite avoir « RDV-Solidarite » pour son territoire, comment se passe l'intéraction avec le Calvados ?

### Problème de performance

Depuis plusieurs jours, nous avons des problèmes de performances sur le service. Nous avons amorcé [un rapport d'incident, largement incomplet, dans la doc](https://doc.rdv-solidarites.fr/informations-generales-et-legales/incidents/incident-de-production-du-22-septembre-2021)

Plusieurs raisons semblent se pertucter

* une mise à jour technique
* une limite d'accès à la base de donnée qui nous empêche d'augmenter le nombre de machine pouvant répondre aux solicitations
* augmentation **très forte** du nombre d'utilisateurs et utilisatrices
* des améliorations à faire dans certaines parties du code de l'application

### Liste de diffusion

Pour soulager l'équipe, et partager plus largement les informations et surtout plus facilement, une liste de diffusion va être mise en place.

Nous allons garder une adresse privée pour l'équipe pour les messages contenant des informations à caractères personnelles.

L'équipe utilise toujours l'adresse [contact@rdv-solidarites.fr](mailto:contact@rdv-solidarites.fr).

**Nous vous invitons à utiliser principalement l'adresse **[**equipe@rdv-solidarites.fr**](mailto:equipe@rdv-solidarites.fr)** pour communiquer avec nous, dans la mesure où vous ne transmettez par d'information sensible**. Chaque sujet, question, problème que vous avez pourrait intéresser d'autres territoires. Merci !

### Sujets à venir

Le prochain ticket actuellement prioritaire d'après le tableau est la possibilité d'ajouter un lieu tiers dans le tunnel de prise de RDV. Cela devrait permettre une saisie libre de lieu, et donc l'ajout d'une URL pour une visioconférence ou bien une adresse temporaire qui ne justifie pas la création d'un lieu.

Suite à la réunion référente précédente, nous avons suffissament avancé sur le sujet du décloisonnement des services. Nous avons des tickets à créer et à ajouter dans le tableau de priorisation. Le thème sera l'autonomisation.

### PMI

Au niveau nationale, il est demandé aux personnes travaillant en PMI de lister leurs actes. C'est au logiciel métier de le faire. Mais certaines personnes travaillant en PMI qui n'ont pas de logiciel métier, ou qui en souhaite pas l'utiliser, ont demandé à pouvoir saisir des actes dans RDV-Solidarités.

Ce n'est clairement pas la finalité du service.

Les personnes travaillant en PMI dans les Pyrénées Atlantique et dans la Drôme n'ont pas d'outil métier pour la PMI (ou ne s'en servent pas ?).

Il y a une envie des agents de pouvoir saisir de manière anonyme (sans mettre les références usagers), alors que les logiciels métiers demande à saisir le nom d'un bénéficiaire.
