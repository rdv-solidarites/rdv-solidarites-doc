---
description: >-
  Démo ; Ma santé 2022 ; Cloisonnement usager ; Instruction de RDV ; RDV
  Collectif
---

# Réunion référentes du 12 octobre 2021

### Démo

* [Mettre à jour les libellés de motifs de l’environnent de démo #1704](https://github.com/betagouv/rdv-solidarites.fr/issues/1704)
* [Nettoyer service PMI pour la Somme #1748](https://github.com/betagouv/rdv-solidarites.fr/issues/1748)
* [Indiquer l’horaire du créneau choisi pendant toutes les étapes du tunnel de création de Rdv #1706](https://github.com/betagouv/rdv-solidarites.fr/issues/1706)

_Nous avons détecté une erreur qui_ rendrait _impossible la prise de rendez-vous. Tout est rentré dans l'ordre en fin de matinée, c'était un problème de déploiement_

Le service PMI reste visible coté usager pour le 80, pourquoi ? Un ticket a été créé pour s'assurer que l'investigation sera faite https://github.com/betagouv/rdv-solidarites.fr/issues/1798

### Ma santé 2022

> Annoncée en septembre 2018 par le président de la république, la stratégie Ma santé 2022 propose une vision d’ensemble et des réponses globales aux défis auxquels est confronté le système de santé français. Tout d’abord, des inégalités dans l’accès aux soins, avec de plus en plus de Français qui connaissent des difficultés à accéder à un médecin dans la journée et sont parfois contraints de se rendre aux urgences par défaut. Ensuite, des aspirations chez les professionnels à mieux coopérer entre eux, à disposer de davantage de temps pour soigner leurs patients et à être formés autrement.

[Ma santé 2022 : un engagement collectif](https://solidarites-sante.gouv.fr/systeme-de-sante-et-medico-social/masante2022/)

Contient un agenda pour l'assuré social.

Comment se brancher avec RDV-Solidarité ?

Il existe des financements possibles pour la mise en conformité avec l'agenda. RDV-Solidarités pourrait sans doute participer d'une manière ou d'une autre à cet engagement !

Attention, c'est sur l'année à venir.

### Nouveaux tickets du tableau de prio

#### Cloisonnement usager

[Associé les usagers aux territoires plutôt qu'aux organisations #1786](https://github.com/betagouv/rdv-solidarites.fr/issues/1786)

Dans la Somme, on maintient un usager par organisation CPEF et MDPH pour bien cloisonner les usagers. L'intérêt, c’est de protéger le panier de rendez-vous. Les rendez-vous restant inaccessible d'une organisation à l'autre, ce n'est pas un problème.

Pour le 77, c’est une bonne idée, pour éviter les doublons.

#### Instruction avant RDV

[Afficher l'instruction d'un motif le plus tôt possible #179](https://github.com/betagouv/rdv-solidarites.fr/issues/1790)

Profiter de ce ticket pour ajouter l'information durée du rendez-vous dans la fenêtre de confirmation.

Maintenir l'utilisation d'une fenêtre de type « popup » permet de proposer un bouton « accepter » qui force un peu à lire.

Si un usager clic un peu vite, il faudrait pouvoir « revoir » les instructions.

Est-ce que ces instructions ne sont pas en fait des « prérequis » ? Changer le vocabulaire est-il nécessaire ?

Ne plus avoir des instructions « après » mais plutôt à la sélection du créneau. C'est un point qui nécessite un nouveau ticket. https://github.com/betagouv/rdv-solidarites.fr/issues/1799 Ce ticket a également été ajouté au tableau de prio.

### Rendez-vous Collectif

_Nous avons amorcé les discussions autour de ce grand thème. Les notes sont un peu en vrac, et j'envisage de les laisser comme ça. La prochaine session permettra peut-être de revenir dessus pour les organiser justement_

Sophie (26) fait déjà des RDV collectifs avec RDV Solidarités.

Action collective essentiellement cotée PMI avec plusieurs motifs. Mais pour faciliter, pour le moment, c'est un seul motif « Action Collective » qui est paramétré.

**Il serait intéressant d'avoir un motif avec le nom de l'action collective.**

Dans le SMS envoyé il n'y a que le nom du service, et pas le motif... Mais par contre, le type de RDV :bulb:

Les actions collectives ont des durées différentes.

Sophie a créé un agenda spécifique pour y placer les actions collectives avec l'adresse générique du CMS (parce que l'agenda de cette adresse n'est pas utilisé).

L'usager, c’est donc de convoquer 3 personnes à la même heure avec 3 créneaux différents pour faire 3 groupe de 3. Les agents fond du surbooking sur un RDV Pas possible de les inscrire au fur et à mesure, il n'y a pas d'envoi de SMS lorsqu'un ajoute une deuxième personne sur un rdv. La pratique, c’est du coup de faire 1 rdv par usager à la même heure avec le même agent pour que chacun ait son SMS, c'est en fait le même RDV. Ça évite d'avoir à gérer la liste d'attente. Pas de recherche de créneau possible, pas d'ouverture à l'usager possible...

**Il serait intéressant d'avoir une liste d'attente, pour laisser ouvert en attendant que le créneau soit rempli**

Autre option utilisée : convoquer 10 à 15 personnes à la même heure.

Sandra (80) : test autour des actions collectives sur RDV-Soldiarités.

Pour un forum (60 personnes). Plusieurs personnes convoquées sur une demi-journée. **Sur quel agenda mettre le ou les RDV ?** Un RDV par personne sur le même horaire == 60 petits RDV sur la même période **Comment gérer la liste des RDV non** renseignée **par la suite ?**

Pour une semaine avec des partenaires qui reçoivent des personnes sur des créneaux horaires. Sorte de « job dating ». Plusieurs partenaires à la même heure. **Quel agenda utiliser ?**

Utilisation du non de lieu pour afficher l'action collective dans le SMS.

Pour organiser des ateliers lecture et préparation à la naissance. On invite 2 ou 3 personnes sur un RDV. Difficulté de l'ouverture usager.

Pouvoir ouvrir une liste d'attente pour l'inscrire sur un créneau, avec une limite sur le nombre de personnes (max). Laissé ouvert tant que le max n'est pas atteint.

Sur quel agenda ? Celui du ou des professionnelles qui sont animateurs de l'action collective ? Comment préciser le nom de l'action collective dans le SMS ? Comment afficher le nom des usagers sur la fiche d'un RDV d'action collective ? Aujourd'hui, c'est un rdv par personne dans les bidouilles. Comment faire autrement et plus proprement ?

Dans le cadre d'une réunion d'information RSA, Assistante familiale, ... Action collective à l'initiative de la MDS. Ce sont les agents qui envoient une invitation. Comment je peux inscrire un de mes bénéficiaires à une action collective qui se passe sur mon territoire (regroupement de 3 MDS) sur une autre organisation ? Problème d'accès vu le cloisonnement actuel par organisation.

Qu'est-ce qu'une action collective ? Est-ce que c'est un motif ? Est-ce que c'est un type de rdv ? Est-ce que ça ressemble à une plage d'ouverture / absence ?

Utiliser le type de rdv permet de l'afficher dans les notifications.

Certaines actions collective se répète. D'autres non... Passer par une configuration malgré tout ?

Quel nom utiliser pour le type de RDV ? Puisqu'il apparait actuellement dans les notifications, ça semble important.
