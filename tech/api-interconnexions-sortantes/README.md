---
description: >-
  RDV-Solidarités peut notifier votre système d’information à l’aide de webhooks
  ou en envoyant des ics par email.
---

# API de notifications

RDV-Solidarités peut notifier n'importe quel système d'information accessible en ligne lors de **modifications** (création, modification, suppression) sur les **RDV,** les **plages d'ouvertures**, les **absences** et les **usagers.**

Pour cela, ce système d'informations doit :

* être accessible à **une URL** publique par exemple [https://interconnexions.votre-departement.fr/rdv-solidarites](https://interconnexions.votre-departement.fr/rdv-solidarites)
* accepter des requêtes HTTP POST à cette URL.

Certains départements ont développé des solutions sur ces sujets :

* pour [Outlook](broken-reference)&#x20;
* pour [Microsoft Dynamics](broken-reference)

Du code d’exemple est aussi [disponible en C# et en NodeJS](https://github.com/guillett/webhook).

### Démonstration

Dans notre environnement de démonstration, nous pouvons envoyer des notifications sur une URL de test (par exemple [https://webhook.site](https://webhook.site)) ou envoyer des emails qui contiennent le contenu brut des notifications envoyées par les requêtes HTTP. Pour cela, [contactez-nous](https://app.gitbook.com/s/-MG9-\_JuLUdv0lRqkUMW/guide-pour-un-charge-dinformatique/contact@rdv-solidarites.fr) !

### Signatures des requêtes

Un secret partagé est associé à chacune de ces URLs pour vous permettre de vérifier que nous sommes bien à l'origine de l'envoi d'information. La requête envoyée en HTTP POST contient un entête `X-Lapin-Signature` qui contient une signature SHA256 hexadécimale du corps de la requête.  [Comment vérifier la signature ?](broken-reference)

### Format des données

Les RDV, les plages d’ouvertures, les absences et les usagers sont envoyés en json, une requête par évènement de création, modification ou suppression. [Format des données](broken-reference).

### Tests

Il est possible de reproduire un appel fait par RDV-Solidarités vers un SI tiers (ici `http://127.0.0.1:3000`) en mettant le texte donné en exemple ci-dessus dans un fichier `XXXX.json` et d'utiliser la commande suivante

```bash
curl 'http://127.0.0.1:3000' --data @XXXX.json -H 'Content-Type: application/json; charset=utf-8'
```

### Implémentation côté RDV-Solidarités

* [https://github.com/betagouv/rdv-solidarites.fr/blob/master/app/jobs/webhook\_job.rb#L11](https://github.com/betagouv/rdv-solidarites.fr/blob/master/app/jobs/webhook\_job.rb#L11)
* [https://github.com/betagouv/rdv-solidarites.fr/tree/master/app/blueprints](https://github.com/betagouv/rdv-solidarites.fr/tree/master/app/blueprints)

Présentation faite aux DSIs : [https://docs.google.com/file/d/1leeQ1B507eNgi2pWfjaOor8TAtkhv6ao/edit?usp=docslist\_api\&filetype=mspresentation](https://docs.google.com/file/d/1leeQ1B507eNgi2pWfjaOor8TAtkhv6ao/edit?usp=docslist\_api\&filetype=mspresentation)

### Emails et icalendar

En plus des webhooks, RDV-Solidarités peut notifier votre SI en [envoyant des emails aux agents](broken-reference).
