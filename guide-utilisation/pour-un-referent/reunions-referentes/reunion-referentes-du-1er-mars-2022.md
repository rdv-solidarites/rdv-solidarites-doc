# Réunion référentes du 1er mars 2022



### Équipe

[Matis Alves](mailto:matis.alves@beta.gouv.fr) rejoint l'équipe ce jour avec une mission de chargé de déploiement. Bienvenue.

### Disponible en production

* [Nouvel interface de configuration (territoire)](https://github.com/betagouv/rdv-solidarites.fr/pull/2151)
* [Première version pour les RDV-collectifs](https://github.com/betagouv/rdv-solidarites.fr/issues/2163)
* [Prise en compte des délais de réservation](https://github.com/betagouv/rdv-solidarites.fr/issues/2005)

et diverses corrections de bug.

[Voir les tickets prévus pour la semaine à venir](https://github.com/betagouv/rdv-solidarites.fr/milestone/12)

À noter que le fichier des dernières nouveautés est utilisé. Il est donc nécessaire que nous le maintenions à jour.

### RDV-Collectif

Dans les sujets à venir il y aura la prise en compte de la capacité maximum. Nous pourrions également afficher le nombre de places prises (ex. 2/15).

[Rdv collectifs : limiter le nombre de participants #2188](https://github.com/betagouv/rdv-solidarites.fr/issues/2188)

Dans la liste des motifs, nous n'avons rien pour distinguer sur le motif et collectif ou non. Nous pourrions ajouter, un peu comme pour les motifs en ligne, un tag / badge pour visualiser les motifs collectifs.

[Visualiser le type RDV-Collectif dans la liste des motifs #2196](https://github.com/betagouv/rdv-solidarites.fr/issues/2196)

### Droits d'accès

Aujourd'hui, les équipes ne peuvent être gérées que par les administrateurs de territoire. C'est dommage que ça ne soit pas accessible pour les administrateurs d'organisation.

### Lieu ponctuel

Lorsque l'on pose un RDV ayant lieu ponctuellement à une adresse particulière, il est nécessaire de pouvoir ajouter une dénomination. Cela permettra de compléter l'adresse qui ne serait pas reconnu par la BAN, en mettant un numéro d'appartement, une salle ou tout autre information nécessaire pour le RDV.

[Utiliser un lieu ponctuel #2175](https://github.com/betagouv/rdv-solidarites.fr/issues/2175)

### RGPD - Champs sociaux et remarques

Nous voudrions masquer les champs sociaux et le champ remarque de la fiche usager. Certains départements et organisation ne souhaite pas s'en servir. Autant les faire disparaitre de l'interface.

* Remarques
* Caisse d'affiliation
* Numéro d'allocataire
* Situation familiale
* Nombre d'enfants
* Logement

L'idée serait de pouvoir masquer/afficher chaque champ, individuellement.

Nous ne proposerons pas de création de nouveau champs directement dans l'interface. S'il y a des besoins, nous pourrons en parler.

Nous suggérons également d'ajouter un champ optionnel à la liste : `numero de dossier`. En effet, le champ remarque sert souvent pour enregistrer le numéro de dossier métier (Solis ou autre application ou référence papier). Ce nouveau champ permettrait au agent de pouvoir se passer du champ adresse.

[Masquer les champs sociaux et le champ remarques de la fiche usager #2192](https://github.com/betagouv/rdv-solidarites.fr/issues/2192)

Nous évoquons à nouveau le fait de pouvoir faire un lien sortant vers l'outil métier utilisé dans le département de la fiche utilisateur... Il y a un travail d'analyse à faire pour vérifier la possibilité.

### Report de RDV et agents référent

Pour reporter un RDV, certaines personnes passe par la duplication d'un RDV. Dans le cas d'un RDV de suivi, s'il y a un référent, il n'est pas maintenu et les créneaux proposés pour la duplication sont ouvert à tous les agents proposant des créneaux sur ce motif.

Il y a deux axes d'amélioration ici.

D'une part le report de RDV. Car très fréquemment, la duplication de RDV est un outil pour faire un report de RDV. Les autres options sont l'annulation directe et la pose d'un nouveau RDV. Il y a aussi l'option de modifier la date et l'heure directement dans les RDV, mais ce n'est pas pratique, ça nécessite d'avoir une idée des disponibilités au moment de le faire.

Il y a un enjeu de garder une trace du report.

Ajout du ticket [Reporter un RDV coté professionnel #2198](https://github.com/betagouv/rdv-solidarites.fr/issues/2198)

L'autre point est lié au manque d'information dans le cadre de RDV de suivi. Le problème, c'est que les agents se retrouvent référents d'un usager sans que nous précisions pour quels motifs. Nous pouvons faire une déduction en fouillant l'historique de RDV, mais c'est impossible à imaginer tant qu'il n'y a pas eu de RDV de suivi...

[Préciser pour quel motif le professionnel est le référent de l'usager #2148](https://github.com/betagouv/rdv-solidarites.fr/issues/2148)

### Encourager et faciliter l'utilisation de la recherche de créneau

Le chemin pour trouver un RDV coté agent n'est pas si évidant que ça au premier abord. Il y a trois options :

* clic dans l'agenda
* trouver un créneau depuis l'agenda
* trouver un créneau depuis une fiche usager.

Nous pourrions aussi ajouter la duplication de RDV, mais c'est un peu particulier et rattrape-la cherche de créneau.

Nous évoquons plusieurs chemins que nous pourrions prendre pour améliorer cela. Pour le moment, tout est mis dans un ticket [Rendre plus visible et compréhensible la recherche d'un RDV #2200](https://github.com/betagouv/rdv-solidarites.fr/issues/2200). Mais nous pourrions envisager de faire la manipulation en plusieurs étapes pour ménager la conduite du changement auprès des utilisateurs.

### Cohérence sur l'utilisation des jours de la semaine

Il y a des incohérences dans l'utilisation des jours de la semaine dans RDV-Solidarités.

* Dans l'agenda, il n'y a pas les samedis et dimanches ;
* Dans la récurrence des plages d'ouverture et des indisponibilités, il y a le samedi ;
* Dans l'agenda de choix d'une date, il y a le samedi et le dimanche ;
* Dans l'affichage des créneaux disponible il y a le samedi et le dimanche ;

Les conseillers numériques ont besoin de visualiser le samedi. Une première modification rapide a été mise en place pour permettre l'affichage du samedi [Afficher le samedi dans les agendas de certains conseillers #2145](https://github.com/betagouv/rdv-solidarites.fr/issues/2145). À terme, les jours ouvrables/affichable seront sans doute à préciser dans le module de configuration.

Nous avons également évoqué le fait que l'affichage des créneaux disponible ne commence pas toujours un lundi, mais ça ne semble pas un point perturbant.

> Ce n'est pas un calendrier, ce n'est donc pas un problème.

### Atelier RGPD

[Atelier RGPD du 24 février 2022](https://doc.rdv-solidarites.fr/guide-utilisation/pour-un-referent/reunions-referentes/atelier-rgpd-du-24-fevrier-2022)

Proposition d'amélioration par rapport à ce qui a été inscrit à propos de l'affichage du label de non-connexion d'un agent : afficher quelque chose dès le 2ᵉ mois de non-connexion.

### Autres

* Il serait intéressant d'avoir des infos sur l'envoie de notification dans les statistiques
* Pouvoir filtrer la liste des RDV par motifs
* Pouvoir débrancher les notifications plage d'ouverture et indisponibilités : [Configurer les notifications de plages d'ouvertures et d'absences comme pour les RDV #1490](https://github.com/betagouv/rdv-solidarites.fr/issues/1490)
