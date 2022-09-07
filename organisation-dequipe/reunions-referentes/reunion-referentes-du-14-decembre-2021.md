---
description: Démo, Roadmap et avancement de l'équipe, Retrouver l'usager, Droits d'accès
---

# Réunion référentes du 14 décembre 2021

### Démo

* Nouveautés sur les Webhook : il est possible de choisir les évènements auxquels s'abonner
* Correction des erreurs de chargement de l'agenda
* Amélioration de la remontée d'erreur en cas de problème dans l'agenda
* La page proposant un guide pour les « Premiers pas » n'est maintenant visible que pour les admins
* Nouveau processus d'invitation permettant de proposer la prise de rendez-vous à un usager pour un motif non ouvert en ligne
* Nouveau moteur de calcul de créneau

Nous avons également découvert un problème lors de la démonstration sur la distinction des agents dans l'affichage des créneaux disponibles

### Retrouver l'usager

Il est parfois difficile de retrouver un usager. La recherche ne propose que les usagers présents dans l'organisation. Pour « affecter » un usager à l'organisation, il faut commencer à faire la saisie, et à la validation (à la fin donc !), un message indique que cet usager existe déjà et que nous pouvons le rapatrier.

Il semble plus intéressant de « décloisonner » les usagers en faisant en sorte qu'ils ne soient affecté qu'au territoire.

[Décloisonner les usagers](https://github.com/betagouv/rdv-solidarites.fr/issues/1934)

### Roadmap

Échange sur le manque d'avancement sur les nouvelles fonctionnalités. Cela fait plusieurs mois (depuis septembre) que l'équipe travail principalement à maintenir l'application en ligne et utilisable. Il y a eu peu d'avancer sur de nouvelles fonctionnalités.

L'équipe espère trouver le bon rythme qui va lui permettre de maintenir l'application en ligne tout en ajoutant de nouvelles fonctionnalités.

Nous parlons également de l'avenir du tableau de priorisation actuel. Que va-t-il devenir avec la Roadmap ?

La Roadmap permettra de définir de grand sujet à mettre en place. Le tableau de priorisation liste des fonctionnalités à une granularité plus petite. Nous ferons sans doute disparaitre ce tableau à terme. En attendant, l'équipe s'en servira pour traiter les tickets les plus importants en premier.

### Les droits d'accès

faire la liste des fonctionnalités qui pourrait être couverte sur les droits d'accès et la partager avec les référentes. Cela permettra de vérifier que la granularité convient.

L'idée étant de ne plus avoir 3 niveaux d'autorisation :

* agent
* admin d'organisation
* admin territorial

Mais plutôt une liste d'activités qui sont accessibles (à l'instar de ce qui est envisagé sur les motifs et les agendas dans le thème `Décloisonnement`)
