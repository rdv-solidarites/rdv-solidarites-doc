# Réunion référentes du 21 septembre 2021

### Démo en recette

_Aucune nouveauté sur l'environnement de recette_

### Performances

Avant il y avait quelques lenteurs en début de matinée et d'après-midi. Maintenant, ça commence à être toute la journée.

Pour pallier problème à court terme, l'équipe a activé un outil automatique d'analyse du temps de réponse. Si c'est trop long, il démarrera automatiquement un autre serveur pour pouvoir répondre aux autres demandes...

Ça ne résout pas le problème de fonds que nous allons traiter au fur et à mesure. Le maintient des performances correctes est un travail continue, d'autant que le nombre d'utilisateurs de RDV-Solidarités va grandissant.

### Invitation agent non reçue

> Environ 10% des invitations agent sont perdu 40% se perdent dans les spams

Dans le 62 il y a un gros problème autour des invitations.

Pas de problème pour les autres départements...

Certains départements utilisant des outils anti-spam nécessitant qu'une personne prouve qu'elle est bien humaine, il y a peut-être un souci avec l'adresse de réponse à ce mail d'invitation. Quelle adresse est utilisée en `reply-to` dans les emails d'invitation. Est-ce que c'est l'agent qui invite ?

L'équipe pourrait remettre contact@rdv-solidarites.fr en expéditeur afin de limiter la classification en pourriel. Ça fonctionnait mieux avant.

Nous pourrions aussi pouvoir créer un compte agent même si l'agent est absent, afin de pouvoir lui poser des rendez-vous.

Il y a également le ticket [https://github.com/betagouv/rdv-solidarites.fr/issues/1721](https://github.com/betagouv/rdv-solidarites.fr/issues/1721) qui propose d'affiche le lien d'invitation. Mais ça ne règle pas le problème des mails qui partent de RDV-Solidarités vers les agents.

Sinon, nous pourrions avoir un vrai mécanisme de création de compte utilisable sans la validation. Cas assez peu fréquent. Il n'y a pas d'intérêt à travailler là-dessus.

### Suppression d'agent

La suppression de l'agent \(de l'organisation ou plus général\) ne supprime pas les rendez-vous des fiches usagers

L'annulation d'un rendez-vous par un usager passe par le compte de l'usager. Il doit l'avoir validé \(création d'un mot de passe\).

La clef de reconnaissance est le mail. C'est le seul moyen de lier le compte créé par l'agent et le compte usager.

### Les week-ends

Dans RDV-Solidarités, nous pouvons créer des plages d'ouverture sur les samedis et les dimanches, mais l'agenda n'affiche pas les samedis et les dimanches.

Ça manque de cohérence.

Nous pourrions :

* Créer une option sur l'affichage du samedi / dimanche
* afficher le samedi / dimanche s'il y a des rdv ou des plages d'ouvertures sur le samedi et dimanche ?
* **\(Retenue\) bloquer le samedi et dimanche en plage d'ouverture**
* Ne rien faire peut-être ?

C'est l'option la plus simple qui conviens pour le moment.

[https://github.com/betagouv/rdv-solidarites.fr/issues/1736](https://github.com/betagouv/rdv-solidarites.fr/issues/1736)

### Comité de Pilotage

C'est jeudi !

Les diapositives des départements, très riche en informations, sont placés en annexe.

Il y aura un temps de paroles dédié pour les départements qui souhaite parler de RDV-Solidarités dans le département.

Nous allons envoyer un mail avec un lien vers le doc à compléter par les départements qui n'ont pas encore pris le temps de le faire

### Décloisonner les services ou le changement de gestion des droits d'accès des agents

Plusieurs références à ce sujet.

* [Réduction de la liste des agents utilisant un agenda](https://forum.rdv-solidarites.fr/t/liste-des-agents-concernes-par-le-planning/252)
* [Les agents sont polyvalents. Un agent peut être en PMI et service social](https://forum.rdv-solidarites.fr/t/avoir-des-agents-multi-services/72)
* [Pouvoir affecter un agent à plusieurs services](https://forum.rdv-solidarites.fr/t/agents-multi-services-nouvelle-proposition-pouvoir-affecter-un-agent-a-plusieurs-services/219)
* [Supprimer l'appartenance d'un agent à un service](https://forum.rdv-solidarites.fr/t/agents-multi-services-piste-supprimer-lappartenance-dun-agent-a-un-service/167)
* [centralisée par plateforme téléphonique](https://forum.rdv-solidarites.fr/t/prise-de-rdv-centralisee-par-plateforme-telephonique/181) Envisager d'avoir accès aux agendas qui sont « sur d'autres » organisations ?
* [Permettre aux agents non-admin d'accéder aux agendas du secrétariat](https://forum.rdv-solidarites.fr/t/permettre-aux-agents-non-admin-dacceder-au-secretariat/76)
* [Agenda Multi Organisation](https://forum.rdv-solidarites.fr/t/agent-agenda-multi-organisation/74) Avoir un seul agenda par agent

Deux dimensions \(deux tickets ?\) :

* un agent pourrait voir \(détail ou pas\) l'agenda d'un autre agent \(peu importe le service\)
* un agent pourrait poser un rendez-vous pour un motif d'un autre service

Précision sur le « voir » : c'est visualisé un rendez-vous dans un agenda \(et sa fiche\) sans le détail usager / motifs. Le lieu peut être affiché si c'est un motif « sur place ».

Comment poser un rendez-vous pour une assistante sociale et une puéricultrice \(par exemple\) ? Décloisonné un motif ?

Aujourd'hui, pour pouvoir faire ce type de rendez-vous en binôme, les ~~agents~~ professionnels procède comme suit :

* l'une pose un rdv de son côté
* l'autre pose une absence

_Quid de l'envoie de SMS quand c'est un rendez-vous dans deux agendas, est-ce que c'est doublé ?_

Une option serait de configurer les motifs au niveau du territoire pour pouvoir :

* l'ouvrir sur une orga ou pas
* donner l'accès à plusieurs services

_Dans cette manœuvre, que mettre dans les SMS/mail \(qui affiche le service\) ?_

