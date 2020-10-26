# Interconnexions

RDV-Solidarités peut notifier n'importe quel système d'information accessible en ligne lors de **modifications** \(création, modification, suppression\) sur les **RDV,** les **plages d'ouvertures** et les **absences.**

Pour cela, ce système d'informations doit :

* être accessible à **une URL** publique par exemple [https://interconnexions.votre-departement.fr/rdv-solidarites](https://interconnexions.votre-departement.fr/rdv-solidarites)
* accepter des requêtes HTTP POST à cette URL

Aujourd'hui, **aucune** API **entrante** n'est mise en place pour le moment.

Certains départements ont avancé sur ces sujets là, vous trouverez des informations dédiées aux pages suivantes :

{% page-ref page="outlook.md" %}

{% page-ref page="microsoft-dynamics.md" %}

De plus, des expérimentations ont été menées, du [code](https://github.com/guillett/webhook) a été écrit en C\# et en NodeJS.

### Démonstration

Dans notre environnement de démonstration, nous pouvons envoyer des notifications sur une URL de test \(par exemple [https://webhook.site](https://webhook.site)\) ou envoyer des emails qui contiennent le contenu brut des notifications envoyées par les requêtes HTTP. Pour cela, [contactez-nous](contact@rdv-solidarites.fr) !

### Aspects plus techniques

#### Vérification des signatures des requêtes

Un secret partagé est associé à chacune de ces URLs pour vous permettre de vérifier que nous sommes bien à l'origine de l'envoi d'information.

La requête envoyée en HTTP POST contient une entête 'X-Lapin-Signature' qui contient une signature SHA256 hexadécimale du corps de la requête.

Pour la génération et la validation des signatures, vous pouvez consulter :

{% page-ref page="generation-de-signature.md" %}

#### Format des informations envoyées

La forme du contenu des requêtes est donnée pour les RDV et les plages d'ouvertures :

Pour un RDV :

```javascript
{
  "data": {
    "id": 1,
    "address": "",
    "agents": [
      {
        "id": 1,
        "email": "martine@demo.rdv-solidarites.fr",
        "first_name": "Martine",
        "last_name": "VALIDAY"
      }
    ],
    "duration_in_min": 30,
    "motif": {
      "id": 1,
      "location_type": "phone",
      "name": "Être rappelé par la PMI"
    },
    "organisation": {
      "id": 1,
      "departement": "75",
      "name": "MDS Paris Nord"
    },
    "starts_at": "2020-08-07 10:00:00 +0200",
    "status": "notexcused",
    "users": [
      {
        "id": 1,
        "address": null,
        "birth_date": "1975-06-20",
        "email": "patricia_duroy@demo.rdv-solidarites.fr",
        "first_name": "Patricia",
        "last_name": "DUROY",
        "phone_number": "01 23 45 67 89",
        "responsible": null
      }
    ],
    "uuid": "966f9fb3-3d9d-4548-b1b8-feaf08548d9e"
  },
  "meta": {
    "model": "Rdv",
    "event": "updated",
    "timestamp": "2020-08-04 10:46:03 +0200"
  }
}
```

Pour une plage d'ouverture

```javascript
{
  "data": {
    "id": 568,
    "agent": {
      "id": 294,
      "email": "vincent.parfait@pasdecalais.fr",
      "first_name": "Jean",
      "last_name": "Parfait"
    },
    "end_time": "18:00:00",
    "first_day": "2020-07-17",
    "ical": "BEGIN:VCALENDAR\r\nVERSION:2.0\r\nPRODID:RDV Solidarités\r\nCALSCALE:GREGORIAN\r\nMETHOD:REQUEST\r\nBEGIN:VTIMEZONE\r\nTZID:Europe/Paris\r\nBEGIN:DAYLIGHT\r\nDTSTART:20200329T030000\r\nTZOFFSETFROM:+0100\r\nTZOFFSETTO:+0200\r\nRRULE:FREQ=YEARLY;BYDAY=-1SU;BYMONTH=3\r\nTZNAME:CEST\r\nEND:DAYLIGHT\r\nBEGIN:STANDARD\r\nDTSTART:20201025T020000\r\nTZOFFSETFROM:+0200\r\nTZOFFSETTO:+0100\r\nRRULE:FREQ=YEARLY;BYDAY=-1SU;BYMONTH=10\r\nTZNAME:CET\r\nEND:STANDARD\r\nEND:VTIMEZONE\r\nBEGIN:VEVENT\r\nDTSTAMP:20200717T085543Z\r\nUID:plage_ouverture_568@RDV Solidarités\r\nDTSTART;TZID=Europe/Paris:20200717T160000\r\nDTEND;TZID=Europe/Paris:20200717T180000\r\nCLASS:PUBLIC\r\nDESCRIPTION:\r\nLOCATION:Rue du Commandant Lherminier 62700 Bruay-la-Buissière\r\nSUMMARY:RDV Solidarités test vt\r\nATTENDEE:mailto:vincent.parfait@pasdecalais.fr\r\nEND:VEVENT\r\nEND:VCALENDAR\r\n",
    "ical_uid": "plage_ouverture_568@RDV Solidarités",
    "lieu": {
      "id": 10,
      "address": "Rue du Commandant Lherminier 62700 Bruay-la-Buissière",
      "name": "CCAS de Bruay-la-Buissière"
    },
    "motifs": [
      {
        "id": 320,
        "name": "Consultation BCG"
      }
    ],
    "organisation": {
      "id": 1,
      "departement": "62",
      "name": "MDS Lapins"
    },
    "rrule": null,
    "start_time": "16:00:00",
    "title": "test vt"
  },
  "meta": {
    "model": "PlageOuverture",
    "event": "created",
    "timestamp": "2020-07-17 10:55:43 +0200"
  }
}
```

Il est possible de reproduire un appel fait par RDV-Solidarités vers un SI tiers \(ici `http://127.0.0.1:3000`\) en mettant le texte donné en exemple ci-dessus dans un fichier `XXXX.json` et d'utiliser la commande suivante

```bash
curl 'http://127.0.0.1:3000' --data @XXXX.json -H 'Content-Type: application/json; charset=utf-8'
```

Détails techniques :

* [https://github.com/betagouv/rdv-solidarites.fr/blob/master/app/jobs/webhook\_job.rb\#L11](https://github.com/betagouv/rdv-solidarites.fr/blob/master/app/jobs/webhook_job.rb#L11)
* [https://github.com/betagouv/rdv-solidarites.fr/tree/master/app/blueprints](https://github.com/betagouv/rdv-solidarites.fr/tree/master/app/blueprints)

Ça vous intéresse d'expérimenter, [contactez-nous](contact@rdv-solidarites.fr) !

Présentation faite aux DSIs : [https://docs.google.com/file/d/1leeQ1B507eNgi2pWfjaOor8TAtkhv6ao/edit?usp=docslist\_api&filetype=mspresentation](https://docs.google.com/file/d/1leeQ1B507eNgi2pWfjaOor8TAtkhv6ao/edit?usp=docslist_api&filetype=mspresentation)

