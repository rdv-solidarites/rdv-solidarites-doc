# Réunion référente du 27 avril 2021

### Démo

Les nouveautés de la plateforme depuis le 13 avril.

* [Inviter un agent d'un autre service ne fonctionne pas, silencieusement](https://github.com/betagouv/rdv-solidarites.fr/issues/1281)
* [verrouille le formulaire en attendant le choix sur le message d'alerte](https://github.com/betagouv/rdv-solidarites.fr/issues/1293)
* [Mise à jour du numéro de téléphone à l’inscription](https://github.com/betagouv/rdv-solidarites.fr/issues/1328)
* [réparer réconciliation sur email pour FranceConnect](https://github.com/betagouv/rdv-solidarites.fr/issues/1237)
* [Vérifier le téléphone de l'usager responsable pour les rendez-vous téléphonique d'un proche](https://github.com/betagouv/rdv-solidarites.fr/issues/1334)
* [Dupliquer une absence de la même manière qu'une plage d'ouverture](https://github.com/betagouv/rdv-solidarites.fr/issues/1331)

Deux remarques / questions durant la démonstration :

> Dommage que agent ne puisse pas voir l'occupation d'un de ces collèges du même service, même s'il n'accède pas à l'autre organisation. Actuellement, avec l'agenda multi-organisation, nous pouvons voir l'agenda d'un collègue, mais uniquement les informations accessibles avec nos accès : service / organisation. Le besoin semble être de voir l'occupation, et non le détail nominatif des rendez-vous (permet d'envisager de préserver une confidentialité).
>
> Problème de mise à jour d'un statut de rendez-vous pour un agent qui n'est plus dans l'organisation.

C'est vrai que nous n'avons pas travaillé sur cet aspect mise à jour du statut de rendez-vous. Il y a cependant un moyen d'accéder aux rendez-vous ayant un statut « à renseigner », même si l'agent du rendez-vous n'est plus dans l'organisation. Depuis la liste des rendez-vous, filtrer sur le statut « à renseigner » et tous les rendez-vous seront visible et modifiable (pour l'agent admin)

### Développement en cours

Les tickets en cours de réalisation ou de test au 20 avril.

* [Agenda agents inter-organisations](https://github.com/betagouv/rdv-solidarites.fr/issues/1185)
* [Envoyer des notifications mails avec fichier ICS aux agents pour les absences](https://github.com/betagouv/rdv-solidarites.fr/issues/1051)
* [Corriger la recherche sectorisée quand un numéro est indiqué](https://github.com/betagouv/rdv-solidarites.fr/issues/1363)

_Liste sur le _[_tableau de développement_](https://github.com/betagouv/rdv-solidarites.fr/projects/8?fullscreen=true).

### Priorisation

À ce jour, un ticket \[S] est traité en moyenne en 1 journée, \[M] est traité en 8 jours, \[L] en 18.

* \[S] [Proposer les bons créneaux disponibles](https://github.com/betagouv/rdv-solidarites.fr/issues/1382)
* \[M] [Désactiver un lieu pour ne plus le voir dans la liste des lieux possible](https://github.com/betagouv/rdv-solidarites.fr/issues/1341)
* \[L] [Envoyer un email avec .ics à l'agent pour chaque RDV](https://github.com/betagouv/rdv-solidarites.fr/issues/1059)
* \[M] [Affiner l'accès aux rendez-vous de suivi](https://github.com/betagouv/rdv-solidarites.fr/issues/1326)
* \[M] [Pouvoir se connecter avec un compte existant avec numéro de téléphone sans email](https://github.com/betagouv/rdv-solidarites.fr/issues/1327)
* \[M] [ Plus de créneau disponible en cas de chevauchement de plage d'ouverture #1340 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1340)
* \[M] [Surveiller les tâches récurrentes](https://github.com/betagouv/rdv-solidarites.fr/issues/1026)
* \[S] [ investiguer le bouton "prochain créneau" n'apparait pas toujours #1239 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1239)
* \[S] [ Clarifier les textes à propos de l'acceptation des notifications de la fiche usager #1377 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1377)
* \[S] [ Retour sur la page de mon secteur dans la liste des secteurs #1346 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1346)

Pour voir la [liste de tous les tickets](https://github.com/betagouv/rdv-solidarites.fr/issues?q=is%3Aissue+is%3Aopen) ou bien [la colonne backlog sur le tableau du projet](https://github.com/betagouv/rdv-solidarites.fr/projects/8?fullscreen=true).

Nous mettons chaque ticket qui entre dans la colonne backlog, puis nous en sélectionnons 10 qui nous semble les plus importants sur le moment.

Prenez le temps de regarder les tickets. Lors de la réunion, nous pourrons clarifier certains tickets si besoin, nous pourrons aussi discuter de la priorisation, changer l'ordre si nous arrivons à une forme de consensus.

N'hésitez pas à regarder la colonne « Backlog » également. Peut-être qu'un des 10 tickets ici à moins ça place qu'un autre. Faite le nous savoir.

### Discussion libre

#### Questions

> Inquiétude au sujet des fiches responsables de proches. Il n'apparaît pas dans la liste des sujets priorisés. C'est un point important pour les agents. -- @Christelle-Cufay-64

Discussion amorcée sur le forum : [https://forum.rdv-solidarites.fr/t/responsable-du-dossier-ou-proche/97](https://forum.rdv-solidarites.fr/t/responsable-du-dossier-ou-proche/97). C'est loin d'être abouti, et il n'y a pas encore de solution claire qui apparaît.

Il y a un lien entre ce sujet et les notifications à plus d'une personne. Voir : [https://forum.rdv-solidarites.fr/t/notifications-gerer-lenvoi-des-notification-a-plus-dun-responsable/65](https://forum.rdv-solidarites.fr/t/notifications-gerer-lenvoi-des-notification-a-plus-dun-responsable/65).

Deux options évoquées rapidement pendant la réunion :

* permettre la saisie de numéro de téléphone et email à notifier en plus de la personne responsable (en fin de tunnel de prise de RDV)
* ajouter des responsables parmi une liste (nécessite d'avoir des fiches pour chacune de ces personnes)

_Niveau RGPD, ça serait pas mal de faire en sorte qu'on puisse ajouter des numéros à la volée, en tunnel, plutôt que d'ajouter des fiches._

**Décision d'organiser un atelier "cellule familiale et notification multiple"**. C'est parfois plus simple à l'oral. Quitte à reporter ensuite les apprentissages dans le forum.

#### Consultation nationale

[https://mon.incubateur.anct.gouv.fr/processes/transformation-numerique/f/10/proposals/602](https://mon.incubateur.anct.gouv.fr/processes/transformation-numerique/f/10/proposals/602) Créer un compte pour pouvoir soutenir RDV-Solidarités dans sa candidature. Cliquer à droite sur "Soutenir", après avoir créé un compte.

#### Gestion de salle

> Est-ce que dans Doctolib, module pour gérer les réservations de salle ?
>
> Non.

Aujourd'hui, le 62 utilise un contournement pour la gestion des salles, en invitant les salles (via leur adresse email) sur le rendez-vous une fois qu'il est synchronisé dans Outlook.

Ce n'est pas un sujet prioritaire, mais il revient souvent.

#### Groupe d'agents

Pourrait-on avoir la possibilité de créer des groupes d'agents pour faciliter la recherche de créneaux disponibles pour ces agents ? Il y a une question UX derrière ce besoin. Ça nécessiterait d'y réfléchir un peu plus. Pour le moment, c'est à noter pour plus tard.

#### Formation et démo

> Comment fonctionnent les webinaires maintenant ? Nous devons documenter notre nouvelle approche.

Des démos pour les nouveaux arrivants, des formations pour les territoires déjà installées. Le rôle du territoire (via la référente ?) dans la formation des agents. L'aide que nous pourrions mettre en place pour faciliter la formation.

> Et les capsules vidéo ? Comment y accéder ?

Une documentation sera à faire sur le forum ou la doc. Il sera intéressant aussi de faire des liens vers ces éléments depuis la page de support de RDV-Solidarités.
