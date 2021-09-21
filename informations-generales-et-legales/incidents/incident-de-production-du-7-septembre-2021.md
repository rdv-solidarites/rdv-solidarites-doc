# Incident de production du 7 septembre 2021

### Le symptôme

L’agenda n’affichait plus aucun contenu. Ni Rdv, ni plage d’ouverture, ni absence, ni jour férié\) entre 14 h 27 et 14 h 39.

Il n’est pas exclu qu’il y ait eu d’autres bugs moins évidents. Aucun retour à ce sujet, et nous n'avons rien constaté d'autres de particulier.

### Contexte

Nous avions une livraison à réaliser, une mise à jour technique. [Une nouvelle version de Ruby](https://www.ruby-lang.org/en/news/2020/12/25/ruby-3-0-0-released/), le langage de programmation utilisé par RDV-Solidarités

Vu le risque de la manœuvre, nous avions préparé un retour arrière rapide en cas de problème. Cela nous permettait d'effectuer ce retour en 5 à 6 minutes. C'est le temps utilisé par le processus de déploiement. Difficile de faire moins.

### Amélioration

Il n'y a aucun test automatisé qui vérifie qu'un agent voit correctement les données sur l'agenda. C'est une page actuellement complexe qui utilise des librairies en JavaScript.

L'écriture d'un test automatisé n'est pas simple dans ce contexte.

Nous pourrions cependant prendre le temps d'écrire ce test. L'affichage des informations dans l'agenda étant un des points principaux de RDV-Solidarités.

### Communication

À 14 h 32, quand nous avons décidé de déployer retour en arrière, ça nous aurait été utile de pouvoir faire un mail à toutes les référentes pour prévenir que l’incident était connu, et en cours de résolution :confused:

Une liste de diffusion serait à mettre en place.

