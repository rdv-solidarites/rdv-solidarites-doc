# Format des données

### RDV

_note : le format contient maintenant des champs optionnels : numéro de dossier, complément d'adresse, ...._

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
    "cancelled_at": "2020-08-04 10:00:00 +0200",
    "created_by": "user",
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
    "status": "noshow",
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

### Plage d'ouverture

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

### Indisponibilité

```json
{
    "data":{
        "id":2,
        "agent":{
            "id":1,
            "email":"martine@demo.rdv-solidarites.fr",
            "first_name":"Martine",
            "last_name":"Validay"
        },
        "end_day":"2022-03-25",
        "end_time":"18:00:00",
        "first_day":"2022-03-24",
        "ical":"BEGIN:VCALENDAR\r\nVERSION:2.0\r\nPRODID:RDV Solidarités\r\nCALSCALE:GREGORIAN\r\nMETHOD:PUBLISH\r\nBEGIN:VTIMEZONE\r\nTZID:Europe/Paris\r\nBEGIN:DAYLIGHT\r\nDTSTART:20220327T030000\r\nTZOFFSETFROM:+0100\r\nTZOFFSETTO:+0200\r\nRRULE:FREQ=YEARLY;BYDAY=-1SU;BYMONTH=3\r\nTZNAME:CEST\r\nEND:DAYLIGHT\r\nBEGIN:STANDARD\r\nDTSTART:20211031T020000\r\nTZOFFSETFROM:+0200\r\nTZOFFSETTO:+0100\r\nRRULE:FREQ=YEARLY;BYDAY=-1SU;BYMONTH=10\r\nTZNAME:CET\r\nEND:STANDARD\r\nEND:VTIMEZONE\r\nBEGIN:VEVENT\r\nDTSTAMP:20220315T204727Z\r\nUID:absence_2@RDV Solidarités\r\nDTSTART;TZID=Europe/Paris:20220324T090000\r\nDTEND;TZID=Europe/Paris:20220325T180000\r\nORGANIZER:mailto:secretariat-auto@rdv-solidarites.fr\r\nSUMMARY:RDV Solidarités Formation\r\nEND:VEVENT\r\nEND:VCALENDAR\r\n",
        "ical_uid":"absence_2@RDV Solidarités",
        "organisation":{
            "id":1,
            "email":null,
            "name":"MDS Paris Nord",
            "phone_number":"0123456789"
        },
        "rrule":null,
        "start_time":"09:00:00",
        "title":"Formation"
    },
    "meta":{
        "model":"Absence",
        "event":"created",
        "timestamp":"2022-03-15 21:47:27 +0100"
    }
}
```

### Usager

```json
{
    "data": {
            "logement":"locataire",
            "notes":"Une remarque pour l'exemple",
            "organisation":{
                    "id":1,
                    "email":null,
                    "name":"MDS Paris Nord",
                    "phone_number":"0123456789"
            },
            "user":{
                    "id":10007,
                    "address":"2 La Place, Éperlecques, 62910, 62, Pas-de-Calais, Hauts-de-France",
                    "address_details":"appartement 31234",
                    "affiliation_number":"123456789",
                    "birth_date":"1970-03-12",
                    "birth_name":null,
                    "caisse_affiliation":"caf",
                    "case_number":"5498465789",
                    "created_at":"2022-03-15 21:27:58 +0100",
                    "email":"louis@yahoo.fr",
                    "family_situation":"divorced",
                    "first_name":"Louis",
                    "invitation_accepted_at":null,
                    "invitation_created_at":null,
                    "last_name":"Amstrong",
                    "notify_by_email":true,
                    "notify_by_sms":true,
                    "number_of_children":6,
                    "phone_number":"0699999999",
                    "phone_number_formatted":"+33699999999",
                    "responsible":null,
                    "responsible_id":null,
                    "user_profiles":null
            }
    },
    "meta":{
            "model":"UserProfile",
            "event":"updated",
            "timestmp":"2022-03-15 21:42:33 +0100"
    }
}
```
