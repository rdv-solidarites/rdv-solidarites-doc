# Atelier RDV Collectif du 29 octobre 2021

Rappel de la discussion précédente : \[Réunion référentes du 12 octobre 2021]\(https://doc.rdv-solidarites.fr/guide-utilisation/pour-un-referent/reunions-referentes/reunion-referentes-du-12-octobre-2021#rendez-vous-collectif)

À notre que dans les Hautes-Seine, des ateliers collectifs sont mis en place via le CRM (sans prise de rendez-vous).

### Création d'un RDV collectif

Dans les discussions précédentes, nous avions conclu que le RDV Collectif serait sans doute à introduire en tant que « Type » de motif.

Cela nous permet d'avoir des éléments de configuration spécifique comme la capacité maximale.

**À noter que le nom à mettre dans les notifications ne serait pas celui du type de rendez-vous, mais plutôt le motif**. Actuellement, dans les courriels, nous envoyons le nom du motif et son type. Dans le SMS, nous n'envoyons que le type. C'est sans doute à revoir. Peut-être que le nom à afficher dans le SMS pourrait être une configuration du motif ?

Nous évoquons rapidement le sujet des droits d'accès. Les deux niveaux d'administration ne sont pas assez fin pour pouvoir ouvrir la configuration de certains éléments à certains agents.

Il serait bien de pouvoir gérer la capacité max sur la plage d'ouverture. Certaines fois, un atelier collectif se déroulant dans une certaine salle, n'accueillera pas le même nombre de personnes que dans une autre.

Est-ce que la jauge est à mettre sur la plage d'ouverture ? Les instructions seraient également à personnalisé sur la plage d'ouverture.

**Pouvoir personnaliser le paramétrage d'un motif dans une plage d'ouverture ?** Pose le problème du nombre de motifs sur une plage d'ouverture.

La plage d'ouverture pourrait :

* devenir un RDV collectif
* Si la case est cochée, on ne peut sélectionner qu'un type de motif : RDV collectif et un seul motif.
* S'afficherais, en plus des champs habituels de la plage d'ouverture, la capacité max
* (option) Il serait chouette de pouvoir ici associer la plage d'ouverture à plusieurs agents ! (**Ticket possible à l'**extérieur** des RDV-Collectifs**)
* modifier la durée ou bien se dire qu'il n'y a pas de durée dans un motif de ce type parce que c'est celle de la plage d'ouverture qui va compter
* pouvoir surcharger les instructions avant et après dans la plage d'ouverture
* le motif permet d'ouvrir à la réservation en ligne ou pas. Nous pourrions personnaliser cette information d'ouverture en ligne sur la plage d'ouverture (**Ticket possible à l'**extérieur** des RDV-Collectifs**)

_Note technique :_ pour le calcule de créneau, on pourrait considérer la `default_duration_in_min` du motif comme étant la durée de la plage d'ouverture dans le cas de motifs de type « collectif »

### L'usager participe à un RDV collectif

* Afficher les motifs pour lesquels il y a un créneau disponible (**Ticket possible à l'extérieur des RDV-Collectifs**)
* Une fois le créneau pris pour un rdv usager, il doit rester disponible pour les autres, dans la mesure de la capacité max (À prendre en compte au moment du calcul de créneau)

L'idée serait d'avoir un RDV avec plusieurs participantes (user) et plusieurs agents (pour le moment du même service et de la même orga). Difficulté : les notifications. Aujourd'hui lorsque l'on ajoute un usager à un RDV, il n'est pas notifié du RDV. Il faut notifier uniquement le nouvel usager.

Quid des rappels ? Un rappel à chaque usager ayant un moyen de contact. Les rappels d'un RDV collectif doivent fonctionner de la même manière qu'un autre RDV.

_En cherchant où sont les impacts de ce genre de changement, nous parlons rapidement des statistiques et du fichier d'export._

Le fichier d'export du fichier « stats » pourrait avoir deux versions :\
versions :

* accueil il faut une ligne par RDV
* stat une ligne par Usager ? (**Ticket possible à l'extérieur des RDV-Collectifs**) Cela permettrait d'avoir plus facilement des informations sur les usagers d'un RDV collectif.

### Agent consulte le RDV collectif

Il faut une fiche RDV spécifique pour les collectifs :

* afficher la capacité max,
* limite les informations usager (pas de place, ni d'intérêt pour l'historique de RDV)
* retirer un seul usager

**STATUS ?** Facile quand c'est annulé l'initiative du département Comment faire quand c'est l'usager (en ligne ou pas) ?

Comment un usager peut signaler qu'il ne vient pas ?

Un RDV pour tous les usagers VS un rdv par usager

Un seul RDV pour avec tous les usagers

* (-) nécessite de revoir la fiche rdv
* (-) question des status individuel (tel usager n'est pas venu, ...)
* (+) facilite annulation en masse
* (+) affiche dans les agendas
* (+) fiche spécifique qui facilite l'ajout d'un usager au RDV
* (+) fiche spécifique qui facilite le nombre de participantes

Un RDV par usager

* (-) annulation en masse compliquée (Sauf si annulation par plage d'ouverture ?)
* (-) affiche dans les agendas
* (+) fiche rdv inchangée
* (+) status de RDV individualisé
* (-) pas de visibilité sur le nombre de participantes attendu

Dans le cadre des réunions d'info collective pour les nouveaux entrants du BRSA, le status RDV individuel est très important. Il y a une forme de suivi de ces RDV. _-Pourquoi ce n'est pas fait dans une application métier ?-_

Notifications multiples des usagers lié à une plage d'ouverture qui est annulé ou sous une absence... Il manque dans cette phrase des niveaux d'indirection. Ce sont les usagers qui ont un RDV lié à une plage d'ouverture qui sont à notifier. Deux problèmes aujourd'hui : nous ne lions pas les RDV au PO. Nous pouvons donc ne faire qu'une déduction. **Faut-il ajouter un lien entre une plage d'ouverture et un RDV ?**

### Conclusion de l'atelier

Notre point de réflexion coince un peu sur le statut de RDV. En plus des petits points à résoudre, celui-ci est un plus gros morceau.

Faut-il le déplacer à la relation RDV-Usager ? Faut-il ajouter un sous statut sur la relation RDV-Usager ?

_Ce point est valable pour les rendez-vous _actuels_, lorsqu'il y a plusieurs bénéficiaires sur un RDV_

Peut-être que le mieux c'est d'ajouter une notion : le status de participation d'un usager à un RDV

Prévoir un autre atelier.
