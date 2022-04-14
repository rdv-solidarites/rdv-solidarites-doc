# Réunion référentes du 15 mars 2022

### En démo

#### [Masque l'adresse dans le cadre d'un RDV à domicile #2265](https://github.com/betagouv/rdv-solidarites.fr/pull/2265)

Mis en production après avoir repris le message à propos des RDV à domicile dans la notification email

#### [Ajoute le numéro dossier et un complement adresse en option #2264](https://github.com/betagouv/rdv-solidarites.fr/pull/2264)

Tous les champs sont envoyés vers les systèmes connectés. S'ils ne sont pas activés, la valeur sera vide. La documentation a été mise à jour pour faire apparaître les nouveaux champs. Voir la page [format des données](broken-reference)

Mis en production avec des modifications de la documentation.

#### [Paramètre l'affichage du motif dans la notif mail #2259](https://github.com/betagouv/rdv-solidarites.fr/pull/2259)

**À ne pas déployer**

Suite à la démonstration, beaucoup de questions et échanges autour de ce point.

**Le problème : comment les usagers s'y retrouve dans leur sdifférents RDV ? Comment orienter les usagers vers les bonnes personnes lorsqu'il arrive sur place ?**

Les idées explorer qui coincent

* Afficher le nom de l'agent dans la notif ?
* Ajouter et afficher un métier ?
* Une catégorie de motif ?
* Avoir un lien vers plus de détail sur le RDV ?

Aucune de ces options semble convenir.

La meilleure piste semble être de pouvoir paramétrer dans le motif ce qui apparaitra dans la notification, en proposant plusieurs choix :

* le nom de l'agent
* le titre du motif
* le titre alternatif du motif (_un titre_ public _à ajouter_)
* le service
* la catégorie (voir ci-dessous)

### Catégorie de motif

La discussion sur ce qui apparait dans la notification nous amène à discuter de catégorie de motifs. Mais il y a deux grands courant à réconcilier pour trouver la bonne option :

* Les motifs très **détaillés** qui creuse un grand écart avec le service. Ces structures souhaitent créer des catégories intermédiaires pour regrouper les motifs
* les motifs très **génériques** qui sont très proche des services, mais peu explicite. Ces structures souhaitent pouvoir préciser un peu plus le motif, sans doute au moment du RDV.

À voir. Les RDV collectifs vont explorer le fait de préciser un motif. C'est peut-être le mieux, si on considère que le motif et une sorte de « configuration » de motif, un template en quelque sorte.

### Bugs corrigés

#### Erreur de chargement de l'agenda

Parfois certains agents avaient des messages d'erreurs sur le chargement des données de leur agenda. C'était lié à des RDV qui était mis à une durée nulle. Nous avons ajouté un contrôle pour empêcher la création de RDV à zéro (voir [déplacer les contrôles de créneau (TimeSlot) au moment de l'écriture du RDV, pas de son affichage #2105 ](https://github.com/betagouv/rdv-solidarites.fr/issues/2105)pour plus de détail).

Nous apprenons lors de la réunion que certains agents mettent les RDV à une durée de 0 pour ne plus les voir dans l'agenda... Les rendez-vous annulés perturbe la lecture de l'agenda.

[Filtrer les RDV sur leur statut dans l'agenda #2271](https://github.com/betagouv/rdv-solidarites.fr/issues/2271)

Nous parlons aussi de la difficulté de lecture dans l'agenda en cas de rendez-vous court (moins de 30 minutes). Il n'y a pas d'option de zoom, mais l'outil que nous utilisons pour l'affichage de l'agenda permet une vue liste. Nous pourrions, dans un premier temps, faire un essai avec ce mode d'affichage.

[Ajouter la vue liste dans l'agenda #2272](https://github.com/betagouv/rdv-solidarites.fr/issues/2272)

#### Changement de RDV par un usager

Des usagers ont réussi à modifier l'heure et l'agent avec qui ils avaient RDV pour des motifs qui ne sont pas ouvert en ligne. C'est en fait le mécanisme de file d'attente qui s'est déclenché. Nous avons ajouté une condition pour le déclenchement : le motif doit être réservable en ligne pour que la file d'attente fonctionne (voir [Empeche acces file attente pour motif non reservable en ligne #2253 ](https://github.com/betagouv/rdv-solidarites.fr/pull/2253)pour plus de détail).

Il reste une question : pourquoi la file d'attente était activée ? Normalement, c'est l'usager qui demande, via l'interface usager, à « activer » la file d'attente.

### [RDV Collectifs : Limiter le nombre de participants #2215](https://github.com/betagouv/rdv-solidarites.fr/pull/2215)

Pour clarifier la création de RDV collectif, une nouvelle entrée dans le menu, au même titre d'une indisponibilité et une plage d'ouverture. Est-ce qu'un RDV collectif doit pouvoir se créer comme une plage d'ouverture ? Faut-il faire bouger le concept de plage d'ouverture ?

Ce nouveau menu permet de gérer les inscriptions aux ateliers. Ceci étant, il serait bien de pouvoir le faire depuis la recherche de créneau pour limiter les chemins possible. Si le motif recherché est un type RDV Collectif, alors la page de résultat pourrait prendre la forme de la liste prévue dans le nouveau menu.

### Dernières nouveautés

Nettoyage et récupération des pages des [dernières nouveautés](https://doc.rdv-solidarites.fr/informations-generales/dernieres-nouveautes). Les modifications de 2020 et 2021 ont été placé dans leur page respective

### Motifs : désactivation

Au même titre que les lieux, certains motifs ne sont plus utilisés / utilisable. Il serait, comme pour les lieux, intéressant de pouvoir les supprimer, mais il faut traiter le problème du lien au RDV avant.

En attendant, nous pourrions proposer une désactivation, comme pour les lieux. Le motif reste visible dans la liste d'administration, et dans les RDV l'ayant utilisé avant désactivation, mais il ne pourrait plus être sélectionné dans la recherche ou dans la création d'un RDV.

[Désactiver un motif #2274](https://github.com/betagouv/rdv-solidarites.fr/issues/2274)
