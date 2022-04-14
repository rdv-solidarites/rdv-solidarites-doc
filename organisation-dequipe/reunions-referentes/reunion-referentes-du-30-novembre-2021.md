---
description: >-
  Démo, RGAA, Copil, RDV à Renseigner, SMS, Design, Tooltip agenda, RDV
  Collectif
---

# Réunion référentes du 30 novembre 2021

### Démo

* [Libérer le libellé de motifs #1780](https://github.com/betagouv/rdv-solidarites.fr/issues/1780)
* [ Correctement afficher les erreurs à l‘étape 2 du AdminRdvWizard #1880](https://github.com/betagouv/rdv-solidarites.fr/issues/1880)

### Référentiel Général d'Amélioration de l'Accessibilité

Nous avons été sollicités par une personne du service design des services numériques de la Direction interministérielle du numérique vis-à-vis de notre avancé de mise en conformité avec le [RGAA](https://www.numerique.gouv.fr/publications/rgaa-accessibilite/). Cela fait suite à une rencontre avec des maires (le salon des maires ?).

Nous avions enclenché les travaux. Nous allons continuer. Nous nous sommes inscrit pour un audit début 2022, et des travaux de préparation sont à faire en décembre.

### Problème compteur de RDV à renseigner

Depuis la livraison du bandeau certains départements nous ont remontés quelques problèmes. Nous en avons listé 3 cas de figure :

* Agents multiorga : On affiche un RDV à renseigner, mais il ne s'affiche pas dans la liste des RDV de l'orga courante. Parce que c'est un RDV à renseigner sur une autre orga
* ajouter et retirer des agents d'un RDV : nous ne recalculons pas le nombre de RDV à renseigner dans ce cas
* création et suppression de RDV : nous ne recalculons pas le nombre de RDV à renseigner dans ce cas.

Un correctif est en route pour la production pour corriger le dernier cas (qui doit être le plus courant).

### Point sur la mise en œuvre du fournisseur d'envoi de SMS par département.

Dans la convention en cours, il est demandé aux départements de prendre à leur charge l'envoie de SMS. Il faut donc trouver un fournisseuret synchroniser avec l'équipe pour qu'elle développe un connecteur si nécessaire. Pour rappel

* Utilisant leur propre fournisseur
  * Hauts-de-Seine
  * Pas-de-Calais
  * Seine-et-Marne
* En cours de test ou réalisation de connecteur
  * Somme
  * Pyrénées-Atlantique
* À mettre en route
  * Meuse
  * Drôme
  * Calvados
  * Côtes d'Armor
  * Aveyron

À voir aussi pour les départements via RDV-Insertion.

### Notes diverses

* Existe-t-il un compte rendu du COPIL ? Si oui, où ?
* Afficher les agents (initiale ?) dans la tooltip agenda. Demande ajoutée au ticket existant [Revoir les informations des infobulles de l'agenda #1821](https://github.com/betagouv/rdv-solidarites.fr/issues/1821)
* Design & RDV-Solidarités : l'équipe amorce, part petites touches, une évolution du design de l'interface coté agent autant que coté usager
* RDV Collectif le dernier atelier a eu lieu, il reste à mettre au propre les notes. Objectif : faire une présentation à la prochaine réunion référente.
