---
description: >-
  Droits d'accès, Contexte de RDV, Lieu ponctuel, Annulation et report de RDV
  coté usager
---

# Réunion référentes du 22 mars 2022

### Droits d'accès équipes

[Accéder à la configuration de l'équipe via des droits d'accès spécifiques #2210](https://github.com/betagouv/rdv-solidarites.fr/issues/2210)

Irène (83) partage son souhait de pouvoir centraliser dans le module de configuration, avec ouverture sur des droits d'accès fin pour

* l'invitation et la gestion des agents ;
* la gestion des lieux ;
* les équipes ;
* les motifs

L'objectif est effectivement de placer dans le module de configuration l'ensemble des éléments de paramétrages

* individuel (préférence de notification, email, mot de passe)
* « organisation » (motif, lieux, etc)
* « Départemental » (webhook, SMS, sectorisation, etc) Le tout en mettant en place de nouveaux droits d'accès part élément (ou famille d'élément).

### Contexte de RDV

[Pouvoir masquer le contexte des RDV #2233](https://github.com/betagouv/rdv-solidarites.fr/issues/2233)

Le contexte est encore présent dans le fichier Excel d'export.

[Ne plus avoir de contexte de RDV dans l'export Excel #2287](https://github.com/betagouv/rdv-solidarites.fr/issues/2287)

### Lieu ponctuel

[Utiliser un lieu ponctuel #2175](https://github.com/betagouv/rdv-solidarites.fr/issues/2175)

Il manque le nom du lieu ponctuel pour préciser l'adresse (à la saisie, à la visualisation et dans les notifications).

Faut-il ajouter des droits d'accès pour la création de lieu ponctuel ? Non, pas besoin.

### Annulation et report de RDV coté usager

Modification liée aux invitations d'usagers. Cette modification permet d'annuler ou reporter un RDV. Et ils peuvent le faire sans s'authentifier.

Quelques remarques sont remontées autour des libellés. Elles seront intégrées avant la mise en production

* [Avoir un lien avec token vers le RDV depuis la notification SMS #2288](https://github.com/betagouv/rdv-solidarites.fr/issues/2288)
* [Reporter un RDV coté professionnel #2198](https://github.com/betagouv/rdv-solidarites.fr/issues/2198)
* Nous parlons du fait que certains départements préconise plutôt l'annulation de l'ancien RDV et la création d'un nouveau. Peut-être que nous pourrions configurer le report pour qu'il puisse suivre la politique départementale à ce sujet ?

### Autres

* Le [forum](https://forum.rdv-solidarites.fr) et le [fichier de priorisation](https://docs.google.com/spreadsheets/d/1ryGnWWCx2EOoJ0a1weckx6TUwxhQD\_AYBWw6vn0R3iA/edit) ne sont plus utilisé. L'équipe va récolter les informations intéressantes sur ces deux médias, puis les supprimer.
* Le Copil du mercredi 16 mars, c'est plutôt bien passé. Prochain prévu pour septembre, avec une journée d'atelier en présentiel prévu en juin.
* D'autres recrutements vont être lancé pour renforcer l'équipe dans les semaines à venir.
* Au moment d'une mise en production d'une modification apportant une modification visible, nous allons faire une note d'informations à destination des agents qui sera envoyé aux référentes. Cela permettra à chacune de décider de faire suivre directement ce message, de ne rien faire ou de l'inclure dans une autre note d'information. Nous pourrions faciliter cette communication en proposant un moyen simple de copier la liste des emails des professionnels utilisant RDV solidarités dans le territoire.
* Irène (83) en plein déploiement se retrouve avec une demande vraiment très forte sur [Filtrer les RDV sur leur statut dans l'agenda #2271](https://github.com/betagouv/rdv-solidarites.fr/issues/2271)
* Performances (affichage de l'agenda, les éléments mettent beaucoup de temps à s'afficher dans l'agenda). L'équipe analyse actuellement les retours pour trouver où sont les problèmes majeurs et mettre en place des corrections. À venir dans la semaine si tout se passe bien.
