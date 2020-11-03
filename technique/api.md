---
description: >-
  L'API de RDV-Solidarités ouvre une interface programmatique à RDV-Solidarités
  et vous permet de lire, créer et modifier des données dans notre base depuis
  votre logiciel
---

# API

{% hint style="danger" %}
L'API est en cours de développement, cette page anticipe les fonctionnalités à venir
{% endhint %}

## Différences avec l'interconnexion

Par [Interconnexion](interconnexions/) nous entendons l'interfaçage d'autres logiciels avec des fonctionnalités de calendrier similaires \(Outlook, MS Dynamics\) etc. 

Du point de vue de RDV-Solidarités, l'interconnexion est sortante \(nous envoyons des requêtes vers vos SI\) tandis que l'API est entrante \(nous recevons des requêtes depuis vos SI\)

## Détails techniques

L'API supporte uniquement le format JSON. Toutes les réponses envoyées par l'API contiendront le header `Content-Type: application/json` et leur contenu sera présent dans le body dans un format JSON à désérialiser. 

L'API adhère aux principes REST : 

* requêtes GET : lecture sans modification
* requêtes POST : création de nouvelle ressource
* requêtes PUT : mise à jour d'une ressource existante
* requêtes DELETE : suppression d'une ressource

Les paramètres des requêtes `GET` doivent être envoyés via les query string de la requête. 

Les paramètres des requêtes `POST` doivent être transmis dans le corps de la requête sous un format JSON valide, et doivent contenir le header `Content-Type: application/json`

Les paramètres doivent respecter les formats suivants : 

* `DATE` : DD/MM/YYYY, par exemple : "21/10/2021"
* `TIME` : H:m, par exemple : "10:30"

Les statuts HTTP des réponses renvoyées par l'API peuvent être les suivants :

* `200` : succès
* `401` : requête non authentifiée
* `403` : requête bien authentifiée mais droits insuffisants pour réaliser l'action demandée. Par exemple si un agent non-admin essaie de créer une absence pour un agent d'un autre service.
* `422` : paramètres reçus et bien formattés mais invalides. Par exemple si vous essayez de créer une absence avec une date de fin antérieure à sa date de début.
* `500` : erreur interne. Nous sommes automatiquement prévus de ces erreurs et devrions nous en occuper rapidement. Vous pouvez nous contacter si cela se reproduit.

⚠️ La pagination n'est pas encore implémentée. Les tableaux de ressources renvoyés sont limités à 100 pour l'instant.

## Authentification

Tous les agents peuvent utiliser l'API. Les requêtes faites sur l'API sont authentifiées grace à des tokens d'accès associés à chaque agent. Chaque action faite via l'API est donc attribuable à un agent.

Pour récupérer le token d'accès d'un agent il faut faire une première requête POST à l'url `https://rdv-solidarites.fr/api/v1/auth/sign_in` en passant en paramètres JSON l'email et le mot de passe de l'agent. Par exemple : 

{% tabs %}
{% tab title="httpie" %}
```bash
http --json POST 'http://localhost:5000/api/v1/auth/sign_in' \
  email='martine@demo.rdv-solidarites.fr' password='123456'
```
{% endtab %}

{% tab title="curl" %}
```bash
curl --verbose --request 'POST' \
  --header 'Content-Type: application/json' \
  --data '{"email":"martine@demo.rdv-solidarites.fr", "password":"123456"}' \
  'http://localhost:5000/api/v1/auth/sign_in'
```
{% endtab %}
{% endtabs %}

En cas de succès d'authentification, la réponse à cette requête contiendra dans le corps le détail de l'agent, et dans les headers les token d'accès à l'API. Par exemple :

```text
< HTTP/1.1 200 OK
< X-Frame-Options: SAMEORIGIN
< X-XSS-Protection: 1; mode=block
< X-Content-Type-Options: nosniff
< X-Download-Options: noopen
< X-Permitted-Cross-Domain-Policies: none
< Referrer-Policy: strict-origin-when-cross-origin
< Content-Type: application/json; charset=utf-8
< access-token: SFYBngO55ImjD1HOcv-ivQ
< token-type: Bearer
< client: Z6EihQAY9NWsZByfZ47i_Q
< expiry: 1605600758
< uid: martine@demo.rdv-solidarites.fr
< ETag: W/"0fe52663d6745c922160384e13afe1e1"
< Cache-Control: max-age=0, private, must-revalidate
< X-Meta-Request-Version: 0.7.2
< X-Request-Id: 291fab6a-043b-4b9c-b4b9-3c7fc9c9453a
< X-Runtime: 0.194743
< Transfer-Encoding: chunked
<
* Connection #0 to host rdv-solidarites.fr left intact
{"data":{"id":1,"deleted_at":null,"email":"martine@demo.rdv-solidarites.fr","provider":"email","service_id":1,"role":"admin","last_name":"VALIDAY","first_name":"Martine","uid":"martine@demo.rdv-solidarites.fr","email_original":null,"allow_password_change":false}}* Closing connection 0
```

Les 3 headers essentiels pour l'authentification sont les suivants : 

```text
access-token: SFYBngO55ImjD1HOcv-ivQ
client: Z6EihQAY9NWsZByfZ47i_Q
uid: martine@demo.rdv-solidarites.fr
```

* `access-token` : c'est le jeton d'accès qui vous a été attribué. Il a une durée de vie de 24h, après ça il vous faudra reproduire cette procédure pour en récupérer un nouveau
* `client`: un identifiant unique associé à l'appareil depuis lequel vous avez effectué la requête 
* `uid`: l'identifiant de l'agent dans l'API, égal à l'email de l'agent.

**Ces 3 headers doivent être transmis avec chacune de vos requêtes successives à l'API**, peu importe la méthode HTTP 

## Permissions

Les rôles et permissions des agents sont les mêmes via l'API que depuis l'interface web.

C'est à dire que les agents classiques ont accès à leur service uniquement, les agents du service secrétariat peuvent accéder aux agendas des agents des autres services, les agents admin ont accès à toute l'organisation, etc...

Par défaut, les requêtes en lecture n'appliquent aucun filtre et retourneront toutes les ressources auxquelles a accès l'agent connecté. Par exemple si un agent admin fait une requête pour accéder à la liste des absences sans filtre, l'API retournera toutes les absences de tous les agents appartenant aux organisations dont fait partie cet agent admin, ce qui peut faire beaucoup.

## Ressources

### Absences

#### GET /api/v1/absences

Paramètres : 

* `organisation_id`  INTEGER - _optionnel_ : filtre les absences retournées pour une seule organisation

Réponse : 

* `absences` : ARRAY\[ABSENCE\]

Exemple de requête :

{% tabs %}
{% tab title="httpie" %}
```bash
$ http 'http://localhost:5000/api/v1/absences' \
 access-token:FLXP6G2hIEYhmGe5MpHKfg \
 client:fySY0UMlNzgbhE8QYhXdkw \
 uid:'martine@demo.rdv-solidarites.fr'

HTTP/1.1 200 OK
...

{
    "absences": [
        {
            "agent": {
                "email": "martine@demo.rdv-solidarites.fr",
                "first_name": "Martine",
                "id": 1,
                "last_name": "VALIDAY"
            },
            "end_day": "2021-01-05",
            "end_time": "08:00:00",
            "first_day": "2020-12-23",
            "ical_uid": "absence_14@RDV Solidarités",
            "id": 14,
            "organisation": {
                "departement": "75",
                "id": 1,
                "name": "MDS Paris Nord"
            },
            "start_time": "08:00:00",
            "title": "Vacances de Noël"
        },
        {
            ...
        }
    ]
}

```
{% endtab %}

{% tab title="curl" %}
```bash
$ curl --verbose \
  --header 'access-token: FLXP6G2hIEYhmGe5MpHKfg' \
  --header 'client: fySY0UMlNzgbhE8QYhXdkw' \
  --header 'uid: martine@demo.rdv-solidarites.fr' \
  'http://localhost:5000/api/v1/absences'

...
< HTTP/1.1 200 OK
...

{"absences":[{"id":14,"agent":{"id":1,"email":"martine@demo.rdv-solidarites.fr","first_name":"Martine","last_name":"VALIDAY"},"end_day":"2021-01-05","end_time":"08:00:00","first_day":"2020-12-23","ical_uid":"absence_14@RDV Solidarités","organisation":{"id":1,"departement":"75","name":"MDS Paris Nord"},"start_time":"08:00:00","title":"Vacances de Noël"},{"id":13,"agent":{"id":1,"email":"martine@demo.rdv-solidarites.fr","first_name":"Martine","last_name":"VALIDAY"},"end_day":"2020-11-20","end_time":"18:00:00","first_day":"2020-11-20","ical_uid":"absence_13@RDV Solidarités","organisation":{"id":1,"departement":"75","name":"MDS Paris Nord"},"start_time":"08:00:00","title":"Congé parental"}]}

```
{% endtab %}
{% endtabs %}

#### POST /api/v1/absences

Paramètres :

* `organisation_id` INTEGER : l'identifiant de l'organisation dans laquelle créer une absence
* `agent_id` INTEGER : l'identifiant de l'agent absent
* `first_day` DATE : le jour de début de l'absence
* `start_time` TIME : l'heure de début de l'absence
* `end_day` DATE : le jour de fin de l'absence
* `end_time` TIME : l'heure de fin de l'absence

Réponse :

* `errors` ARRAY\[STRING\] : uniquement présent quand l'absence n'a pas pu être créée. Contient une liste d'erreurs groupées par champ.
* `absence` : ABSENCE : uniquement présent quand l'absence a été créée avec succès. Contient l'absence qui vient d'être créée.

Exemple de requête : 

{% tabs %}
{% tab title="httpie" %}
```bash
$ http --json POST http://localhost:5000/api/v1/absences \
  access-token:FLXP6G2hIEYhmGe5MpHKfg \
  client:fySY0UMlNzgbhE8QYhXdkw \
  uid:martine@demo.rdv-solidarites.fr \
  organisation_id=1 \
  agent_id=1 \
  title="Congé parental" \
  first_day="20/11/2020" \
  start_time="08:00" \
  end_day="20/11/2020" \
  end_time="18:00"

HTTP/1.1 200 OK
...

{
    "absence": {
        "agent": {
            "email": "martine@demo.rdv-solidarites.fr",
            "first_name": "Martine",
            "id": 1,
            "last_name": "VALIDAY"
        },
        "end_day": "2020-11-20",
        "end_time": "18:00:00",
        "first_day": "2020-11-20",
        "ical_uid": "absence_10@RDV Solidarités",
        "id": 10,
        "organisation": {
            "departement": "75",
            "id": 1,
            "name": "MDS Paris Nord"
        },
        "start_time": "08:00:00",
        "title": "Congé parental"
    }
}

```
{% endtab %}

{% tab title="curl" %}
```
$ curl --verbose --request 'POST' \
  --header 'access-token: FLXP6G2hIEYhmGe5MpHKfg' \
  --header 'client: fySY0UMlNzgbhE8QYhXdkw' \
  --header 'uid: martine@demo.rdv-solidarites.fr' \
  --header 'Content-Type: application/json' \
  --data '{"agent_id":"1","end_day":"20/11/2020","end_time":"18:00","first_day":"20/11/2020","organisation_id":"1","start_time":"08:00","title":"Congé parental"}' \
  'http://localhost:5000/api/v1/absences'

...
< HTTP/1.1 200 OK
...

{"absence":{"id":12,"agent":{"id":1,"email":"martine@demo.rdv-solidarites.fr","first_name":"Martine","last_name":"VALIDAY"},"end_day":"2020-11-20","end_time":"18:00:00","first_day":"2020-11-20","ical_uid":"absence_12@RDV Solidarités","organisation":{"id":1,"departement":"75","name":"MDS Paris Nord"},"start_time":"08:00:00","title":"Congé parental"}}

```
{% endtab %}
{% endtabs %}



