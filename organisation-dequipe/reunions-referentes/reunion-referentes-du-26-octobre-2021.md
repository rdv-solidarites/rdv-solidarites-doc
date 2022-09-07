# Réunion référentes du 26 octobre 2021

### Performances

* travaux réalisés ([https://github.com/betagouv/rdv-solidarites.fr/issues/1754](https://github.com/betagouv/rdv-solidarites.fr/issues/1754))
* infrastructure (outils d’analyse, tableau de bord sur scalingo, www, redis et postgresql)
* **reste à faire : optimisation des recherches de créneaux**

### En production

* ajustements sur l’affichage de l’historique
* index sur la recherche texte
* redis
  * mise en cache des résultats intermédiaires des recherches de créneaux
  * de l’historique des modifications
* bugs corrigés :
  * erreurs au chargement du calendrier pour certains agents (suite à des changements de file d’attente)
  * lien visible (et inopérant) vers la “prochaine disponibilité)

### En recette

* Renommer “Absence” par “Indisponibilité”
* (en recette en fin de matinée) Corrections sur l’intégration Outlook/Zimbra (fichiers .ics)

### En cours

* Débrayer l’envoi de notification au rendez-vous #1617
* Faciliter l’accès aux RDV à renseigner #1788

### Priorisé :

* Pouvoir créer des RDV effectués en binôme d’agents de services différents
  * Refaire le point sur la création de Rdv en binôme d’agents de services différents
  * C’est lié au décloisonnement. -> Yannick a une opinion sur le sujet
* Tiers lieux et visioconférence pour un RDV

### Trie des résultats de recherche

* Il faudrait trier les résultats de recherche des usagers par nom _puis_ prénom.
  * (ancien sujet de forum? je ne l’ai pas retrouvé.)
  * \-> Créer un nouveau ticket : [https://github.com/betagouv/rdv-solidarites.fr/issues/1836](https://github.com/betagouv/rdv-solidarites.fr/issues/1836)

### Protocole de recette

* Prévenir [equipe@rdv-solidarites.fr](mailto:equipe@rdv-solidarites.fr) sur les changements en recette :
  * Renommage d'Absence en Indisponibilité
  * Ajustements de comportements des emails avec ics

### Géolocalisation

* Vérifier si les adresses ont été re-géolocalisées en production
  * ```
    User.where.not(address: nil).where(city_code: nil).count
    => 123826
    ```
  * On dirait que non :)
  * Le script ne doit pas fonctionner correctement

### Statut « en salle d'attente »

* Le passage de statut “En salle d’attente” était supposé envoyer un email aux agents concernés
  * Ce n’est pas très compliqué, pas urgent non plus. (rien à faire pour le moment)

###
