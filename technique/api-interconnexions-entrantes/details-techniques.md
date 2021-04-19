# Détails techniques

L'API supporte uniquement le format JSON. Toutes les réponses envoyées par l'API contiendront le header `Content-Type: application/json` et leur contenu sera présent dans le body dans un format JSON à désérialiser. 

L'API adhère aux principes REST : 

* requêtes `GET` : lecture sans modification
* requêtes `POST` : création de nouvelle ressource
* requêtes `PUT` : mise à jour d'une ressource existante
* requêtes `DELETE` : suppression d'une ressource

Les paramètres des requêtes `GET` doivent être envoyés via les query string de la requête. 

Les paramètres des requêtes `POST` doivent être transmis dans le corps de la requête sous un format JSON valide, et doivent contenir le header `Content-Type: application/json`

Les paramètres doivent respecter les formats suivants : 

* `DATE` : "YYYY-MM-DD" par exemple : "2021-10-21"
* `TIME` : H:m\[:s\], par exemple : "10:30"

Les statuts HTTP des réponses renvoyées par l'API peuvent être les suivants :

* `200` : succès
* `400` : requête mal formatée. Par exemple si le JSON du body est invalide.
* `401` : requête non authentifiée
* `403` : requête bien authentifiée mais droits insuffisants pour réaliser l'action demandée. Par exemple si un agent non-admin essaie de créer une absence pour un agent d'un autre service.
* `422` : paramètres sains \(JSON valide\) mais incorrects. Par exemple si vous essayez de créer une absence avec une date de fin antérieure à sa date de début.
* `500` : erreur interne. Nous sommes automatiquement prévus de ces erreurs et devrions nous en occuper rapidement. Vous pouvez nous contacter si cela se reproduit.

{% hint style="warning" %}
La pagination n'est pas encore implémentée. Les tableaux de ressources renvoyés sont limités à 100 pour l'instant.
{% endhint %}

En cas d'erreur reconnue par le système \(par exemple erreur 422\), les champs suivants seront présents dans la réponse pour vous informer sur les problèmes :

* `errors` : \[ERREUR\] : liste d'erreurs groupées par attribut problèmatique au format machine
* `error_messages` : \[ERREUR\] : idem mais dans un format plus facilement lisible

