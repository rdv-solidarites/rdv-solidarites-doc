# Réunion référentes du 4 janvier 2022

### Démo

* Nouveau calculateur de créneau (le retour) ;
* Mise à jour technique (framework ruby on rails) ;
* Plus de transformation automatique des noms de famille (agent comme usager). Il reste des affichages qui mettent en majuscule l'ensemble du nom ;
* Système de notification personnalisable au niveau du RDV

À propos du système de notification personnalisable, il est souhaité d'ajouter des traces sur les choix à la création (et par qui), et sur les modifications. Voir le ticket https://github.com/betagouv/rdv-solidarites.fr/issues/1970

Ces points seront livrés en production jeudi sauf problème majeur entre temps.

### En cours

_Nous n'avons pas eu l'occasion d'en parler durant la réunion, mais voici ce qui est prévu dans les jours qui viennent en recette_

* [Éviter les timeout à l’export des Rdv #1868](https://github.com/betagouv/rdv-solidarites.fr/issues/1868)
* [Créer des équipes de professionnels #1731](https://github.com/betagouv/rdv-solidarites.fr/issues/1731)
* Une première vague de modification (relativement invisible) pour améliorer l'accessibilité
* [Tiers lieux et visioconférence pour un RDV #1639](https://github.com/betagouv/rdv-solidarites.fr/issues/1639)
* [Supprimer les doublons de lieux dans la recherche côté usager #1955](https://github.com/betagouv/rdv-solidarites.fr/issues/1955)
* [Clarifier le message de confirmation d'une annulation de RDV passée #1921](https://github.com/betagouv/rdv-solidarites.fr/issues/1921)

### Sécurisation des mises en production

Il y a eu plusieurs problèmes suite aux mises en production à l'automne. Le dernier en date du [17 décembre 2021](broken-reference) est principalement lié à un manque de test en recette.

L'augmentation du nombre d'utilisateurs du service nécessite une amélioration de la qualité du processus de mise en production.

L'équipe met en place et maintient plusieurs éléments techniques de vérification de non-régression, de performances, de sécurité, et bientôt d'accessibilité, mais il reste une étape de test manuel qui est délicate à réaliser par l'équipe technique : des tests de recette.

L'idée serait donc d'ajouter une étape à la recette pour concevoir des tests métiers plus ou moins poussé selon la criticité de la fonctionnalité.

Pour faire ce travail, il faudrait avoir une personne dédiée dans l'équipe ou bien, une possibilité que nous avons évoquée, faire appel aux personnes référentes. Sur la base du volontariat (et peut-être de l'intérêt sur la fonctionnalité ?), nous pourrions solliciter de l'aide pour vérifier que tout va bien avant de mettre en production.

Clarisse a évoqué la création d'un cahier de recette. Ces cahiers permettraient à chaque référente de pouvoir dérouler des jeux de tests large, prenant en considération des contextes variée, et s'appuyant sur un jeu de données fictif préparé et automatisé.

Yannick a parlé de l'anonymisation partielle (uniquement les usagers) de la base de donnée de production pour pouvoir la dupliquer en démo et surtout en recette. Cette piste permettrait à chaque référente de « retrouver » sa propre configuration et de pouvoir vérifier si pour son contexte, la fonctionnalité apporte ce qui est attendue.

L'équipe doit discuter un peu de ces propositions pour peser le pour et le contre de chacune, voir s'il existe des alternatives ou des pièges et contraintes non évoquées ici.

### Roadmap

Au dernier COPIL il a été acté que l'ANCT proposerait une roadmap pour orienter le service en donnant un cap sur un horizon de 6 mois avec un point trimestriel (à minima) pour rediscuter de cette roadmap.

Une première version à été discuté à la réunion aujourd'hui, et voici ce qu'il en ressort :\
ressort :

_Retiré_ **Flux ical** _(pour agent, pour lieux accueil, ...)_

Ce point proposait de travailler sur un élément technique facilitant les interactions avec les agendas. De l'avis général des personnes présentent, il n'y a pas de réel besoin. Ce n'est pas urgent.

Il reste donc 6 points dans la roadmap :

* [**RGAA**](https://www.numerique.gouv.fr/publications/rgaa-accessibilite/)
* **Migration HDS** (RGPD)

1. **Affinage des autorisations** (agents, motifs, agenda)
2. **RDV Collectif**
3. **Sectorisation**
4. **Statistiques** (export de données brutes)

Le RGAA et la migration vers un hébergeur de donnée de santé sont des sujets de fond, au long cours. Ils sont en cours, mais n'occupe pas l'équipe à plein temps. Du moins pour le moment.

Les 4 points restants ont été priorisé. Les statistiques à la fin, car aujourd'hui, la solution est relativement viable pour le moment. Et il manque beaucoup d'autres choses plus importantes.

### Motif associé à un service et notification

Les notifications SMS contiennent le nom du service. Quelle information seront transmise lorsque les motifs ne seront plus forcément associé à un service, mais plus largement et accessible à des agents de divers services ?

### Blocage déploiement CPEF dans la Drôme

Arrêt des déploiements pour le CPEF dans la Drôme. Le problème est lié au cloisonnement (agent double : médecin PMI qui ne peuvent pas faire avec service CPEF).

### Recherche de doublon

Il manque de la documentation à propos des mécanismes d'alerte et de blocage des doublons dans RDV Solidarités ?

Il existe une documentation à propos de l'[unicité de la fiche usager](https://doc.rdv-solidarites.fr/guide-utilisation/pour-les-agents/guide-dutilisation-pour-les-agents/bases-usagers#unicite-des-fiches-usagers). Elle n'est peut-être pas assez explicite ou nécessite d'être sur une page à part

Nous avons également parlé de la date de naissance. La rendre obligatoire est intéressant pour les doublons, mais peut poser des problèmes dans certains cas. Faut-il la rendre obligatoire et laisser la possibilité de mettre une date bidon ou bien faire en sorte que ça ne soit pas obligatoire, mais ajouter un message d'alerte sur le fait qu'elle n'est pas renseignée ?

### Proposer de reprendre un RDV

Lors de l'annulation de RDV (à l'initiative de l'usager ou de l'agent), il est intéressant de pouvoir envoyer une notification pour « inviter » l'usager à reprendre RDV.

https://github.com/betagouv/rdv-solidarites.fr/issues/1972
