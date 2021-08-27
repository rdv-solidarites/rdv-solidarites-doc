# Réunion référent.e du 18 mai 2021

### Démo

Les nouveautés de la plateforme depuis le 11 mai 2021.

_Aucune livraison sur cette période_

### Développement en cours

Les tickets en cours de réalisation ou de test au 4 mai.

* [Configuration des envois de SMS par territoire](https://github.com/betagouv/rdv-solidarites.fr/issues/1408)
* [ Envoyer un email avec .ics à l'agent pour chaque RDV \#1059 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1059)
* [ Afficher le bloc de statistique des rendez-vous par statuts \#1427 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1427)

_Liste sur le_ [_tableau de développement_](https://github.com/betagouv/rdv-solidarites.fr/projects/8?fullscreen=true).

### Priorisées

À ce jour, un ticket \[S\] est traité en moyenne en 1 journée, \[M\] est traité en 7 jours, \[L\] en 14.

* \[S\] [ Changement de status d'un rendez-vous pour un agent qui n'est plus attaché à l'organisation \#1413 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1413)
* \[M\] [ Faciliter la recherche d'usager existant \#1348 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1348)
* \[M\] [ Envoyer les notifications d'annulation d'un rendez-vous, même s'il a été supprimer avant l'envoi \#1361 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1361)
* \[S\] [ Retour sur la page de mon secteur dans la liste des secteurs \#1346 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1346)
* \[M\] [ Investiguer le problème synchronisation de mise à jour et suppression de plage d'ouverture et absence \#1354 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1354)
* \[S\] [ Distinguer la démo / formation de la prod \#1058 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1058)
* \[M\] [ Inclure la commune de l'usager responsable dans l'export \#1187 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1187)
* \[M\] [ Modification des référents d'un autre service \#1405 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1405)
* \[S\] [ Rendre visible les statistiques par organisation \#1404 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1404)

Pour voir la [liste de tous les tickets](https://github.com/betagouv/rdv-solidarites.fr/issues?q=is%3Aissue+is%3Aopen) ou bien [la colonne backlog sur le tableau du projet](https://github.com/betagouv/rdv-solidarites.fr/projects/8?fullscreen=true).

### Problématique des agendas cloisonné par service

62 : un agent dois pouvoir accéder à l’agenda des autres personnes.

* Lecture seule \(affichage des indisponibilités\)
* lecture plus écriture

Un agent seul dans une organisation aurait besoin de voir les agendas d'agents dans d'autres orgas -⇾ Oui situation possible -⇾ Nécessité d'avoir un accès multiorganisation

Sur le 92 : les agents chargés de l'accueil téléphonique prennent les RDV sur tout le département. Pour y arriver, on va leur ouvrir des accès à toutes les orgas.

Q - Un agent hors de l'organisation peut-il visualiser les rendez-vous en mode anonyme ou détaillé ?

\(sujet Forum d'Élodie [https://forum.rdv-solidarites.fr/t/etendre-la-vue-de-mon-agenda-multi-organisation-a-l-ensemble-de-mon-service/254/2](https://forum.rdv-solidarites.fr/t/etendre-la-vue-de-mon-agenda-multi-organisation-a-l-ensemble-de-mon-service/254/2)\)

Note à propos des notifications : nous ne pouvons pas mettre le motif dans une notification pour garantir une forme de discrétion, de protection \(IVG, etc.\).

### Point RGPD convention

L'équipe va reprendre la lecture de la proposition de convention des DPO.

Nous allons aussi refaire une passe sur les aspects légaux, obligatoire lié au RGPD.

L'équipe enverra un email avec une description de ce que nous pouvons faire et ce que nous ne ferons pas, avec un délai de réponse.

### Cellule familiale & notifications multiples

[https://forum.rdv-solidarites.fr/t/atelier-cellule-familiale-et-notifications-multiples-jeudi-6-mai-2021-11h/247/2](https://forum.rdv-solidarites.fr/t/atelier-cellule-familiale-et-notifications-multiples-jeudi-6-mai-2021-11h/247/2)

Nous allons mettre au propre nos notes et réflexion, puis lancer des sujets plus spécifiques sur les premières actions à mettre en place.

### Interface usager : choisir un motif

Pour le 77, devoir choisir un service pour choisir un motif coté usager est un frein ! Pour le 64 ce n'est pas évidant non plus.

Yannick souhaite proposer une maquette pour changer l'affichage et la structure de cette page. Pas de changement en grande profondeur, simplement une présentation différente.

Questionnement sur les motifs : nationalisé avec un travail éditorial ? Laissé libre au département ? La première option nécessiterais un gros travail de consensus et de travail de formulation de la part de l'équipe. La deuxième option laisse les départements face à la problématique. _L'équipe peut-elle se positionner « simplement » en conseil sur ce point ?_

Difficulté de trouver les bons termes pour définir les motifs. Même le fait de savoir si je suis suivi ou pas, ce n'est pas si évidant.

Le 64 : l'uniformisation ne serait peut-être pas si gênante que ça.

