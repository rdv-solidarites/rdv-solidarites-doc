---
description: >-
  Performance, Parcours usager, droit d'accès, adresse, fiche usager, référents,
  atelier à venir
---

# Réunion référentes du 29 mars 2022

### Performances

Nous continuons à mettre en place quelques modifications visant à améliorer les performances.

Il nous reste à mettre en place des améliorations pour le calcul de créneau.

### Lettre d'information

Nous allons expérimenter l'envoie d'une lettre d'information hebdomadaire.

### Parcours usager

Dans le cadre du processus d'invitation mis à place par Data.insertion, nous avons pu amorcer un nouveau parcours usager pour la prise de RDV.

Pour le moment, nous maintenons les deux chemins en parallèle. Pour tester le nouveau, vous pouvez vous rendre sur https://www.rdv-solidarites.fr/prendre\_rdv

Nous reparlons des « instructions » qui arrivent un peu trop tardivement ? [Afficher l'instruction d'un motif le plus tôt possible #1790](https://github.com/betagouv/rdv-solidarites.fr/issues/1790)

La page qui affiche la liste de motif pourrait être amélioré également avec

* un champ de recherche pour filtrer les motifs recherchés
* regrouper les motifs par service
* afficher les instructions en info bulle ? (avec un icône pour inviter à passer dessus i d'information ?)

### Invitation et accès aux organisations

Présentation des travaux en cours sur l'invitation et l'ouverture d'accès aux organisations d'agent depuis le module de configuration.

[Invite les agents depuis le module de configuration](https://github.com/betagouv/rdv-solidarites.fr/issues/2032) [Demo](https://production-rdv-solidarites-pr2283.osc-secnum-fr1.scalingo.io)

### Adresse

Nous revenons sur les problématiques d'adresse introuvable. Nous utilisons une autocomplétion basée sur la base adresse nationale. Or il manque parfois des numéros, et parfois des rues.

Faut-il découper la saisie de l'adresse en plusieurs champs ?

### Fiche usager

Les fiches usagers sont cloisonnées par organisation. Mais lorsque l'on crée une fiche, si l'usager existe déjà dans une autre organisation (éventuellement sur un autre territoire), nous proposons de le « copier ».

Ne pas pouvoir trouver les usagers directement au moment de la recherche, devoir créer la fiche avant d'avoir une proposition pour récupérer ce qui a été déjà saisi est gênant.

De plus, si l'on crée une fiche usager par organisation, au moment où l'usager crée un compte, il pourra prendre rendez-vous sur une organisation ou une autre, sans distinction.

Le cloisonnement est demandé par certains médecins dans le 14 (le 64 aussi sans doute). Ce sont les rendez-vous qui ne doivent surtout pas être visible.

### Agent référent

Est-ce c'est un référent par motif ? Est-ce qu'un usager peu avoir plusieurs référentes ? Oui.

Comment intégrer la sélection d'agent référent directement dans le formulaire usager ?

### Atelier à venir

* Mai / juin : journée de travail RDV-Solidarités à Paris. Si vous souhaitez participer, merci de préciser vos disponibilités sur le [sondage pour définir la date](https://framadate.org/Xinl6JkJuJ42oGsh)
* Septembre : 7ᵉ COPIL RDV-Solidarités. Merci de renseigner, pour les personnes concernées, [le sondage pour définir la date](https://framadate.org/GKDzkmeaQlAYgDJx)
