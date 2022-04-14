---
description: Bug, Calendrier de la roadmap, Lieu du RDV, Nouvelles référentes
---

# Réunion référentes du 18 janvier 2022

### En production jeudi 20

* Accessibilité usager (RGAA)
* [Envoi du fichier Excel par email](https://github.com/betagouv/rdv-solidarites.fr/issues/1868)
* [Créer des équipes de professionnels #1731](https://github.com/betagouv/rdv-solidarites.fr/issues/1731)
* [Indiquer le numéro de téléphone dans les résumés de notification #1978](https://github.com/betagouv/rdv-solidarites.fr/issues/1978)
* [Ajouter des traces dans l'historique de changement du RDV à propos des notifications #1970](https://github.com/betagouv/rdv-solidarites.fr/issues/1970)

Pour les modifications à propos des équipes, il reste des points à corriger avant la livraison :\
livraison :

* Il y a des doublons dans la liste des agents dans la page de création des équipes.
* Corriger la recherche de créneau pour pouvoir cherche sur une équipe ET un ou plusieurs agents.
* Ne pas afficher le champ équipe s'il n'y a pas d'équipe.

Corriger au moins les éléments de configuration pour que les référentes qui le souhaitent puissent commencer les configurations. Ce qui est visible pour les agents pourrait être désactivé si ce n'est pas corrigé avant jeudi midi.

### En cours

* RGAA
* [Clarifier le message de confirmation d'une annulation de RDV passée #1921](https://github.com/betagouv/rdv-solidarites.fr/issues/1921)
* [Prendre en compte les jours fériés #2006](https://github.com/betagouv/rdv-solidarites.fr/issues/2006)
* [Tiers lieux et visioconférence pour un RDV #1639](https://github.com/betagouv/rdv-solidarites.fr/issues/1639)
* [Supprimer les doublons de lieux dans la recherche côté usager #1955](https://github.com/betagouv/rdv-solidarites.fr/issues/1955)
* [Faciliter la recherche d'une plage d'ouverture en particulier dans la liste des plages d'ouvertures #1918](https://github.com/betagouv/rdv-solidarites.fr/issues/1918)
* [Affiche un motif que la saisie soit à la rue ou sur la ville lorsque la sectorisation porte sur la ville #2012](https://github.com/betagouv/rdv-solidarites.fr/issues/2012)

### Droits d'accès sur les motifs

Nous parlons de l'ouverture des droits d'accès sur les motifs. Cela permettra à des agents de services différents de pouvoir utiliser un même motif.

Certains libellés de motif sont aujourd'hui dupliqués d'un service à l'autre. D'autres motifs sont très spécifiques à un service donné. Il sera intéressant d'envisager des motifs non liés à un service.

Une question revient à propos de ce qui va apparaître dans les notifications. Aujourd'hui c'est le service. Demain il faudra sans doute imaginer autre chose.

Discussion à avoir le moment venu.

### Signalement de bugs :

#### Duplication de RDV

Christelle (64) nous signale un problème : le contexte n'est plus transféré dans le processus de duplication de RDV.

Ticket de bug [Dupliquer aussi le motif d'un RDV à l'autre #2020](https://github.com/betagouv/rdv-solidarites.fr/issues/2020)

#### RDV à renseigner

Sophie évoque la disparition du bandeau des rdv à renseigner dans la Drôme. Nous regardons rapidement, le bandeau est bien là en recette ainsi que sur d'autres départements.

Sophie va vérifier et revenir vers nous.

### Lieu du RDV

Dans le cadre du ticket sur les [Tiers lieux et visioconférence pour un RDV #1639](https://github.com/betagouv/rdv-solidarites.fr/issues/1639), nous nous demandons s'il ne serait pas intéressant de considérer l'emplacement dans le tunnel de prise de RDV comme étant « l'endroit où le RDV aura lieu » avec des possibilités de vérifier et de modifier.

Serait-il intéressant, dans le cadre d'un motif de RDV téléphonique, de rappeler le numéro (par défaut celui de l'usager), avec la possibilité d'en saisir un autre ?

Nous écartons ce point en se disant que nous pourrons toujours y revenir plus tard. Pas d'urgence, pas de besoin.

### Calendrier de la roadmap

Pour rappel

* RGAA
* migration HDS

1. Affinage des droits d'accès (agents, motifs, agendas, (lieu)...)
2. RDV Collectif
3. Sectorisation
4. Statistiques

Il nous a été demandé une estimation, un calendrier prévisionnel. Le besoin est surtout sur les RDV-Collectifs. Certaines personnes sont prêtes à repousser leurs RDV de groupes pour pouvoir le faire confortablement dans RDV-Solidarités. À condition que ça ne soit pas repoussé à septembre.

L'équipe va créer des tickets pour les droits d'accès et pour les RDV-Collectif, ça nous permettra sans doute d'avoir une meilleure visibilité sur les mois à venir.

Pour information, l'équipe expérimente le [regroupement de tickets dans des milestones](https://github.com/betagouv/rdv-solidarites.fr/milestones). L'idée, c'est de pouvoir y retrouver les sujets de la Roadmap, et les autres.

### Accueil de nouvelles référentes.

Aujourd'hui, nous avons accueilli les référentes de l'Aveyron. Nous avons cependant déroulé une réunion référente comme nous en avions l'habitude.

Clarisse (92) propose que nous utilisions une partie de la réunion référente de la semaine prochaine pour faire un tour de table, pour que chaque référente puisse faire un point de situation dans son département (service déployé ? Nombre d'agents ? Stratégie ? Motifs ? Ouverture en ligne ? Etc.).

Rendez-vous est pris :)
