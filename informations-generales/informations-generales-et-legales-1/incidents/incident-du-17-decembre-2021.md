---
description: >-
  À propos du nouveau calculateur de créneau et d'un nouveau parcours
  d'affichage des créneaux disponible.
---

# Incident du 17 décembre 2021

### Les faits

Jeudi 16 décembre, mise en production, en fin de journée, du nouveau calculateur de créneau, d'un changement d'organisation de l'affichage de la recherche de créneau côté agent et d'autres points.

Vendredi 17 décembre \~ 10 h 00, plusieurs emails de référentes et d'agents dans la boite de l'équipe. Il y a plusieurs problèmes en production

Nous avons entamé une analyse du problème pour essayer de le résoudre plutôt que de revenir en arrière. Il semble que des absences ne soient pas prises en compte.

À 11 h 00, nous n'arrivons pas à trouver de solution pour chaque problème. Nous revenons en arrière sur ces deux points. Les choses rentrent dans l'ordre peu de temps après.

### Problème sur le moteur de créneau

Nous pensions avoir bien testé le moteur, mais plusieurs cas sont resté dans notre angle mort.

Plus tard, avec une copie des données de production, nous avons pu faire des tests comparatifs entre ce que le moteur de calcul actuellement en production propose et ce que le nouveau moteur propose. Il y a plusieurs écarts.

#### Leçon

Il nous a manqué une personne (ou plusieurs ?) effectuant des tests poussés, sur divers cas.

Difficile de recruter une personne spécifiquement dédiée aux tests. Et les personnes dans l'équipe ne sont pas forcément au courant de l'ensemble des cas possible.

S'appuyer sur la communauté de référentes est sans doute un bon moyen de vérifier certaines fonctionnalités importantes.

Comment permettre ça ?

Les personnes référentes ont besoin d'avoir un environnement qu'elles connaissent. C'est aussi une garantie que les tests se déroulent au plus proche de situation de production.

Nous pourrions anonymiser les données (de manière destructive, sans pouvoir refaire le lien inverse), et injecter tout ou partie dans la base de recette (et pourquoi pas démo également ?) pour permettre un environnement similaire à la production et faciliter les tests réalisés par quelques personnes référentes volontaires.

_Cet export devra aussi masquer les adresses_ postales\_. Comment faire alors pour garder une cohérence pour tester la sectorisation ?\_

### Interface de recherche de créneau agent

Nous avons également exploré les problèmes liés au multiple façon d'arriver sur la page de résultat de recherche de créneau. Page que nous avons déplacé et qui impact chacun de ces points.

#### Leçon

Nous n'avons pas une visibilité claire de l'ensemble de l'application. Une cartographie du service nous permettrais sans doute de penser à vérifier chaque chemin.

C'est un travail amorcé dans le cadre de notre démarche d'amélioration de l'accessibilité.

Ce problème est donc une raison supplémentaire de faire cette carte.
