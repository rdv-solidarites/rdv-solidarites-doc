---
description: RDV Collectif, interconnexion, notification, format d'adresse,
---

# Réunion référentes du 5 avril 2022

## RDV Collectif

* Démonstration de l'intégration des RDV collectifs dans la recherche de créneau.
* Mise en place d'un intitulé optionnel dans les RDV collectifs uniquement permettant de spécifier le contenu des ateliers. **Il serait nécessaire d'afficher** cet intitulé **dans les notifications par email (avec** où **à la place) des motifs**

### Interconnexion

Nous avons un peu de retard sur les webhook. Il manque, dans la documentation et dans le code peut-être

* les champs optionnels
* les nouveaux champs (numéro de dossier et complément d'adresse)
* les lieux ponctuels dans les RDV
* les infos liées au RDV collectif

### Format d'adresse

[Formater les anciennes adresses de lieux pour qu'elles soient plus courtes #2293](https://github.com/betagouv/rdv-solidarites.fr/issues/2293)

Les nouvelles adresses sont maintenant plus courtes.

### Notification

Nous nous étions posés la question de la compréhension des notifications SMS et courriel.

Les DPD souhaiteraient que nous ne mettions plus les motifs dans les notifications courriel. Les SMS sont encore un peu trop longs (coût double).

Dans les SMS, pour les VAD ou les RDV téléphoniques, le tel qui est affiché, c'est celui de l'organisation. Une organisation contient plusieurs lieux. Difficile de transmettre le bon numéro de téléphone

Élodie (62) fait remarquer que la date contient le jour de la semaine. Peut-être que nous pourrions l'enlever.

Si l'usager n'a pas eu de contact physique avant la notification, elle est difficilement compréhensible. Est-ce que ce sont des cas courant ? Combien de RDV les usagers ont de RDV en moyenne ? En médian ? Est-ce que les usagers se « perdent » dans les notifications ?

Voilà des pistes à explorer directement auprès des usagers.

### Agenda

[Masque ou affiche les rdv annulés #2322](https://github.com/betagouv/rdv-solidarites.fr/pull/2322)

### Trouver un RDV

[Simplifie l'acces à la recherche de créneaux #2324](https://github.com/betagouv/rdv-solidarites.fr/pull/2324)

Avant de mettre en production, nous allons faire en sorte que le bouton dans le menu soit contextuel et prenne en compte le fait que l'on est sur une fiche usager.
