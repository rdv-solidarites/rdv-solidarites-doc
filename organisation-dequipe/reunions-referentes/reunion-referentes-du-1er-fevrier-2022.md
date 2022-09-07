# Réunion référentes du 1er février 2022

### En production

#### Bugs corrigés

* Copier le contexte à la duplication d'un RDV
  * https://github.com/betagouv/rdv-solidarites.fr/issues/2020
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2043
* Eviter d’ajouter les usagers en doublon quand on modifie un RDV
  * https://github.com/betagouv/rdv-solidarites.fr/issues/2028
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2038
* Permettre les ré-invitations d’agents
  * https://github.com/betagouv/rdv-solidarites.fr/issues/2019
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2045
* Bien prendre en compte le dernier jour d’indisponibilité par dessus une plage d’ouverture
  * https://github.com/betagouv/rdv-solidarites.fr/issues/2055
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2056
* Ne pas mentionner l’envoi de notifications lorsqu’un rdv passé est annulé (et qu’aucune notif n’est envoyée)
  * https://github.com/betagouv/rdv-solidarites.fr/issues/1921
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2030
* Annule un RDV passé sans message de confirmation
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2040
* Corrige l’affichage du label des notifications de rappel
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2039
* Ne pas afficher les agents en doublon dans la liste d’agents du territoire
  * https://github.com/betagouv/rdv-solidarites.fr/issues/2025
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2044
* Respecter le tri de la recherche texte dans les résultats
  * https://github.com/betagouv/rdv-solidarites.fr/issues/2047
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2051
* Corriger une erreur à l’affichage du créneau suivant
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2103
* Ne pas afficher les membres des équipes recherchées dans le champ agents
  * https://github.com/betagouv/rdv-solidarites.fr/issues/2026
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2052
* Affiche le lieu qui avait été sélectionné quand on revient au filtre de la recherche de créneaux agent
  * https://github.com/betagouv/rdv-solidarites.fr/issues/2054
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2052

#### Outillage/Interne

* Ajuste les modèles d’issue et de PR
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2041
* Set search terms in seed data for Users and Agents
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2049
* Remove useless scopes
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2053
* Ébauche de style de code dans la doc
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2058

#### Data-insertion

* feat(invitations): Precise location type when a motif is selected
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2035
* refactor(invitations): Link invitation matching motifs to
  * https://github.com/betagouv/rdv-solidarites.fr/pull/2046

### En cours

*   Affiche le premier prochain créneau

    https://github.com/betagouv/rdv-solidarites.fr/pull/2106
* nouvelle interface de configuration
* performance sur l’affichage des usagers
* tiers-lieux / adresse de visio

### Pour discussion

Tour de table des usages et du déploiement sites

#### Élodie Vaneecke (62)

* 25 site du département ;
* 3 services (secrétariat, social, PMI) ;
* 53 % de déploiement ;
* Stratégie d'ouverture en ligne ;
* Secrétariat pour rdv tel en préqualif ;
* Une seule référente ;
* Démarrage dans le Pas-de-Calais en juillet 2019 ;
* 50 agents par site

#### Fabienne Guerle (80)

* 5 territoires ;
* 22 MDSI
* Une personne référente par territoire (un territoire est une organisation) ;
* Début en janvier 2020 ;
* Autonomie, social et enfance formés ;
* Social et autonomie bien déployés, enfance moins pour le moment ;
* PMI, CPEF et MDPH ouverts en ligne.

#### Sophie Naslot (26)

* Avril 2019 co-construction ;
* 4 territoires ;
* 1 territoire (8 CMS) totalement déployé coté agent (PMI, Social, Psy, infirmière, un peu ASE sur quelque motifs) ;
* 1 CMS == 1 organisation ;
* 25 CMS au total ;
* Reste 17 à déployer
* Fin 2022 avoir déployé dans tout les CMS ;
* Objectif : laisser le temps aux équipes de prendre en main l'outil ;
* Janvier 2023 pour l'ouverture en ligne (attente que les équipes soient à l'aise, et que le déploiement soit sur tout le territoire) ;
* 2 coordinatrices de territoire à terme ;
* 2 référentes de site dans chaque CMS ;
* Pour la formation, présentation, guide utilisateur ;
* Réunion trimestrielle pour faire le point avec les référentes.

#### Clarisse Beauvois (92)

* Sur l'année 2021 (fin mai -> fin décembre), déploiement des 13 territoires (pmi, social, cpef, protection de l'enfance) du 92 ;
* Déploiement RDV-Soldiarités associé au déploiement d'un CRM (connecté avec RDV-S et les autres logiciels métiers) ;
* 900 utilisateurs ;
* 6 accompagnatrices aux usages numériques pour accompagner les professionnelles sur le terrain ;
* Référente du 92 est responsable d'application ;
* Phase d'accompagnement encore en cours ;
* Préparer les acteurs de terrain avant l'ouverture en ligne ;
* 2022 objectifs MDPH et mineur non accompagné

#### Marie Phillips (12)

_(avec Anne Raquet)_

* Déploiement en janvier 2021 PMI et social ;
* Ouvert à la prise de RDV en ligne dès le début ;
* 4 territoires ;
* 6 MSD ;
* Utilisation de Data-Insertion sur le RSA ;
* Ouverture aux partenaires sociaux (5 organisations supplémentaires) ;
* Élargir sur les thématiques sociales ;
* 180 agents utilisateurs de RDV ;
* Pas vraiment de référentes attitrée, expérimentation sur 3 mois pour voir le travail nécessaire et envisager la suite.

#### Vaéa Castaing (77)

_(Avec Amandine Perriot)_

* Depuis 2019, 2020 déploiements sur 14 territoires ;
* 1 500 agents ;
* 3 services PMI-CPEF, Social, SAPHA (Seniors ainés, personnes handicapées et aidants) ;
* Échec sur l'ASE pour le moment. ASSFAM présente ;
* 2 MDS qui sont un peu en difficulté ;
* Pas encore beaucoup de prise de RDV en ligne.

#### Élise Forget (14)

* Priorité PMI et CPEF ;
* 11 PMI et 1 CPEF et également 1 MDPH ;
* Reste 3 PMI à déployer ;
* Certaines circonscription ont demandé à déployer sur d'autres secteurs : un peu de RSA, Engagement réciproque, RIP (recueil d'information prioritaire lié à l'ASE) ;
* Opposition assez forte sur l'ouverture en ligne pour l'instant ;
* Tentative sur certains motifs sans enjeux ;
* Peur de la perte de contrôle sur l'agenda ;
* Élise, seul référente sur le projet : personne dans le département n'a de disponibilité pour prendre la charge de travail de référente ou coordinatrice pour aider ;
* Début de déploiement été 2020.

#### Magalie Le Helloco (22)

* 5 territoires avec une MDD sur chaque ;
* Début de déploiement été 2020 sur la PMI de Saint-Brieuc ;
* La MDD de Saint-Brieuc est sur 3 sites ;
* Dans le 22, 1 site == 1 organisation ;
* Fin 2020, la MDD de Saitn-Brieuc était entièrement déployée ;
* 2021 débuts des actions sociales de Saint-Brieuc sur un site ;
* Objectif 2022 déployer les sites d'actions sociales ;
* Grande frilosité à l'ouverture en ligne : peur de perdre la main sur l'agenda ;
* Reste les autres MDD, Dinan sont lancé, mais ça stagne ;
* Pas de portage sur les autres MDD, mais il n'y en a pas.

#### Christelle Cufay (64)

* Démarrage 2019 ;
* Chargé du déploiement sur tout le déploiement ;
* 7 SDSEI, avec plusieurs sites par SDSEI ;
* 23 organisations sociales et 7 PMI + 2 organisations extérieures pour des partenaires extérieurs ;
* Déploiement à 100 %, mais pas sur tous les métiers ;
* Reste référent ASE (lié à un manque de certaines évolutions) ;
* Inviter l'ASSFAM en tant qu'agent (pourquoi ça coince ?) ;
* Pas de règle sur l'ensemble du département, chacun a choisi comment déployer dans leur organisation ;
* Obligation d'ouvrir en ligne pour avril 2022 ;
* Peur de perdre la main sur son agenda, les usagers vont prendre RDV pour tout et n'importe quoi ;
* Sur les motifs ouverts en ligne (un peu test), 50 % des RDV sur ces motifs sont pris en ligne ;
* Data-Insertion aussi sur l'aspect RSA ;
* Blocage de l'ouverture de certains motifs lié à la sectorisation

### Notes de réunion

#### Recherche de créneaux coté agent

Afficher un message lorsqu'il n'y a pas de créneau pour les critères de recherches pour être explicite (UX) : [Préciser qu'il n'y a pas de créneau pour ces critères coté agent #2119](https://github.com/betagouv/rdv-solidarites.fr/issues/2119)

#### Droit d'accès

Le fichier qui a été partagé la dernière fois est un exemple. Vous pouvez supprimer les profils proposés pour en proposer d'autres.

De la même manière, si certains droits manque d'après vous, n'hésitez pas à les ajouter.

#### Territoire

Nous avons utilisé le terme territoire plutôt que département dans RDV-Solidarités pour faciliter l'utilisation de l'outil par d'autres types d'utilisateurs, sur des granularités différentes.

Le problème, c'est que ce terme signifie quelque chose pour les référentes, souvent, une organisation est à un ou plusieurs territoires...

Nous envisageons de changer ce nom. Encore faut-il trouver lequel utiliser.
