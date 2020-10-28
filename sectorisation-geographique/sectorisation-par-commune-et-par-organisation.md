---
description: >-
  Cette page décrit comment configurer la sectorisation de RDV-Solidarités pour
  orienter les usagers vers les bons agents en fonction de leur commune de
  résidence
---

# Sectorisation par commune et par organisation

## Exemple

Dans cet exemple, nous étudierons un cas imaginaire et simplifié de configuration dans le Pas de Calais \(62\). 

On imagine ici 3 organisations distinctes : 

* MDS Site Arques
* MDS Site Erny
* MDS Locale Campagne

Ainsi que 2 Secteurs : 

* Arques et environs
* Rural

et un ensemble de communes : Arques, Audicthun, Bomy ...

Voici une description schématique de la configuration d'exemple dans RDV-Solidarités :

![Sch&#xE9;ma de la configuration de la sectorisation en exemple](../.gitbook/assets/sectorisation_explanations-c08b09070b679859842b9a8e9f4f232a.png)

### **Recherche usager 1 : dans la commune AUDICTHUN**

La commune Audicthun est configurée et associée au secteur violet Arques et Environs. 

Les créneaux proposés à l'usager seront ceux disponibles dans l'organisation "MDS Site Arques", la seule attribuée à ce secteur.

### **Recherche usager 2 : dans la commune DELETTES**

La commune DELETTES est configurée et associée au secteur jaune Rural.

Les créneaux proposés à l'usager seront ceux disponibles dans les deux Organisations associées à ce secteur jaune : "MDS Site ERNY" et "MDS locale campagne"

### **Recherche usager 3 : dans la commune BOMY**

La commune BOMY n'est pas configurée, elle n'est rattachée à aucun secteur.

Aucun RDV ne sera donc proposé à l'usager, il lui sera indiqué que la prise de RDV en ligne n'est pas disponible à son adresse.
