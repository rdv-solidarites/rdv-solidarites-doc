---
description: >-
  Démo ; Champs sociaux ; Performance ; Motif invisible ; Retours ; Finalité de RDV-Solidarités ; Atelier RDV Collectif
---

# Réunion référentes du 19 octobre 2021


## Démo

- [Tracabilité de la fiche usager #1675](https://github.com/betagouv/rdv-solidarites.fr/issues/1675)

En plus de la traçabilité usager, il a été ajouté le fait de pouvoir suivre les modification d'un agent, d'un motif, d'une organisation.
Il a été demandé pendant la démo de le faire aussi pour les plages d'ouvertures et les absences. [Traçabilité plages d'ouverture et absences #1813](https://github.com/betagouv/rdv-solidarites.fr/issues/1813)

## Champs sociaux

Nous avons reparlé des champs du social de la fiche usager. Sans doute parce que nous les avons vu lors de la démo de l'historique usager.

La demande est forte dans les départements. Reste le Pas-de-Calais qui pour le moment n'envisage pas de s'en passer.
Un piste serait la mise en place d'un élément de configuration. Un peu lourd pour un seul département ? Avons nous des précédents sur d'autres sujet ?

Ajout d'un ticket pour ajouter le [paramétrage d'utilisation de ces champs sociaux](https://github.com/betagouv/rdv-solidarites.fr/issues/1814). Ce ticket est ajouté au tableau de priorisation.


Nous avons reparler de l'utilisation du champ remarque. Il y a beaucoup de cas où ce champs contient un complément d'adresse, et beaucoup d'autres où il y a un numéro de dossier. Il serait intéressant d'avoir des champs dédiés pour ces informations, et de geler le champs remarque. Une fois un paramétrage des champs utilisées en place, chaque département pourrait « configurer » la fiche usager en fonction de son usage.

Ajout d'un ticket à propos de la [création d'un champ « complément d'adresse » et de deux champs pour les « numéros de dossier social et PMI »](https://github.com/betagouv/rdv-solidarites.fr/issues/1815). C'est un petit pas vers la réduction de l'utilisation du champ remarque.

Je l'évoque dans le ticket : à ce jour, il y a un peu plus de 20 000 remarques sur un peu moins de 180 000 usagers.
La Seine-et-Marne, avec un déploiement sur tout le territoire en PMI, CPEF et Social à un peu plus de 10 000 champs remarques non vide. Suit le Pas-de-Calais avec plus de 2 000 champs non vide. Les Pyrénées Atlantique et la Somme suivent avec respectivement autour de 1 000 et 800 remarques non vide.

Nous pourrions basculer ce champ remarque en lecture seule à un moment. Ça permettrait de ne pas perdre l'information qui a été mise dedans, et ça bloquerais de nouveau usage de ce champs. Peut-être que ça ferait remonter des besoins du terrain.

Nous avons aussi rapidement abordé le lien de RDV-Solidarités vers les applications métiers. Faire ces liens permettrait sans doute d'envoyer un message clair que RDV-Solidarités est là pour la prise de rendez-vous, et que pour le reste, il y a les applications métier. Il restera à évoque le cas des départements qui n'ont pas d'application métier ou qui ne souhaite pas l'utiliser. Une opportunité pour une autre expérimentation territoriale ?


## Performance

Amélioration sensible. 20 % plus rapide en général. Il nous reste des « points durs ». Assez spécifique. Merci de nous transmettre les informations en précisant bien le scénario à partir duquel vous constaté les problèmes de performance.

Un des gros problème restant est sur la recherche de créneau coté agent (et coté usager ?)... Signalé par le Calvados. Est-ce qu'il y a d'autres département qui ont remarqué ça ? Nous sommes en train de travailler dessus.

Élodie (62) a constaté des lenteurs lors de l'enregistrement d'une commune sur un secteur un peu long. Étant lié à l'administration territorial, nous n'allons pas en faire une priorité pour le moment.

## Motif invisible

Traiter la visibilité du rendez-vous au moment de la prise de rendez-vous plutôt que dans la configuration de motif. Un point ajouté dans le ticket en cours de réalisation à propos du débraillage de notification dans le tunnel de prise de RDV.

La description du ticket à été revue en conséquence [Débrayer l’envoi de notification au rendez-vous #1617](https://github.com/betagouv/rdv-solidarites.fr/issues/1617).


## UX et design d'interface

- Maintenir l'affichage des jours de la semaine sur l'agenda (comme dans Excel).
- Pouvoir changer les status de RDV depuis un smartphone.

Ces deux points ont été ajouté dans l'onglet des thèmes à discuter.

## Lieu de rendez-vous

> Pourquoi le lieu n'est pas prérempli lorsque l'on clic sur l'agenda, sur une plage d'ouverture, pour poser un rendez-vous ?
> -- Magalie (22)

Les rendez-vous ne sont pas associé à une plage d'ouverture. Conséquence : si je clic dans l'agenda sur une plage d'ouverture (permanence) le lieu n'est pas prérempli dans le tunnel de prise de rendez-vous.

## Couleurs des absences

Est il envisageable de mettre en place un choix de couleurs dans les absences ? Pas vraiment dans les objectifs. Un ticket existe [Personnaliser les couleurs des absences / indisponibilités #1521](https://github.com/betagouv/rdv-solidarites.fr/issues/1521). Ce n'est pas du tout prioritaire.

## Import de liste d'usager

> suite à ma rencontre avec la DEEI qui teste DATA-Insertion sur la Drôme et fixe les RDV avec RDVS, j'ai constaté que leur fichier usager était créé à partir d'un fichier excel transmis par la CAF. Ils m'ont dit que toutes les informations du tableau permettait de créer automatiquement les usagers dans RDVS....
> Serait il envisageable, afin de soulager nos secrétariats qui saisissent un par un tous les usagers de leur organisation d'envisager la même solution pour nous ?

Data.insertion utilise l'[API usager proposé par RDV-Soldiarités](https://doc.rdv-solidarites.fr/pour-un-charge-informatique/api-interconnexions-entrantes/api-usagers). Ils ont même fait évoluer l'API pour quelle réponde mieux à leur besoin.

Un développement spécifique pourrait être réalisé par une équipe (DSI du département, prestataire, ...) pour utiliser l'API pour faire de la création d'usager via l'API (à partir des logiciels métiers ?).

> Et si oui, de faire pareil pour la sectorisation ?

Il existe déjà un mécanisme d'import de fichier pour la sectorisation. Voir la [documentation « pour un territorie/sectorisation-geographqiue »](https://doc.rdv-solidarites.fr/pour-un-territoire/sectorisation-geographique).

## Finalité de RDV-Soldiarités

Discussion sur la finalité de RDV : prise de RDV ou agenda ? Plutôt prise de RDV. Cependant, certains département éprouve des difficultés à utiliser leur agenda en plus de RDV-Solidarités. En grande partié lié a l'absence de synchronisation de l'agenda vers RDV-Soldiarités.

Certains département garde les rendez-vous historique dans leur agenda. Cela leur permet de faire des statistique annuel en fin d'année.

Il y a également la question de la prise de rendez-vous directement dans l'agenda plutôt que par recherche de créneau. Autour de 70 % de prise de RDV via l'agenda pour le Pas-de-Calais.

## Metabase / Statistique

Pas vraiment pratique, et si on l'enlève, est-ce que ça pose un problème ? Vérifier avec la Seine-et-Marne. Elles ont été les premières utilisatrice. Elles le sont peut-être encore.

## Organiser un atelier sur les RDV collectifs

Pour faire avancer le travail sur ce sujet, nous avons convenu d'organiser un atelier spécifique sur les RDV Collectif. Prévoir 2 heures.

[Vous pouvez voter sur le créneaux qui vous conviens le mieux sur le framadate](https://framadate.org/v6XiaWzb1jjUQmGX).


