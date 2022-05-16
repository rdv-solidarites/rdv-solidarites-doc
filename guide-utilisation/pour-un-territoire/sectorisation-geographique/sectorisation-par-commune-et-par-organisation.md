---
description: >-
  Cette page décrit comment configurer la sectorisation de RDV-Solidarités pour
  orienter les usagers vers les bonnes organisations en fonction de leur commune
  de résidence
---

# Exemple 1 : Par commune et par organisation

## Exemple

Dans cet exemple, nous étudierons un cas imaginaire et simplifié de configuration dans le Pas de Calais (62).

On imagine ici 3 organisations distinctes :

* MDS Site Arques
* MDS Site Erny
* MDS Locale Campagne

Ainsi que 2 Secteurs :

* Arques et environs
* Rural

et un ensemble de communes : Arques, Audicthun, Bomy ...

Voici une description schématique de la configuration d'exemple dans RDV-Solidarités :

![Schéma de la configuration de la sectorisation en exemple](../../../.gitbook/assets/sectorisation\_explanations-c08b09070b679859842b9a8e9f4f232a.png)

### **Recherche usager 1 : dans la commune AUDICTHUN**

La commune Audicthun est configurée et associée au secteur violet Arques et Environs.

Les créneaux proposés à l'usager seront ceux disponibles dans l'organisation "MDS Site Arques", la seule attribuée à ce secteur, ET pour des motifs sectorisés au niveau de l'organisation.

Si des motifs sectorisés au niveau du département existent dans une des trois organisations, les créneaux disponibles apparaîtront aussi pour l'usager.

### **Recherche usager 2 : dans la commune DELETTES**

La commune DELETTES est configurée et associée au secteur jaune Rural.

Les créneaux proposés à l'usager seront ceux disponibles dans les deux Organisations associées à ce secteur jaune : "MDS Site ERNY" et "MDS locale campagne" ET pour des motifs sectorisés au niveau de l'organisation.

Si des motifs sectorisés au niveau du département existent dans une des trois organisations, les créneaux disponibles apparaîtront aussi pour l'usager.

### **Recherche usager 3 : dans la commune BOMY**

La commune BOMY n'est pas configurée, elle n'est rattachée à aucun secteur.

Seuls les créneaux disponibles pour des motifs sectorisés au niveau du département entier apparaîtront pour l'usager.
