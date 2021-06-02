---
description: >-
  Décrit l'isolation des bases usagers, les contraintes d'unicité pour éviter
  les fiches doublons, et les champs des fiches usagers
---

# Fiches usagers

## Isolation des bases usagers

Chaque organisation a une liste d'usagers indépendante, \(même au sein d'un seul département\). Les usagers sont cependant partagés entre les différents services d'une organisation.

Un usager apparaît dans la liste d'une organisation dès qu'un agent y créé sa fiche, ou bien si cet usager prend RDV en ligne avec cette organisation.

Un usager peut apparaître dans la liste d'usagers de plusieurs organisations. Par exemple, en tant qu'usager je peux prendre RDV dans l'organisation du Nord des Yvelines puis dans l'organisation du Sud des Yvelines, voire plus tard dans l'organisation de l'agglomération de Pau si j'ai déménagé.

### Infos communes versus infos indépendantes

L'usager n'a qu'un seul compte unique : il se connecte avec une seule paire email - mot de passe. La majeure partie de ses informations sont uniques sur son compte : nom, prénom, date de naissance etc... Lorsque l'usager modifie ces informations, elles sont modifiées pour toutes les organisations. De même lorsqu'un agent modifie ces informations depuis son organisation, elles sont en fait modifiées pour toutes les organisations.

Il existe 2 champs sur les fiches usagers qui sont indépendants entre les organisations : le type de logement et les notes libres. Une organisation A peut donc renseigner des notes libres, l'organisation B ne pourra jamais accéder à ces notes, et pourra par contre prendre des notes différentes. 

### Rapatriement de comptes usagers d'une organisation à une autre

Lorsqu'un agent essaie de créer un compte usager avec des infos identiques à un compte usager existant dans une autre organisation, nous avertissons l'agent et l'invitons à "réutiliser" ce compte usager plutôt qu'en créer un nouveau qui serait potentiellement doublon.

Cet avertissement peut se produire sur l'email, le numéro de téléphone ou sur des combinaisons de champs d'identité civile \(noms, prénoms, dates de naissances ...\). Selon la contrainte d'unicité en question \(voir plus bas\), l'avertissement peut être ignoré ou non : dans certains cas vous serez obligés de réutiliser le compte existant ou bien de modifier les informations de la fiche usager à créer.

### Champs non-modifiables FranceConnect

Lorsqu'un usager s'est connecté via FranceConnect, ses informations d'identité civiles ont été "certifiées". Elles ne peuvent alors plus être modifiées, ni par l'usager, ni par les agents. Un message apparaît pour expliquer cette interdiction.

## Unicité des fiches usagers

### Email

L'email est unique, deux usagers ne peuvent pas utiliser le même email. Si un agent essaie de créer un compte avec un email déjà utilisé, une erreur apparaîtra. Si un usager essaie de créér un compte avec un email déjà utilisé, une erreur l'en empêchera.

### Numéro de téléphone

Plusieurs usagers peuvent avoir le même numéro de téléphone, il n'y a pas de contrainte d'unicité sur ce champ. C'est une demande assumée pour gérer les cas de familles partageant un téléphone mobile. Cependant, pour prévenir de fiches d'usagers doublons, nous affichons des avertissements non-bloquants lorsqu'un agent essaie de créer un compte usager avec un numéro de téléphone déjà utilisé.

RDV-Solidarités autorise les numéros de téléphone au format international \(+33 XX XX XX XX\) ou au format français à 10 chiffres. Au format international, vous pouvez saisir un numéro étranger. Au format français, vous pouvez saisir un numéro de france métropolitaine ou d’outre-mer. Pour que les sms soient correctement envoyés, assurez-vous de saisir un numéro de mobile.

### État civil

Comme pour le numéro de téléphone, nous n'imposons pas de contrainte stricte sur l'unicité des fiches usagers selon les infos d'état civil. Deux usagers peuvent donc avoir le même nom, prénom et date de naissance. Cependant, nous affichons des avertissements non-bloquants, pour éviter la multiplication des fiches doublons.



