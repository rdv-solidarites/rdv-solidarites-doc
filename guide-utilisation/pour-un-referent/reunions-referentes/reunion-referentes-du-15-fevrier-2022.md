# Réunion référentes du 15 février 2022

### Les nouveautés

* [Afficher des créneaux à venir uniquement #2013](https://github.com/betagouv/rdv-solidarites.fr/issues/2013)
* [Utilise un identifiant cours pour les invitations usager](https://github.com/betagouv/rdv-solidarites.fr/pull/2121)
* [Corrige l'affichage d'information sur la désactivation des notifications #2135](https://github.com/betagouv/rdv-solidarites.fr/issues/2135)
* [Corrige l'affichage des agents pouvant être référent #1998](https://github.com/betagouv/rdv-solidarites.fr/issues/1998)
* [Améliorer les performances de l’affichage des usagers #2109](https://github.com/betagouv/rdv-solidarites.fr/issues/2109)
* [Paginer les personnes pouvant être référentes #2057](https://github.com/betagouv/rdv-solidarites.fr/issues/2057)
* [Ne pas afficher les membres des équipes recherchées dans le champ agents #2026](https://github.com/betagouv/rdv-solidarites.fr/issues/2026)
* [Affiche le lieu qui avait été sélectionné quand on revient au filtre de la recherche de créneaux agent #2054](https://github.com/betagouv/rdv-solidarites.fr/issues/2054)
* [Afficher les créneaux disponibles hors période d'indisponibilité #2055](https://github.com/betagouv/rdv-solidarites.fr/issues/2055)
* [Prioriser les résultats exacts dans la recherche full-text #2047](https://github.com/betagouv/rdv-solidarites.fr/issues/2047)
* [Ne pas afficher les agents en doublon dans la liste d’agents du territoire #2025](https://github.com/betagouv/rdv-solidarites.fr/issues/2025)
* [Clarifier le message de confirmation d'une annulation de RDV passée #1921](https://github.com/betagouv/rdv-solidarites.fr/issues/1921)

### À venir

* [Nouvelle interface configuration #2151](https://github.com/betagouv/rdv-solidarites.fr/pull/2151)
* [Invitation et accès organisation depuis le module de configuration #2032](https://github.com/betagouv/rdv-solidarites.fr/issues/2032)
* [Considérer les délais min et max des motifs #2005](https://github.com/betagouv/rdv-solidarites.fr/issues/2005)
* [Tiers lieux et visioconférence pour un RDV #1639](https://github.com/betagouv/rdv-solidarites.fr/issues/1639)
* [Faciliter la recherche d'une plage d'ouverture en particulier dans la liste des plages d'ouvertures #1918](https://github.com/betagouv/rdv-solidarites.fr/issues/1918)
* [Rediriger vers la connexion (et non vers l’inscription) après une erreur de connexion #2029](https://github.com/betagouv/rdv-solidarites.fr/issues/2029)
* [Permettre aux agents de réinitialiser leur mot de passe depuis la page de connexion d’usagers #1614](https://github.com/betagouv/rdv-solidarites.fr/issues/1614)
* [Améliorer la performance des envois de webhooks #2154](https://github.com/betagouv/rdv-solidarites.fr/issues/2154)

### Pause entre les RDV

Nous nous sommes demandé si nous avions besoin de créer, lors du calcul de créneau, des espaces entre les créneaux pour que les professionnels aient des temps de pose.

Les départements utilisent la durée du rendez-vous pour inclure des temps de pause. **Aucun besoin de créer une complexité supplémentaire**.

### Notifications

Aujourd'hui, nos messages SMS sont longs, ils dépassent les 160 caractères. Cela nous fait donc facturer 2 SMS par notification.

Nous avons discuté du contenu des SMS. Nous allons effectuer un premier travail sur la longueur de l'adresse. [Afficher des adresses moins longues #2159](https://github.com/betagouv/rdv-solidarites.fr/issues/2159)

Nous allons également proposer un changement pour les informations complémentaires (la fin du message), en proposant un lien spécifique vers une page de détail du RDV.

[Ajouter un lien vers une page de détail de RDV aux notifications #2161](https://github.com/betagouv/rdv-solidarites.fr/issues/2161)

### Monitoring

Nous sommes en train de mettre en place des outils de suivi des notifications (email et SMS) afin de faciliter la remontée d'information en cas de problème. Cette première version minimaliste sera sans doute accessible à l'équipe seulement.

Nous devrions pouvoir décliner par la suite des outils accessible à certaines personnes du département.

### Détail de RDV dans les agendas

Nous aimerions avoir votre avis sur le fait d'afficher ou non le détail des RDV dans vos agendas.

Il semble que nous ayons envisagé deux pistes, et nous aimerions vérifier si elles sont toujours nécessaires.

* Soit afficher le détail des RDV dans le fichier ICS pour que toutes les infos soient visibles dans les agendas outlook, zimbra et autres.
* Soit avoir uniquement un lien dans la description du « créneau de RDV » de l'agenda zimbra, outlok ou autres, pointant vers la page dans RDV-Solidarités

Merci de votre participation&#x20;

[https://framadate.org/GWBJ7SiIrAHVm6lK](https://framadate.org/GWBJ7SiIrAHVm6lK)

