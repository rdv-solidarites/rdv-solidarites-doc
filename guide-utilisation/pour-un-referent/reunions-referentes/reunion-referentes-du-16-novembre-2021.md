---
description: >-
  Démo, accessibilité, Atelier RDV Collectif, Messages usagers, Dupliquer de
  motif, Agenda multiagent
---

# Réunion référentes du 16 novembre 2021

### Démo

* [Faciliter l'accès aux RDV à renseigner #1788](https://github.com/betagouv/rdv-solidarites.fr/issues/1788)
* [Changer de statut sur la fiche RDV depuis un smartphone #1823](https://github.com/betagouv/rdv-solidarites.fr/issues/1823)
* Correction recherche agent : la recherche se lance maintenant dès la première lettre saisie

Il y a sans doute un bug sur la page de liste des RDV : le nom de l'agent n'apparait pas dans le filtre (et pourtant, nous ne voyons que les RDV de l'agent sélectionné) : https://github.com/betagouv/rdv-solidarites.fr/issues/1872

### Accessibilité

Travaux amorcés par Rebecca. Le RGAA concerne les usagers comme les agents.

L'information sur le niveau d'accessibilité coté agent ne pointe pas vers la page exposant les informations légales.

https://github.com/betagouv/rdv-solidarites.fr/issues/1873

### Atelier RDV Collectif

Atelier RDV Collectif ce jeudi 18 de 9 h 30 à 11 h. Comme la conformation arrive un peu tard, il est possible que toutes les personnes ne puissent pas venir. Nous relancerons dans ce cas un Framadate pour un nouveau rendez-vous.

### Traitement des messages usager reçu par l'équipe

Nous évoquons à nouveau les messages que l'équipe reçoit sur l'adresse contact@rdv-solidarites.fr. En ce moment, c'est de l'ordre de 5 à 6 par jour (tout département confondu). Le traitement de ces messages n'est pas forcément très chronophage. C'est l'aspect respect du RGPD qui est problématique ici.

Nous avons parlé de l'option de faire en sorte que les réponses usagers aux notifications lié à un RDV soient envoyé à une boite générique par département ou par organisation. Ça ne semble pas si simple.

La solution la plus directe et la plus souple, c'est de faire en sorte que la réponse arrive directement dans les emails des agents liés au RDV.

Nous utiliserions une adresse générique, lié au RDV pour masquer l'adresse des agents.

https://github.com/betagouv/rdv-solidarites.fr/issues/1876

### Pouvoir dupliquer les motifs d'une organisation

Dans le tableau de priorisation des discussions, nous sommes arrivés à évoquer le sujet [pouvoir dupliquer les motifs d'une organisation dans une nouvelle organisation](https://forum.rdv-solidarites.fr/t/pouvoir-dupliquer-les-motifs-dune-organisation-dans-une-nouvelle-organisation/78).

Ce sujet est en fait traité par le ticket [simplifier la configuration et affiner les droits d'accès des motifs #1779](https://github.com/betagouv/rdv-solidarites.fr/issues/1779)

### Agenda multiagent

La discussion suivante fait suite à plusieurs messages sur le forum

* [Agenda multi-agents par jour voire par semaine](https://forum.rdv-solidarites.fr/t/agenda-multi-agents-par-jour-voire-par-semaine/92/5)
* [Un seul écran l’agenda de tous les professionnels présents un même jour dans la structure](https://forum.rdv-solidarites.fr/t/un-seul-ecran-l-agenda-de-tous-les-professionnels-presents-un-meme-jour-dans-l-structure/139)

Les usages liés à ces demandes sont

* la recherche de créneaux communs
* Savoir tel jour quelle permanence j'ai et qui la fait (64, ...)
* Les agents d'accueil impriment la liste des RDV avec l'export pour faciliter l'aiguillage (22, ...)

Est-ce que ça fait partie de la finalité de RDV Solidarités ? Pas sûr. C'est peut-être un élément lié au suivi usager. Faut-il passer beaucoup de temps sur ce sujet ? Peut-être pas.

Aujourd'hui, la liste des RDV (qui permet de faire des filtres sur le fichier exporté également) permet de répondre à la plupart des usages.

Peut-être pourrions-nous ajouter un filtre par service, un filtre pour les motifs.
