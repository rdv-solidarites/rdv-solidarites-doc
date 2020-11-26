---
description: >-
  RDV-Solidarités permet d'orienter les usagers vers le bon service et les bons
  agents en fonction de leur adresse
---

# Sectorisation géographique

{% hint style="warning" %}
Cette page décrit des fonctionnalités qui vont être déployées d'ici quelques jours
{% endhint %}

## Fonctionnement

La sectorisation permet de définir des secteurs géographiques et de leur attribuer des responsables. Les usagers sont orientés vers les bons responsables selon l'adresse saisie lors de leur prise de RDV en ligne.

![Exemple de carte de sectorisation dans le Pas de Calais](../.gitbook/assets/screenshot_2020-11-26_at_10.58.08.png)

### Secteurs

Chaque secteur est défini comme un ensemble de communes ou de rues.

Chaque secteur est attribué à une ou plusieurs organisations entières ou bien à un ou plusieurs agents spécifiques.

### Motifs

Chaque motif a un niveau de sectorisation propre parmi les trois possibles : 

* **niveau département** : les créneaux pour ce motif apparaîtront pour les recherches d'usagers depuis l'ensemble du département
* **niveau organisation** : les créneaux pour ce motif apparaîtront pour les recherches d'usagers couvertes par des secteurs attribués à des organisations entières
* **niveau agent** : les créneaux pour ce motif apparaîtront pour les recherches d'usagers couvertes par des secteurs attribués à des agents spécifiques

### Combinaison pour qu'un motif apparaisse dans une recherche usager

Dans les recherches usagers, des créneaux apparaissent donc quand : 

* le motif est sectorisé au niveau du département OU 
* le motif est sectorisé au niveau de l'organisation ET un secteur géographique correspond à l'adresse recherchée par l'usager ET ce secteur est attribué à l'organisation entière OU
* le motif est sectorisé au niveau de l'agent ET un secteur géographique correspond à l'adresse recherchée par l'usager ET ce secteur est attribué à un agent 

\(il faut aussi que les conditions hors-sectorisation soient remplies : que le motif soit marqué "réservable en ligne", et que l'agent ait une plage d'ouverture à venir pour ce motif\)

### Configuration et permissions

Les agents n'ayant pas le rôle Administrateur ne peuvent configurer ni les motifs ni les secteurs.

Les agents avec le rôle Administrateur peuvent configurer les secteurs de leurs organisations uniquement. Ces agents voient les secteurs des autres organisations du département; mais ne peuvent pas les éditer

## Exemples

{% page-ref page="sectorisation-par-commune-et-par-organisation.md" %}

{% page-ref page="sectorisation-par-rue.md" %}





