---
description: >-
  À l'occasion du retour de Radia :tada: on fait un petit point de situation. Ce
  message est le report d'une discussion à un instant données. Ces informations
  ne sont pas des engagements, des promesses.
---

# Point de situation de l'équipe au 23 avril 2021

### Réunion référentes

* Revoir la liste des 37 référentes à qui nous envoyons les invitations. Il y a sans doute des ratés, des personnes que nous ne devrions pas contacter dans ce cadre-là, et d'autres qui ne sont pas dans la liste.
* Voir si on peut créer des alertes à partir du forum et cibler les bonnes personnes.
* Contacter les personnes des départements qui ne viennent pas, ou pas souvent, pour voir si on peut aménager les réunions sur d'autres heures ou une autre journée, pour avoir les bonnes personnes présentes, au bon moment pour elles. 

### Démo et Formation

#### Constat

Il y a eu une réunion avec l'Aveyron pour évoquer [le rôle de la personne référent](https://forum.rdv-solidarites.fr/t/le-role-de-la-personne-referente/233). Nous y avons évoqué un peu la formation.

Nous savons que certains départements ne font plus suivre les invitations au webinaire, car le format n'est peut-être plus adapté, ou ne convient plus.

Les départements ont des modes de fonctionnement spécifiques, c'est pour ça aussi que souvent les formations sont faites dans le territoire, par des personnes du territoire. Ça permet d'aborder des spécificités de fonctionnement et de paramétrage.

#### Actions

Nous allons distinguer les démonstrations des formations.

**Démonstration**

* les démonstrations faites aux territoires intéressées par le service ;
* l'accompagnement à la configuration \(démo++ à destination des agents administrateurs d'un département\)

**Formation**

* Aider les départements à organiser leur formation en interne. **Quels sont les besoins du terrain ?**
* Finaliser les petites capsules vidéos de démonstration pouvant être proposées via la documentation.

_La documentation est un outil servant aux deux aspects : démonstration et formation. Nous allons capitaliser dessus._

En résumé, il y a les **DÉMONSTRATIONS** pour faire découvrir l'outil et les **FORMATIONS** plutôt à la charge des départements, mais nous pouvons aider à leurs constructions et déroulement.

Une fois vérifié, nous pourrions, par exemple, nous assurer que la plateforme de démonstration est aussi utile pour la formation. Ou bien, prévoir une plateforme de formation.

_Peut-être que la_ [_plateforme de démonstration_](https://demo.rdv-solidarites.fr/) _sert pour la démonstration aux départements qui n'ont pas encore rejoint le consortium et peut_ servir _de plateforme de formation pour les autres. Il faudrait pouvoir remettre les données d'un territoire à zéro, récupérer la configuration depuis la production peut-être… Il y aurait sans doute des choses à faire pour faciliter._

### Produit

Les sous-titres qui suivent sont des thèmes, une sorte de ROADMAP sur laquelle nous pensons travailler ces prochains mois. Aucun de ces points n'est vraiment abouti, ce ne sont que des constatations, des hypothèses, des éléments de travail dont nous devons discuter avec la communauté, sur lesquelles nous allons aller vérifier les données, les usagers, pour trouver la meilleure façon de faire évoluer le service. Comme dit plus haut, ce ne sont en aucun cas des promesses, des engagements, ou quoi que ce soit d'autre de ce genre. Un sujet vous intéresse ? Vous voulez en parler ? Ouvrons la discussion !

#### Profil usager

**Compte**

Il y a parfois \(?\) un email pour toute une famille, voire un numéro de téléphone seulement. Nous pourrions nous orienter sur une approche, comme sur Netflix, où nous ferions une séparation entre la notion d'un compte RDV, et les profils attachés.

Ce qui serait intéressant, c'est de pouvoir ajouter les personnes à contacter, avec email et tel. Ces personnes ne sont pas des usagers directement.

Cela pourrait ressembler à la cellule familiale ? Ça serait sans doute plus souple et plus large. L'assistante familiale pourrait être là, une voisine, une personne d'une association à prévenir...

> J'ai un compte, j'y ajoute ma fille, sans contact j'y ajoute ma mère, avec info de contact j'y ajoute l'assistante familiale ça me permet de demander à notifier ces personne-là en plus de moi ça me permet de prendre rendez-vous pour ces personneslà \(sans qu'elles aient de compte\)

_Une fiche usager pourrait être associée à plusieurs comptes._

**Fiche usager**

Faire la distinction personne mineure et majeure. Pour les mineurs, nous ne demandons pas ou peu d'information \(comme aujourd'hui\). Pour les majeurs, on ouvre l'ensemble du formulaire.

Chaque majeur est une fiche usager qui pourrait être ajouté à un compte. Les doublons seront à gérer au niveau de ces fiches usagers.

Préciser le lien entre les profils.

Attention RGPD au moment de l'ajout de profil. Il faudra sans doute envoyer un message à ces personnes pour signaler qu'elles ont été ajouté en tant que contact par tel autre personne. À prendre en compte que pour l'interface usager sans doute ?

Il y aura sans doute à voir aussi sur les contraintes d'unicité \(téléphone et email aujourd'hui\). Un numéro de téléphone ou un email identifie un et un seul compte. Mais ces numéros pourraient être attribués à plusieurs personnes \(fiche usager\) en dessous. Sans doute que ces personnes seraient automatiquement associées au même compte ?

**Authentification**

Plusieurs étude nous montrent que l'accès à internet se fait de plus en plus sur mobile

* [BAROMÈTRE DU NUMÉRIQUE 2019 - Enquête sur la diffusion des technologies de l’information et de la communication dans la société française en 2019](https://www.economie.gouv.fr/files/files/directions_services/cge/barometre-numerique-2019.pdf)
* [Les Français privilégient désormais le mobile pour accéder à Internet](https://labo.societenumerique.gouv.fr/2017/07/19/les-francais-privilegient-desormais-le-mobile-pour-acceder-a-internet/)
* [Démarches administratives en ligne : progression des usages mais persistance des difficultés pour les publics défavorisés](https://labo.societenumerique.gouv.fr/2017/03/15/demarches-administratives-en-ligne-progression-des-usages-mais-persistance-des-difficultes-pour-les-publics-defavorises/)

Ou encore le questionnement sur l'authentification par mot de passe

* [Gestion des mots de passe : une conscience accrue des risques, des pratiques qui perdurent](https://labo.societenumerique.gouv.fr/2017/02/02/gestion-des-mots-de-passe-une-conscience-accrue-des-risques-des-pratiques-qui-perdurent/)

Ces éléments nous amènent à envisager de :

* permettre l'authentification par le numéro de téléphone \(ou l'email\)
* utiliser un nombre magique ou un lien magique \(authentification sans mot de passe\)

La connexion par numéro de téléphone nous a été plusieurs fois demandé. Surtout pour le traitement du RSA ou autre volant du social. C'est sans doute une approche à combiner avec le compte multiusager.

**Multi-notification**

Pour notifier plusieurs personnes pour un rendez-vous. Se baser sur le compte et les profils. Ou les profils des comptes. L'idée serait de pouvoir, à la fin du tunnel de prise de rendez-vous cocher ou décocher les personnes à notifier. Et pouvoir en ajouter.

#### Motifs

Les motifs sont aujourd'hui très nombreux. Et pourtant il n'est pas possible de configurer correctement l'application.

Il y a un travail à faire sur le paramétrage d'un motif dans le contexte d'une plage d'ouverture.

Un point basique pourrait être de permettre la création d'un motif avec libellé \(avoir la main sur les libellés\).

Attacher les motifs au territoire \(pas de duplication à faire entre les organisations\)

Arborescence de catégories \(combien de niveau ?\) de motif \(ou utilisation de tag ?\). Proposé par l'équipe ? À la main des départements ?

> se méfier des espaces de libertés -- Voir Dr Design Faire appel à l'UXWriter nouvellement arrivée.

Peut-être que nous devrions proposer un travail, avec le support des UX transverse, pour la définition de motifs nationaux. C'est un vrai défi, mais ça nous permettrait de proposer une arborescence correcte, un parcours de recherche d'un motif simplifier. À voir comment ça pourrait se combiner avec les façons de travailler de chaque département.

#### Autorisation

Basculer les agents des organisations au territoire \(et plutôt qu'à une organisation\). Un agenda par agent Autoriser l'agent à accéder à certains agendas \(voir ? Poser un rendez-vous ? CRUD\)

Métier des agents plutôt que service. Peut-être avec arborescence aussi ?

> Mon métier puéricultrice fait partie de la PMI. Qualifier les agents plutôt que les rangers dans des services.

Autoriser l'agent à accéder à certains motifs \(voir ? Poser un rendez-vous ? CRUD\)

#### Organisation et sectorisation

Affecter un secteur à un motif plutôt qu'à une organisation ? À quoi servent les organisations. L'impression qu'historiquement, c'était un découpage géographique. Aujourd'hui repris dans la notion de secteur peut-être. Et si les affectations de secteur allaient plutôt vers des motifs et ou des agents ?

#### Historique

On fait quoi des anciens rendez-vous, des anciennes plages d'ouverture, des anciennes absences, des anciens lieux ?

Aujourd'hui, c'est utile principalement pour le calcul des statistiques. Elles sont calculées à la demande, à l'affichage des pages de statistique. Si nous supprimons les rendez-vous passés, nous ne pourrons pas recalculer si nous voulons une nouvelle donnée dans les statistiques. Nous aurons cette nouvelle donnée sur les nouvelles.

Nous pourrions aussi décorréler l'historique du vivant. Je copie dans le rendez-vous le nom du lieu, mais je coupe le lien. Pareil pour l'usager, qui pourrait être anonymisé…

Il y a également le problème des parcours. Certains rendez-vous passés sont utiles pour des rendez-vous futurs. Peut-être que nous pourrions étoffer les type de motifs pour y définir des parcours, et permettre d'envisager des liens entre les motifs ou des choses de cet ordre. Ça nous permettrait de faire ce que nous essayons de faire avec les anciens rendez-vous.

Dans un premier temps, nous pourrions supprimer les plages d'ouvertures et les absences passées en tout cas. Aucune ne sert aux statistiques.

À noter que nous ne pouvons pas supprimer d'ancien lieu aujourd'hui, principalement parce qu'ils sont attachés à un ancien rendez-vous.

#### Métriques

Recueillir les feedbacks usagers, agents. Pour les agents, avoir un petit cercle représentatif que nous pourrions solliciter via la référente.

Mieux analyser le Matomo.

Quelles pages de la documentation sont lues ? Avons-nous des statistiques d'accès à la documentation ? Est-ce que nous devons déplacer les éléments de la documentation dans le forum ?



