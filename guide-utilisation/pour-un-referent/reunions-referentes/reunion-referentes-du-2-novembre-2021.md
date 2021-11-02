---
description: >-
  Démo, RDV en binôme, RDV en séquence, organisation réunion, Agenda Accueil,
  Métier agents, Recherche de créneaux
---

# Réunion référentes du 2 novembre 2021

### Démo

* [Retourner les résultats de recherche par nom exacts avant les résultats approchés #1836](https://github.com/betagouv/rdv-solidarites.fr/issues/1836)
* [Mettre à jour la date de fin au moment de la mise à jour d'un RDV en file d'attente #1826](https://github.com/betagouv/rdv-solidarites.fr/issues/1826)

Deux corrections de bug. Celle qui évoque la date de fin au moment de la mise à jour d'un RDV via la file d'attente est lié au problème de contenu d'agenda qui ne s'affichait pas pour certains agents. Ça ne devrait plus arriver.

Pourquoi le mécanisme de fil d'attente n'est pas beaucoup utilisé ? Deux réponses :

* l'ouverture aux usagers est réduites dans encore beaucoup de département, et c'est une fonctionnalité coté usager ;
* il y a peu d'attente dans certains départements, dans le cas de rendez-vous à une ou deux semaines, il y a peu de change que le mécanisme se déclenche.

### Pouvoir créer des RDV effectués en binôme d’agents de services différents

Ce [ticket](https://github.com/betagouv/rdv-solidarites.fr/issues/1708) est trop gros. Il décrit bien le problème et oriente la solution vers ce que nous avons déjà évoqué : le décloisonnement.

Pour rappel, le thème « décloisonnement » ne signifie pas enlever les mûrs de séparation entre les services, mais les rendre plus flexible.

L'idée est bien de permettre à des agents de services différents de réaliser des rendez-vous ensemble pour un motif donné (et seulement sur ceux-là). **C'est le décloisonnement de motif**. Pour y arriver, l'agent aura besoin de trouver des créneaux disponible dans l'agenda de l'autre agent. **C'est le décloisonnement d'agenda**. Où nous avons ajouté un élément qui permet de partager un agenda avec ou sans le détail des rendez-vous.

Nous allons donc fermé ce ticket unique [#1708](https://github.com/betagouv/rdv-solidarites.fr/issues/1708). Il correspond au groupement de tous les tickets de décloisonnement :

* [Simplifier la configuration et affiner les droits d'accès des motifs #1779 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1779); Ce ticket contient le déplacement des motifs au niveau du territoire (département) ET la modification d'accès. C'est-à-dire la liste des agents que l'on peut sélectionner lorsque l'on cherche un créneau ou que l'on crée un RDV ; Aujourd'hui, c'est une liste selon le service, après ce ticket, ça sera ceux qui ont l'autorisation sur ce motif (peu importe le service). Peut être fait avant l'accès à l'agenda (#1692 et #1782) mais dans ce cas, le rendez-vous se posera en « aveugle », sans voir l'agenda de l'autre agent. Ce n'est pas bloquant je pense.
* [Accéder agenda par agenda, en lecture seul ou en écriture #1692 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1692)warning Faire ce ticket après #1782
* [Remonter la gestion des agents et leur accès au niveau du territoire #1782](https://github.com/betagouv/rdv-solidarites.fr/issues/1782)
* [Associé les usagers aux territoires plutôt qu'aux organisations #1786 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1786)Si ce ticket est réalisé avant #1692 et #1779 alors la restriction d'accès se fera en fonction du service. C'est un ticket un peu à part, et qui pourtant à un impact assez fort sur la prise de RDV : plus besoin de créer un usager pour se rendre compte « ensuite » qu'il existe déjà... Nécessite sans doute un travail sur la visibilité des champs (avant ?) [Paramétrer les champs utilisé pour qualifier un usager #1814](https://github.com/betagouv/rdv-solidarites.fr/issues/1814)

Certaines d'entre vous ont récupéré par mal de points du coup. Penser à les redistribuer selon vos priorités.

### Changement d'organisation

Principalement de contenu. Nous sommes en train de parler en interne de changer le contenu de la réunion référente.

L'idée serait d'alterner tout les 15 jours entre

* une réunion produit
* une réunion développement, gouvernance, embarquement, ...

### Affichage des RDV pour l'accueil

_Sujet abordé sur le forum _[_Agenda multi-agents par jour pour un lieu_](https://forum.rdv-solidarites.fr/t/agenda-multi-agents-par-jour-voire-par-semaine/92)__

Question de la finalité ? Ce ticket sert la finalité de l'agenda ?

Aujourd'hui, certaines personnes utilisent RDV-Solidarités en ouvrant plusieurs onglets, un agenda/agent par onglet.

Ajout d'un ticket suite à la découverte de cet usage de RDV-Solidarités pour faciliter le choix de l'onglet : [Afficher le nom de l'agent en premier dans le titre #1842](https://github.com/betagouv/rdv-solidarites.fr/issues/1842)

Afficher plusieurs agendas en même temps, c'est pratique pour :\
pour :

* trouver des créneaux communs (voir [recherche de créneaux en binôme et en séquence](reunion-referentes-du-2-novembre-2021.md#undefined))
* avoir une vision globale de la journée, de la semaine, par mois

Rappel, dans le fichier Excel qui est (était ?) utilisé dans le Calvados pour gérer les RDV, il y a un bloc par jour (créneaux horaires en ligne, professionnels en colonne regroupée par métier), 5 blocs dans un onglet, une semaine un onglet, 4 onglets (ou 5) pour un mois).

_Ajout du ticket _[_Agenda d'une journée / page d'accueil pour un lieu (organisation ?) #1843 _](https://github.com/betagouv/rdv-solidarites.fr/issues/1843)_dans le tableau des prio. Il restera à régler la question du niveau : lieu ou organisation ?_

### _Recherche de créneaux en binôme et en séquence_

Lorsque que nous recherchons un créneau, il faudrait pouvoir préciser si c'est créneau commun ou si ce sont les créneaux individuels des agents sélectionnés qui nous intéresse.

Créneau commun : dans la recherche de créneau avoir une case pour trouver des créneaux commun (simultanée)

Création d'un ticket [Recherche de créneau pour un binôme d'agent #1845](https://github.com/betagouv/rdv-solidarites.fr/issues/1845).

Il y a aussi les créneaux consécutifs. D'abord puéricultrice, puis médecin ou encore d'abord assistante sociale puis médecin. J'imagine que nous pourrions aussi envisager un motif commun à ces deux agents et donc une recherche de créneaux communs suffirait... Sauf que ça bloquerais des temps trop long pour les uns et les autres.

La recherche de créneau consécutif est plus délicate, car ça serait plutôt à envisager comme 2 RDV. Il faut alors envisager d'avoir une séquence de validation de 2 rendez-vous (en faisant peut-être en sorte de n'avoir qu'une notification).

Ajout d'un ticket à ce sujet [Recherche de créneaux consécutifs pour deux agents #1846](https://github.com/betagouv/rdv-solidarites.fr/issues/1846)

Une autre option complémentaire et surtout plus rapide à mettre en œuvre serait d'avoir une couleur différente pour chaque agent dans l'affichage des créneaux disponible.

Ajout du ticket correspondant : [Distinguer les agents dans la proposition de créneaux disponible #1848](https://github.com/betagouv/rdv-solidarites.fr/issues/1848)

L'étape d'après serait d'avoir une couleur différente par métier uniquement. Cela nécessite de mettre en place la notion de métier d'abord.

Ajout du ticket [Préciser le métier d'un agent/professionnel #1849 ](https://github.com/betagouv/rdv-solidarites.fr/issues/1849)dans le tableau de priorisation.
