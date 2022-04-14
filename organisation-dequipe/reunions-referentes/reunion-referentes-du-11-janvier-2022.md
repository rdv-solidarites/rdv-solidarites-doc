---
description: RGAA, Visioconférence et tiers lieux, Droits d'accès,
---

# Réunion référentes du 11 janvier 2022

### À venir sur la production

Les livraisons de jeudi en production porterons sur des améliorations techniques.

### À venir dans la semaine sur la recette

#### RGAA

_sur cette semaine et les suivantes_

Mise en place de tests automatiques afin d'avancer sur l'accessibilité de RDV-Solidarités avant l'audit fin janvier ou courant février. Les tests automatiques permettent de ne pas faire marche arrière dans l'accessibilité lors de prochaines modifications de l'application. Quelques couleurs/style risquent de changer au cours des futures semaines.

#### Tiers lieux et visioconférence

[Tiers lieux et visioconférence pour un RDV #1639](https://github.com/betagouv/rdv-solidarites.fr/issues/1639)

Une demande à émergée de la réunion référente : pouvoir ajouter un nom au lieu que l'on ajoute de manière exceptionnelle à un RDV.

### Droits accès

Nous avons beaucoup parlé des droits d'accès.

Aujourd'hui RDV-Solidarités à 4 « profiles »

* agent
* agent du service secrétariat → Accède à tous les agendas de l'organisation, peu importe le service
* administrateur d'organisation → Comme le secrétariat + accède aux paramètres liés à une organisation
* administrateur de territoire → Comme l'administrateur d'organisation + accède aux paramètres liés à un territoire

Ce n'est pas très fin. Certains départements souhaiteraient ouvrir certaines actions plus largement et fermer certains accès aussi.

L'idée serait donc d'avoir, pour chaque agent, une liste d'action possible (ou pas). Nous avons fait une liste des actions que nous pourrions proposer.

* Inviter/retirer des agents sur mon organisation
* créer/modifier/supprimer des motifs dans une organisation
* créer/modifier/supprimer des secteurs
* affecter/retirer des secteurs
* créer/modifier/supprimer des lieux d'une organisation
* créer/modifier/supprimer des organisations
* créer/modifier/supprimer des webhook
* modifier la configuration d'envoi de SMS
* Modifier les droits d'accès agent
* visibilité des statistiques de l'organisation
* création/modifier/supprimer des plages d'ouvertures
* Est-ce que j'ai un agenda (sur une organisation)

Il faudra bien sûr pouvoir faire les attributions de droits d'accès de façon groupé (ex : autorisé la création d'organisation à tout un groupe d'agent d'un seul coup).

Une suggestion a été évoquée pour l'interface graphique : avoir un tableau avec en ligne les droits potentiel et une colonne par organisation. Il y aurait sans doute au-dessus de ce tableau a sélectionné un agent, une équipe, un service ou une organisation. Se pose alors la question du cas des droits différents au sein d'un même groupe ? Si dans l'équipe A un agent peut créer des organisations, mais pas les autres agents, comment sera l'affichage du tableau des droits lorsque l'on sélectionnera ce groupe ?

Nous avons évoqué un point qui sera pour l'étape des droits sur agenda : le niveau de visibilité des agendas (affichage du motif, du nom de l'usager) dans les agendas auxquels nous accédons.

### Roadmap

Nous avons reparlé de la Roadmap, pour rappel, avant de parler des droits d'accès. À cette occasion, il a été proposé de partager plus largement cette roadmap, particulièrement auprès des membres du COPIL. Plus à titre d'information que de validation.

Un email va être préparé et envoyé aux membres du COPIL

### Problèmes remontés lors de la réunion

#### lieux

Lorsqu'il n'y a qu'un seul lieu, celui-ci n'est pas systématiquement sélectionné. Il faut aller le chercher.

Il existe déjà un ticket sur le sujet [Sélectionner automatiquement le seul lieu disponible #1906](https://github.com/betagouv/rdv-solidarites.fr/issues/1906)

#### Ajout d'un agent référent pour un usager

Il y a des agents en double dans la liste des possibilités. Sans doute des agents multiorganisation.

[Afficher une seule fois les agents pouvant être référent #1998](reunion-referentes-du-11-janvier-2022.md#roadmap)
