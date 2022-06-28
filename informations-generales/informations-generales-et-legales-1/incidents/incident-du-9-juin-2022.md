---
description: Post mortem réalisé le 28 juin 2022
---

# Incident du 9 juin 2022

### Chronologie

Cette modification intervient dans le cadre plus large d'une modification sur la logique de droit d'accès pour permettre à des agents de prendre des rendez-vous « inter-services ».

* Sujet discuté et analysé depuis plus d'un an
* PR ouverte en mars 2022
* 2 ou 3 réunions référentes où la fonctionnalité a été présenté
* mercredi 8 juin dans la soirée, mise en production de la PR à propos des déplacements de gestion des agents (invitation agent et affectation, organisation)
* jeudi 9, plusieurs retours d'agents à propos de la « perte » des écrans de gestions des agents et invitations
* vendredi 10 découvertes d'un bug affectant les agents multi-territoire (concerne uniquement l'équipe RDV-S et l'équipe Data.insertion pour le moment) qui supprime les droits d'accès sur les autres territoires lorsque l'on invite un agent sur un territoire donné
* du 13 au 17 absence de Yannick qui avait fait la PR et la mise en prod
* le 13, 14, 15 juin : questions de la part des CNFS sur leur mattermost pour savoir comment inviter des nouveaux agents + remontée sur Zammad
* le 16 juin : réunion de l'équipe pour décider de ce qu'on fait pour sortir de l'urgence : on décide de remettre en place l'ancien menu
* retour à la normale avec le retour de l'ancien menu

Conscience qu'il n'y avait pas dans cette PR de

* visualisation des invitations en attente
* de suppression d'agent

### Problèmes

* perte d'intuitivité, rallongement du parcours

> c'étais mieux avant

* Surcharge de travail pour l'équipe support (beaucoup de message, quoi répondre ?)
* Pas d'information liée à cette modification
* Délai entre la démo et la mise en prod. Difficile pour les référentes de faire le lien
* Pas d'annonce claire et précise sur le fait que certaines choses seront implémenter plus tard (visualisation des invitations en attentes, suppression d'agent)
* Les anciennes invitations peuvent peut-être créer des cas de problème https://github.com/betagouv/rdv-solidarites.fr/issues/2611 ? À vérifier.

### Actions possibles

* Accompagner le changement d'ergonomie : maintenir un menu, une page, avec une explication d'où partent les choses lorsqu'on les déplace (voir ce qui a été fait pour le téléchargement de fichier statistique, il reste d'ailleurs le texte dans la page des statistiques d'organisation)
* Mettre en place une validation par l'équipe support/produit (Nesserine, Myriam, voir Matis). À la demande de la personne qui a fait la modification. Peut aussi être visualisé dans une nouvelle colonne.
