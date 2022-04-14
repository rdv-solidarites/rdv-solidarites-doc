# Réunion référentes du 22 février 2022

### Équipe

* Thomas Guillet facilitation ;
* Yannick François développement et produit ;
* Radia Diffalah déploiement ;
* Nicolas Bouilleaud développement ;
* Victor Mours développement pour les conseillers numériques ;
* Myriam Keddad relation utilisateur ;
* Matis déploiements ;

### Les nouveautés

* [Calcul les créneaux sans min booking delay](https://github.com/betagouv/rdv-solidarites.fr/pull/2170)
* [Nouvelle interface de configuration](https://github.com/betagouv/rdv-solidarites.fr/pull/2151)
* [Supprime une duplication sur la date de naissance](https://github.com/betagouv/rdv-solidarites.fr/pull/2160)
* [Considérer les délais min et max des motifs #2005](https://github.com/betagouv/rdv-solidarites.fr/issues/2005)

### À venir

* [RGAA](https://github.com/betagouv/rdv-solidarites.fr/milestone/2)
* [Tiers lieux et visioconférence pour un RDV #1639](https://github.com/betagouv/rdv-solidarites.fr/issues/1639)
* [Améliorer la performance des envois de webhooks #2154](https://github.com/betagouv/rdv-solidarites.fr/issues/2154)
* [RDV Collectifs v0 #2163](https://github.com/betagouv/rdv-solidarites.fr/issues/2163)
* [Faciliter la recherche d'une plage d'ouverture en particulier dans la liste des plages d'ouvertures #1918](https://github.com/betagouv/rdv-solidarites.fr/issues/1918)
* [Invitation et accès organisation depuis le module de configuration #2032](https://github.com/betagouv/rdv-solidarites.fr/issues/2032)

### RDV Collectif

Nous avons commencé les développements pour les RDV-Collectifs. Très demandé dans le cadre des conseillers numériques, c'est aussi une demande très forte du médico-social.

Voici un ticket qui documente le premier pas que nous vous proposons : [RDV Collectifs v0 #2163](https://github.com/betagouv/rdv-solidarites.fr/issues/2163)

Lors de la présentation, il y a eu plusieurs questions et pistes pour la suite.

> Pourquoi ce n'est pas une plage d'ouverture ?

Effectivement, dans cette première version, nous sommes partis sur le fait de poser un RDV directement. Après avoir créée un motif pour des rendez-vous collectif, il est donc possible de poser un RDV pour ce moment. Cela permet de ne pas avoir à saisir d'usager tout de suite, au moment de la création (c'est possible, mais pas obligatoire), et de faire des notifications individuelles, y compris au moment de l'ajoute d'un usager.

Il manque actuellement la possibilité de renseigner une capacité maximum.

Une demande très forte aussi pour pouvoir « trouver la prochaine place disponible pour un atelier collectif ». Nous avons discuté de pouvoir le faire par le même chemin qu'aujourd'hui (recherche de créneau) ou de le faire via une nouvelle entrée de menu, spécifique aux RDV collectifs.

Il a été évoqué les difficultés de changer les habitudes. C'est aussi ce qui a été dit à propos du flux habituel : je crée un motif, je crée une plage d'ouverture, je pose un RDV. Alors que pour les RDV-Collectifs, tel que proposé dans cette première version, nous avons : je crée un motif, je pose un RDV.

Nous apprenons que les Pyrénées-Atlantique utilise une organisation spécifique pour faire des ateliers collectifs et ouvre des plages d'ouverture de la longueur de l'atelier, avec un motif d'une durée équivalente à la longueur de l'atelier / la capacité de l'atelier. Cela permet d'avoir plein de créneau de 5 minutes par exemple, mais sur des horaires décalés...

L'information sur la durée de l'atelier pourrait être intéressante à ajouter aux notifications. Un contournement est possible en utilisant le titre du motif.

Faut-il ajouter le nombre minimum de participants ? Cela permettrait d'avoir une annulation automatique (avec notification) ou simplement une alerte ?

### Tiers lieux et visioconférence pour un RDV

Le ticket [Tiers lieux et visioconférence pour un RDV #1639 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1639)contient en fait deux actions à mener. Nous allons découper pour avoir un ticket concernant le fait de pouvoir saisir un lieu éphémère dans le tunnel de RDV, et un autre pour traiter du nouveau type de RDV : la visioconférence.

#### Lieu éphémère

Le premier est celui que nous allons finaliser dans les jours à venir : [Utiliser un lieu éphémère #2175](https://github.com/betagouv/rdv-solidarites.fr/issues/2175).

L'idée, comme indiqué dans le ticket, c'est de pouvoir saisir un lieu dans le tunnel de prise de RDV.

#### Motif de RDV visioconférence

[Faire des RDV en visioconférence #2176](https://github.com/betagouv/rdv-solidarites.fr/issues/2176)

La meilleure façon de faire est d'ajouter un type de RDV, au niveau de la configuration de motif. Nous aurions donc « sur place », « à domicile », « au téléphone » et « en visioconférence ».

#### Discussion sur le type de RDV

Dans la discussion sur l'ajout d'un type visioconférence, nous avons abordé la problématique des doublons de motifs. Un motif est créé en double (et bientôt en triple ?) pour en avoir un par type de RDV. Cela permet de préciser des plages d'ouvertures mixtes (avec les deux types) et surtout d'avoir des plages d'ouverture (voir des agents) qui ne font que du sur place ou que du téléphonique.

C'est au moment de la construction de créneau que ce choix intervient.

Et si nous déplacions le choix du type de RDV sur les plages d'ouverture ?

[Limiter les duplications de motif, déplacer le type de RDV dans la plage d'ouverture #2177](https://github.com/betagouv/rdv-solidarites.fr/issues/2177)

Attention à ne pas trop alourdir la création de plage d'ouverture.

#### Recherche de créneau en précisant le type de RDV

Nous avons également parlé d'ajouter un filtre pour trouver des créneaux sur place. Pour le moment, coté agent, la recherche de créneau se base sur le motif. Le motif est porteur du type de RDV. Il n'est donc pas possible de chercher des créneaux sur place ET au téléphone.

Par contre, il est laborieux de retrouver le bon motif (sur place ou au téléphone). Ajouter un filtre, comme pour le service, pour limiter le choix des motifs serait très intéressant.

[Filtrer les motifs sur le type de RDV dans la recherche de créneaux coté agent #2178](https://github.com/betagouv/rdv-solidarites.fr/issues/2178)

### Utilisation de terminaux mobile

RDV-Solidarités n'a pas été tout de suite pensé pour fonctionner sur un téléphone. C'est faisable, mais vraiment pas optimal. Pourtant, nous avons à ce jour, [plus de 20 % des connexions à RDV-Solidarités qui se font sur mobile](https://stats.data.gouv.fr/index.php?module=CoreHome\&action=index\&idSite=123\&period=range\&date=previous30#?idSite=123\&period=range\&date=previous30\&category=General\_Visitors\&subcategory=DevicesDetection\_Devices).

Un point de blocage actuellement, le clique dans l'agenda depuis un mobile n'ouvre pas le tunnel de prise de RDV. Est-ce un bug ?

La recherche de créneau fonctionne, mais certaines équipes sur le terrain, équipé d'un téléphone, n'utilise pas de plage d'ouverture pour la gestion de leur RDV à domicile.

Nous pouvons [Ajouter un bouton « Créer un RDV » dans l'interface agent #2179](https://github.com/betagouv/rdv-solidarites.fr/issues/2179). C'est la solution la plus simple, et qui semble convenir.

### Procédure de mise en production

L'équipe à deux protocoles de mise en production des modifications apportées au service.

* **Directement** une fois le travail terminé, vérifier en interne. Cela concerne les corrections de bugs, les évolutions techniques, certaines modifications n'ayant aucun impact sur le processus de prise de RDV ou autres pour les agents.
* **Après présentation aux référentes** (le mardi matin). Cela concerne les fonctionnalités qui apportent un changement sur l'utilisation du service.

Irène attire notre attention sur le problème que pose les livraisons fréquentes : la mise à jour des tutoriels et de la documentation réalisée par les référentes dans les départements.

Nous allons faire en sorte de prendre une plus grande par dans la rédaction de documentation, au moins sur l'usage de RDV-Solidarités. Le curseur à placer entre les protocoles de fonctionnement lié au fonctionnement d'un département est l'usage générique de RDV-Solidarités reste à trouver.

Pour rappel, il existe un site qui répertorie des [Guides et ressources de RDV-Solidarités](https://doc.rdv-solidarites.fr).

### Équipes et organisations

Une demande de Christelle : pouvoir [Lier les équipes aux organisations #2174](https://github.com/betagouv/rdv-solidarites.fr/issues/2174)

### Atelier RGPD

Pour rappel, il y a un atelier RGPD ce jeudi 24 de 10 h à 12 h. Nous espérons traiter l'ensemble des points ce jeudi matin. Si ce n'est pas le cas, nous pourrons utiliser le créneau du lundi 7 mars au matin.

Pour rappel, cet atelier fait suite à une demande de la Somme. L'idée est de définir et prioriser les modifications dans le service RDV-Solidarités pour les points suivants :\
suivants :

* La durée de conservation des données indiquée sur le site, mais avec des infos incohérentes et non appliquée réellement (sauf erreur de ma part)
* la référence à "privacy".. qqchose sur le site
* les exports de documents nominatifs
* les zones de commentaires
* le contenu des SMS et mail
* les mails des usagers reçus par les développeurs

Ces tickets seront ensuite présentés sous forme d'un compte rendu d'atelier à une réunion référente ultérieur. Ainsi, si vous ne pouvez pas être disponible aux dates proposées, nous pourront malgré tout discuter de vos attentes sur ces points-là.
