# Atelier RGPD du 24 février 2022

### Ordre du jour

Afin de créer les demandes de modification adéquate, nous proposons de faire un atelier pour aborder les points suivant :

* La durée de conservation des données indiquée sur le site, mais avec des infos incohérentes et non appliquée réellement (sauf erreur de ma part)
* les exports de documents nominatifs
* les zones de commentaires
* le contenu des SMS et mail
* les mails des usagers reçus par les développeurs

Ces tickets seront ensuite présentés sous forme d'un compte rendu d'atelier à une réunion référente ultérieur. Ainsi, si vous ne pouvez pas être disponible aux dates proposées, nous pourront malgré tout discuter de vos attentes sur ces points-là.

Le contexte de cet ordre du jour et lié à une demande de la Somme, qui fait suite à la rédaction de la fiche du logiciel dans le cadre du RGPD

### Mails des usagers reçus par l'équipe

aujourd'hui : Les mails de notifications sont envoyés avec une adresse de réponse contact@rdv-solidarites.fr

Envisagé : Avoir une adresse email intermédiaire (type rdv4545667@rdv-solidarites.fr) pour les réponses aux notifications. Les mails envoyés à cette adresse seraient transféré aux agents liés à ce RDV.

Autre option, mettre les adresses emails des agents. Difficulté de gestion. Pour la protection des agents.

Suggérer une configuration pour passer d'une option à l'autre. Pas nécessairement.

**Invalider l'adresse une fois le RDV passé ? À mettre en place pour limiter la réutilisation du mail.**

Vérifier la complexité de mise en œuvre du masquage des adresses pour valider ou non la solution. Il faut peut-être reposer la question du risque lié à l'affichage des adresses d'agents. Nous pourrions probablement commencer par mettre en place un système de réponse qui expose l'email professionnel et mettre en place un système plus complexe si les agents sur le terrain se plaigne de ce système.

Autre point évoqué : ajouter un texte explicatif autour de l'élément de contact à l'équipe. Afin de limiter les emails à destination de professionnels du médico-social reçu par l'équipe technique

### Durée de conservation des données

> La durée de conservation des données indiquée sur le site mais avec des infos incohérentes et non appliquée réellement (sauf erreur de ma part)

Pourquoi une différence entre la fiche usager avec une durée de 3 ans et le compte usager avec une durée de 2 ans ?

Nous évoquons également la notion d'inactivité liée au compte usager, qu'est-ce que ça signifie ?

Nous avons évoqué par ailleurs le manque d'information sur le niveau d'inactivité sur un RDV.

Nous pourrions considérer que la fiche usager est active s'il y a eu un RDV dans les 2 ans.

Prévenir les usagers et les agents quand une fiche sera supprimer.

Compte agent ? À la charge de la collectivité. Fournir une liste des comptes inactifs. Afficher un label à côté d'un agent non connecté depuis 1 an.

Fiche active, on fait quoi des RDV de plus de 2 ans ? Fiche inactive, suppression de la fiche ? On fait quoi des RDV ?

**L'inactivité d'un usager est associé au dernier RDV. S'il date de plus de deux ans, on supprime**

Que faire d'un RDV passé ?

**Supprimer un RDV au bout de 2 ans**

Ajouter la durée de conservation des RDV dans [la page des politiques de confidentialité](https://doc.rdv-solidarites.fr/informations-generales/informations-generales-et-legales-1/politique-de-confidentialite)

Ajouter une mention sur la durée de conservation des données de RDV (2 ans).

### Zones de commentaires

Zone de remarque de la fiche usager, zone de contexte dans le RDV et champs sociaux de la fiche usager.

Mettre en place des champs personnalisés sur les fiches usagers pour que chaque département puisse faire à sa guise. Ne pas mettre de zone de saisie libre (remarque). Laisser uniquement un champ court libre. Avoir également au maximum des champs personnalisé sous forme de liste déroulante.

Faut-il faire apparaitre la liste des champs personnalisés dans la convention ? _À voir._

Quid du champ contexte dans les RDV ? Ce champ pourrait faire partie des champs optionnels. Cela signifie l'ajout de champs personnalisé dans les RDV en plus de ceux de la fiche usager.

Faciliter un lien vers l'outil métier ? C'est une option intéressante pour inciter les professionnels à ne pas utiliser RDV-Solidarités pour faire le suivi des usagers.

### Exports de documents nominatifs

Avoir des habilitations pour limiter l'usage de l'export. C'est en cours.

L'export à plusieurs usages aujourd'hui :

* pour l'accueil
* pour se rassurer (si jamais il y des pépins informatiques liés au réseau ou au logiciel)
* pour les statistiques
* pour palier au manque de connexion de certains lieux de RDV (domicile usager, site partenaire)

Ajouter un message d'avertissement sur les bonnes pratiques de sécurité et de respect de la vie privée.

Avoir des exports statistiques anonymes.

Nous évoquons par ailleurs [le guide du secret statistique de l'INSEE](https://www.insee.fr/fr/information/1300624). RDV-Solidarités n'est pas concernée en tant que produit.

Avoir une page spécifique pour l'accueil, afin de contrôler les informations affiché et limiter l'usage d'un export de donnée. Envisager un accès hors ligne sur cette page d'accueil ?

Certaines personnes ont besoin d'avoir une version papier des informations usagers lors des RDV à domicile ou dans des lieux sans connexion.

Export de donnée brut ? À voir si chaque département à la capacité d'intégrer ces données brutes pour un traitement statistique.

Retirer le champ contexte de l'export, le numéro de tel également.

Nous avons aussi parlé du chiffrement de disque dur. [Bitlocker](https://fr.wikipedia.org/wiki/BitLocker\_Drive\_Encryption) : rendre le disque dur inaccessible sans un code spécifique. Disque dur chiffré.

### Les points que nous n'avons pas abordés

Rendez-vous le lundi 7 mars de 10 h à 12 h pour aborder ces derniers points.

#### Référence à "privacy"

_Sandra recherchera la référence_

#### Contenu des SMS et mail

#### Mot de passe

> Pourra t-on ajouter le sujet du mot de passe de connexion à la prochaine réunion ? pas de nombre de caractères, ni de changements réguliers..
