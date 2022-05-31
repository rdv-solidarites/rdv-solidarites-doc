# Incident du 30 mai 2022



## Post mortem du 30 mai 2022

### Chronologie

* 10:19 : Au matin du lundi 30 mai 2022, la PR [#2506](https://github.com/betagouv/rdv-solidarites.fr/pull/2506) a été déployée. Ce code contenait une régression qui empêchait la modification du statut d'un RDV.
* 10:48 : Premier mail d'une référente sur contact@rdv-solidarites.fr
* 11:10 : Message de Nicolas sur le chat à propos de ce mail
* 11:17 : Début d'essai de revert des changements
* 11:50 : Revert en ligne

### Problèmes

* Besoin de changer les paramètres du repo github pour merger une PR non approuvée et sur laquelle les tests de feature étaient rouges
* Timeout mystérieux qui fait que les tests de features ne passent pas sur la CI, alors qu'elles passent en local
* Environ 9mn de build
* Pas de processus de rollback/revert très clair
* Pas de test qui soit passé au rouge lors du développement de la PR qui a introduit le bug

### Actions possibles

* Ajouter une spec d'intégration pour les modifications de status de RDV
* Voir si c'est possible de paralléliser en plusieurs job le job de features specs sur la CI, afin d'avoir un build plus rapide
* Documenter quoi faire quand il y a un gros bug en prod (comment faire le revert, comment communiquer)
* avoir une adresse mail pratique pour s'adresser aux référentes, sans avoir le temps de latence des framalistes
* Essayer de débugger la CI, et faire plus attention à ce qu'elle soit fonctionnelle
* Ajouter une entrée de log de prise de décision qui indique que la vigie doit surveiller la boite contact@rdv-solidarites.fr
