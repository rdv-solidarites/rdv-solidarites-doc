# Configuration Territoire

### Webhook

_(Ce titre est sans doute à modifier pour le rendre plus compréhensible par les agents concernés)_

L'entrée de menu correspondante affiche une liste des webhooks actuellement configurées.

![Ici aucun webhoook n'est configuré pour le moment](../../.gitbook/assets/screenshot\_2021-09-17-administration-75-paris-rdv-solidarites.png)

Dans l'ajout d'un webhook, il faut

* choisir l'organisation liée
* l'URL (qui doit être en HTTPS)
* le secret (sorte de mot de passe que s'échangeront les systèmes pour s'assurer qu'ils se connaissent)

![example de remplissage du formulaire de création/modification](../../.gitbook/assets/screenshot\_2021-09-17-ajouter-un-webhook-rdv-solidarites.png)

### SMS

_Si vous ne voyez pas cette entrée de menu dans l'interface de_ configuration \_territoriale, c'est que l'équipe n'a pas activé la personnalisation de configuration d'\_envoi _de SMS pour votre territoire. Vous pouvez la contacter pour que ce soit accessible_

![](../../.gitbook/assets/screenshot\_2021-09-20-sectorisation-75-paris-rdv-solidarites.png)

S'affiche ensuite le fournisseur actuel ainsi que les éléments d'identification. En cliquant sur le bouton modifié, un formulaire propose la liste des fournisseurs actuellement supportés par le service et un champ permettant de saisir les éléments d'identification.

_Nous avons remarqué que la plupart des fournisseurs_ demandent _un seul élément d'identification. Soit une clef, soit un identifiant et un mot de passe qui sont envoyé cote à cote. Nous avons donc opté pour l'utilisation d'un seul champ._

![](../../.gitbook/assets/screenshot\_2021-09-20-modifier-lorganisation-rdv-solidarites.png)

Attention, comme sur l'exemple ici en capture d'écran, il faut parfois (selon votre fournisseur) saisir un identifiant ou un utilisateur et le mot de passe, les deux séparés par `:` dans la même zone.
