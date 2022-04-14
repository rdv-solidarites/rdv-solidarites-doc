# Réunion référent.e du 4 mai 2021

## Réunion référente du 4 mai 2021

Voici l'ODJ de la réunion du 4 mai 2021 et le détail de la priorisation des fonctionnalités pour cette semaine.

### Démo

Les nouveautés de la plateforme depuis le 27 avril.

* [Proposer les bons créneaux disponibles](https://github.com/betagouv/rdv-solidarites.fr/issues/1382)
* [Corriger la recherche sectorisée quand un numéro est indiqué](https://github.com/betagouv/rdv-solidarites.fr/issues/1363)
* [Clarifier les textes à propos de l'acceptation des notifications de la fiche usager](https://github.com/betagouv/rdv-solidarites.fr/issues/1377)
* [Pouvoir se connecter avec un compte existant avec numéro de téléphone sans email](https://github.com/betagouv/rdv-solidarites.fr/issues/1327)
* [Désactiver un lieu pour ne plus le voir dans la liste des lieux possible](https://github.com/betagouv/rdv-solidarites.fr/issues/1341)
* [Envoyer des notifications mails avec fichier ICS aux agents pour les absences](https://github.com/betagouv/rdv-solidarites.fr/issues/1051)
* [Investiguer le bouton "prochain créneau" n'apparait pas toujours](https://github.com/betagouv/rdv-solidarites.fr/issues/1239)
* [Investigation : Plus de créneau disponible en cas de chevauchement de plage d'ouverture](https://github.com/betagouv/rdv-solidarites.fr/issues/1340)

### Développement en cours

Les tickets en cours de réalisation ou de test au 4 mai.

* [Numéro de téléphone d'un lieu bien présent dans le SMS](https://github.com/betagouv/rdv-solidarites.fr/issues/1414)
* [Affiner l'accès aux rendez-vous de suivi](https://github.com/betagouv/rdv-solidarites.fr/issues/1326)
* [Agenda agents inter-organisations](https://github.com/betagouv/rdv-solidarites.fr/issues/1185)
* [Configuration des envois de SMS par territoire](https://github.com/betagouv/rdv-solidarites.fr/issues/1408)

_Liste sur le_ [_tableau de développement_](https://github.com/betagouv/rdv-solidarites.fr/projects/8?fullscreen=true).

### Priorisées

À ce jour, un ticket \[S] est traité en moyenne en 1 journée, \[M] est traité en 8 jours, \[L] en 18.

* \[S] [Changement de status d'un rendez-vous pour un agent qui n'est plus attaché à l'organisation](https://github.com/betagouv/rdv-solidarites.fr/issues/1413)
* \[L] [Envoyer un email avec .ics à l'agent pour chaque RDV](https://github.com/betagouv/rdv-solidarites.fr/issues/1059)
* \[M] [Faciliter la recherche d'usager existant](https://github.com/betagouv/rdv-solidarites.fr/issues/1348)
* \[M] [Envoyer les notifications d'annulation d'un rendez-vous, même s'il a été supprimer avant l'envoi](https://github.com/betagouv/rdv-solidarites.fr/issues/1361)
* \[S] [Retour sur la page de mon secteur dans la liste des secteurs](https://github.com/betagouv/rdv-solidarites.fr/issues/1346)
* \[M] [Investiguer le problème synchronisation de mise à jour et suppression de plage d'ouverture et absence](https://github.com/betagouv/rdv-solidarites.fr/issues/1354)
* \[S] [Distinguer la démo / formation de la prod](https://github.com/betagouv/rdv-solidarites.fr/issues/1058)
* \[M] [Inclure la commune de l'usager responsable dans l'export](https://github.com/betagouv/rdv-solidarites.fr/issues/1187)
* \[S] [Modification des référents d'un autre service](https://github.com/betagouv/rdv-solidarites.fr/issues/1405)
* \[S] [ Rendre visible les statistiques par organisation #1404 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1404)

Pour voir la [liste de tous les tickets](https://github.com/betagouv/rdv-solidarites.fr/issues?q=is%3Aissue+is%3Aopen) ou bien [la colonne backlog sur le tableau du projet](https://github.com/betagouv/rdv-solidarites.fr/projects/8?fullscreen=true).

Nous mettons chaque ticket qui entre dans la colonne backlog, puis nous en sélectionnons 10 qui nous semble les plus importants sur le moment.

Prenez le temps de regarder les tickets. Lors de la réunion, nous pourrons clarifier certains tickets si besoin, nous pourrons aussi discuter de la priorisation, changer l'ordre si nous arrivons à une forme de consensus.

N'hésitez pas à regarder la colonne « Backlog » également. Peut-être qu'un des 10 tickets ici à moins ça place qu'un autre. Faite le nous savoir.

### Retour sur l'incident du 29 avril 2021

[Dans la matinée du 29 avril, nous avons eu deux incidents simultanés qui ont rendu l’accès du site très difficile, voire impossible, pour les usagers et pour les agents](https://forum.rdv-solidarites.fr/t/incident-de-production-du-29-avril-2021/241).

Tout est rentré dans l'ordre en fin de matinée. Aucune perte de données. Par contre, nous avons du retiré la fonctionnalité des [agendas inter-organisation](https://github.com/betagouv/rdv-solidarites.fr/issues/1185) pour la retravailler.

### Formation et démo

Pour les démos, nous allons les réaliser à la demande plutôt que d'organiser des webinaires bimensuels.

Pour les formations, nous allons nous positionner en support de la formation. Les départements organisent déjà en partie leur formation interne.

[https://forum.rdv-solidarites.fr/c/formation-demo/12](https://forum.rdv-solidarites.fr/c/formation-demo/12)

Pour faciliter les formations et l'usage de la plateforme de démo, il serait bien d'avoir les motifs de production. Peut-être même copie toute la production d'une organisation, sans les usagers, les RDV, les plages d'ouverture et les absences.

Organiser un atelier spécifique autour de la formation semble la bonne chose.

**Il faut dissocier démonstration et formation.**

### Atelier Cellule familiale et notification multiple

Après avoir récolté [vos avis sur vos disponibilités](https://forum.rdv-solidarites.fr/t/atelier-cellule-familiale-et-notifications-multiples/243), nous allons organiser un atelier d'une heure pour parler des problématiques lié à la cellule familiale et aux notifications multiple.

Un compte rendu sera proposé sur le forum et les discussions resterons ouvertes après cet atelier. Si vous ne pouvez pas participer, n'hésitez pas à vous exprimer sur le forum.

### Atelier Statistique

Proposition de dates pour un Atelier Statistiques : Qui seraient intéressés ? RETEX sur vos usages et besoins.

### Tri par ordre alphabétique perturbant

Attention, les listes d'usagers et d'agents sont trié par ordre alphabétique du nom alors que c'est le prénom qui est affiché en premier. Ça fait très bizarre. Peut-être faut-il afficher Nom - prénom dans la liste.

### Changement de statut et notification masquée

Quand on annule un RDV via le changement de Statut, RDV-Solidarités envoie une notification sans informer l'agent que la notification va partir. Lorsqu'on appuie sur le bouton annuler le système nous informe qu'une notification va partir. Peut-être faut-il faire la même chose ?
