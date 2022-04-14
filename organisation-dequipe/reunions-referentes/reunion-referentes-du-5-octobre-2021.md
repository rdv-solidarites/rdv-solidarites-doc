---
description: >-
  Incident de mercredi 29 septembre, Doublon dans la page référent, Nouveaux
  tickets dans le tableau de priorisation, Décloisonnement, Informations BizDev
---

# Réunion référentes du 5 octobre 2021

### Réalisation de la semaine

* [Éviter le timeout en cas d’erreur de connexion superadmin #1764](https://github.com/betagouv/rdv-solidarites.fr/issues/1764)

Et des éléments améliorant les performances.

### Incident de mercredi 29 septembre

Il y a eu un court moment où l'application n'a pas répondu à 2 reprise. Voir le rapport d'incident [https://doc.rdv-solidarites.fr/informations-generales/informations-generales-et-legales-1/incidents/incident-du-29-septembre-2021](https://doc.rdv-solidarites.fr/informations-generales/informations-generales-et-legales-1/incidents/incident-du-29-septembre-2021)

### Doublon dans la page référent

Christelle (64) signale un problème de doublon dans la page de gestion des agents référents d'une fiche usager.

Non reproduit pour le moment, le problème est peut-être lié à une condition particulière. Christelle revient vers nous avec l'exemple qu'elle a eu.

### Nouveaux tickets dans le tableau de priorisation

Nous avons parcouru les tickets ajoutés au tableau de prio le lundi 4 en fin de journée. Certains n'ont pas soulevé de question sur le moment. D'autres ont nécessité des clarifications et des modifications.

#### Export de liste de Motif

_C'est un ticket qui est directement dans le backlog dev vu le peu d'impact sur le quotidien des _~~_agents_~~_ professionnels_

[https://github.com/betagouv/rdv-solidarites.fr/issues/1781](https://github.com/betagouv/rdv-solidarites.fr/issues/1781)

Après discussion, il a été décider de modifier le ticket pour limiter l'accès a la liste des motifs aux agents administrateur.

Un des arguments clefs est le fait que rendre visible l'ensemble des motifs, y compris ceux qui ne sont pas ouvert aux usagers pour une prise de rendez-vous autonome pourrait créer des difficultés. Certains usagers souhaitant peut-être vouloir prendre rendez-vous sur ces motifs réservé à un usage par les agents.

#### Décloisonnement agenda par agenda

Ce ticket va nous amener à (enfin) avoir un seul agenda par agent. Faut-il maintenir un lien entre une organisation et

* une absence
* une plage d'ouverture
* un RDV
* un usager (et son profil)

Pour vraiment décloisonner, nous devons casser le lien entre un RDV et une organisation. Sans doute faut-il casser l'ensemble des liens évoquer ci-dessus.

**Ces suppressions pourront être réalisées dans d'autres tickets, sauf celle du RDV ? ???**

Ainsi, un usager sera accessible dans l'ensemble des organisations d'un territoire à partir du moment où il a été créé.

Ce point donne lieu à un nouveau ticket [Associé les usagers aux territoires plutôt qu'aux organisations #1786](https://github.com/betagouv/rdv-solidarites.fr/issues/1786)

Au moment où on ouvre un accès à une organisation pour un agent, il serait pratique de lui donner les accès en écriture aux agendas des autres agents de cette organisation et du même service. Attention au secrétaire. Cet élément a été ajouté au ticket.

Accès en lecture sans détail ? Est-ce bien nécessaire ? Qui en aurait besoin ? Peut-être pour le 80, dans le cadre du CPEF. Pour le 64 aussi ? Cas sage-femme qui fait PMI et CPEF (2 organisations). Rendre visible ces disponibilités.

* Pour les rdv de PMI
  * accès lecture sans détail pour les agents du CPEF
  * accès lecture avec détail pour les agents de PMI
* Pour les RDV de CPEF&#x20;
  * accès lecture avec détail pour les agents du CPEF
  * accès lecture sans détail pour les agents de PMI

Cet échange à permis de préciser que nous utiliserons 3 niveaux d'accès : lecture sans détail, lecture avec détail et écriture.

Élodie a également évoqué le fait de pouvoir copier la configuration d'accès d'un agent à un autre. Cela simplifierais pas mal la configuration. C'est à voir dans un autre ticket. Une autre option serait de pouvoir appliquer des droits d'accès à un groupe d'agent. Cette dernière option nécessiterait de mettre en place les groupes d'agents au préalable.

### Page d'accueil agent

_Ce ticket n'est pas dans le_ décloisonnement __ [https://github.com/betagouv/rdv-solidarites.fr/issues/1783](https://github.com/betagouv/rdv-solidarites.fr/issues/1783)

L'objectif de ce ticket est surtout d'inviter les ~~agents~~ professionnels à renseigner le status des rendez-vous passé. Les référentes ont suggéré qu'il y avait sans doute une approche plus simple et plus direct. C'est très juste.

Voici un ticket pour essayer de faire rapidement quelque chose [https://github.com/betagouv/rdv-solidarites.fr/issues/1788](https://github.com/betagouv/rdv-solidarites.fr/issues/1788)

### Informations BizDev

* Le Var est très bien parti pour rejoindre le consortium début 2022.
* Il y a une rencontre ce mardi avec la [Sonum](https://societenumerique.gouv.fr) et les conseillers numériques
* RDV-Solidarités sera présentée par Radia lors d'un webinaire de l'association [Les interconnectés](https://www.interconnectes.com)

### Colonne de poids dans le tableau de prio

Il serait intéressant de rendre visible le poids des tickets dans le tableau de prio.
