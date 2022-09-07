# Réunion référentes du 8 février 2022

### Production

* Améliore l'accessibilité de la page publique de statistique
* Corrige le problème de « se souvenir de moi » pour les connexions utilisateurs et agents
* Corrige la recherche par email
* Ajoute une pagination pour les agents référents
* Corrige l’affichage des notifications par usager dans l’historique Rdv
* Améliore la performance de la page listant les usagers
* Corrige le lien “Réinitialiser” de la recherche agents de la page de liste des agents du module de configuration
* Corrige la navigation vers les prochains créneaux

À venir dans la semaine

* Modification de l'interface du module de configuration
* Amélioration des performances de la fiche usager

_Demande d'ajout d'un lien vers la configuration depuis le menu paramètres pour accompagner le changement_

### À venir

* \[Bug] [Afficher des créneaux à venir](https://github.com/betagouv/rdv-solidarites.fr/issues/2013)
* \[Bug] [Considérer les délais min et max des motifs](https://github.com/betagouv/rdv-solidarites.fr/issues/2005)
* Accessibilité (RGAA)
* [Tiers lieux et visioconférence pour un RDV](https://github.com/betagouv/rdv-solidarites.fr/issues/1639)
* \[Bug] [Supprimer les doublons de lieux dans la recherche côté usager](https://github.com/betagouv/rdv-solidarites.fr/issues/1955)
* [Invitation et accès organisation depuis le module de configuration](https://github.com/betagouv/rdv-solidarites.fr/issues/2032)
* \[Bug] [Rediriger vers la connexion après une erreur de connexion](https://github.com/betagouv/rdv-solidarites.fr/issues/2029)
* \[Bug] [Permettre aux agents de réinitialiser leur mot de passe depuis la page de connexion d'usagers](https://github.com/betagouv/rdv-solidarites.fr/issues/1614)

### Suppression de motif

Marie (12) évoque les motifs qui ont été créés au début de l'expérimentation. Motif qui n'a plus aucun sens aujourd'hui. Elle aimerait les supprimer. Il n'y a rien dans l'application aujourd'hui pour supprimer des motifs, ni pour les désactiver.

Aujourd'hui, il existe la possibilité de désactiver un lieu, et la possibilité de supprimer un usager ou un agent (une fausse suppression, mais l'un comme l'autre ne sont plus visible dans l'application par la suite).

Après vérification, il existe aujourd'hui un mécanisme de suppression de motifs.

Dans le cas d'un motif qui a été utilisé pour un RDV (future ou passé), la suppression est une désactivation qui laisse les RDV associé à ce motif.

Si c'est un motif qui n'a pas de RDV, alors le motif est réellement supprimé.

Peut-être que dans certains cas, cela ne fonctionne pas ? L'équipe va faire un message à Marie pour en savoir plus.

### Droits d'accès

Nous avons agrégé [vos retours dans un tableau](https://docs.google.com/spreadsheets/d/1eT1M7N4nHDS8a11Q0ZKpUMqcPZ2K-AgabLJ3kUA6PeQ/edit?usp=drive\_web\&ouid=105077925985295860964) (un onglet par département pour le moment). L'idée sera ensuite de chercher les écarts et les points communs pour appuyer notre décision.

Pour rappel, nous envisageons deux options pour la gestion des droits d'accès :

* affecter les droits agents par agent ;
* créer des rôles avec des droits puis d'affecter un rôle à un agent

### RGPD

Un [sondage](https://framadate.org/4uBeGYeXP5gKFgaG) est en cours pour l'organisation d'un atelier autour du RGPD et de son impact sur le service.

### Organisation

Qu'est-ce qu'une organisation ?

Une question que nous allons aborder dans les semaines à venir. Nous le ferons sans doute autour d'un atelier.

Quelques éléments de réponses évoquées qui pourront être exploré durant cet atelier à venir :

* une organisation est un élément de sectorisation
* une organisation facilite la gestion du contact téléphonique
