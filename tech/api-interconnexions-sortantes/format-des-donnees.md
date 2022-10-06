# Format des données

### RDV

```json
{
  "data": {
    "id": 8025,
    "address": "",
    "agents": [
      {
        "id": 1,
        "email": "martine@demo.rdv-solidarites.fr",
        "first_name": "Martine",
        "last_name": "Validay"
      }
    ],
    "cancelled_at": null,
    "collectif": false,
    "context": "",
    "created_by": "agent",
    "duration_in_min": 30,
    "ends_at": "2022-10-07 11:00:00 +0200",
    "lieu": null,
    "max_participants_count": null,
    "motif": {
      "id": 2,
      "category": null,
      "deleted_at": null,
      "location_type": "phone",
      "name": "Consultation gynécologie / contraception",
      "organisation_id": 1,
      "reservable_online": false,
      "service_id": 1
    },
    "name": null,
    "organisation": {
      "id": 1,
      "email": null,
      "name": "MDS Paris Nord",
      "phone_number": "0123456789"
    },
    "rdvs_users": [
      {
        "send_lifecycle_notifications": true,
        "send_reminder_notification": true,
        "status": "unknown",
        "user": {
          "id": 3,
          "address": null,
          "address_details": null,
          "affiliation_number": null,
          "birth_date": "1982-12-01",
          "birth_name": null,
          "caisse_affiliation": null,
          "case_number": null,
          "created_at": "2022-10-06 10:37:12 +0200",
          "email": "lea_dupont@demo.rdv-solidarites.fr",
          "family_situation": null,
          "first_name": "Léa",
          "invitation_accepted_at": null,
          "invitation_created_at": null,
          "last_name": "Dupont",
          "notify_by_email": true,
          "notify_by_sms": true,
          "number_of_children": null,
          "phone_number": "0101010102",
          "phone_number_formatted": "+33101010102",
          "responsible": null,
          "responsible_id": null,
          "user_profiles": null
        }
      }
    ],
    "starts_at": "2022-10-07 10:30:00 +0200",
    "status": "unknown",
    "users": [
      {
        "id": 3,
        "address": null,
        "address_details": null,
        "affiliation_number": null,
        "birth_date": "1982-12-01",
        "birth_name": null,
        "caisse_affiliation": null,
        "case_number": null,
        "created_at": "2022-10-06 10:37:12 +0200",
        "email": "lea_dupont@demo.rdv-solidarites.fr",
        "family_situation": null,
        "first_name": "Léa",
        "invitation_accepted_at": null,
        "invitation_created_at": null,
        "last_name": "Dupont",
        "notify_by_email": true,
        "notify_by_sms": true,
        "number_of_children": null,
        "phone_number": "0101010102",
        "phone_number_formatted": "+33101010102",
        "responsible": null,
        "responsible_id": null,
        "user_profiles": null
      }
    ],
    "users_count": 1,
    "uuid": "10af380f-13e2-4d44-9f60-47f8f381a7d7"
  },
  "meta": {
    "model": "Rdv",
    "event": "created",
    "timestamp": "2022-10-06 15:53:57 +0200"
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
