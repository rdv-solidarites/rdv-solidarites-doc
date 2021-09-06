# Flux de production

Cas nominal : 

* Développement sur une branche spécifique, avec déploiement sur un environnement spécifique \(review app\)
* Quand c'est ok, merge sur la branche « recette », déployé sur l'environnement « recette » \(pour les référentes\) à l'adresse https://recette.rdv-solidarites.fr
* Le mardi présentation des nouveautés, sur l'environnement de recette
* le jeudi, sauf problème, on merge la banche de recette sur la branche de production. On merge que ce qui aura été montré le mardi. Nous allons utiliser un tag, le lundi soir ou mardi matin, avec la date pour signaler un point de livraison.

Cas exceptionnel \(livraison rapide\) :

* Développement sur une branche spécifique, avec déploiement sur un environnement spécifique \(review app\)
* Quand c'est ok, merge sur la branche « production » directement, déployé sur l'environnement « production »
* On rebase recette sur production pour mettre à jour la branche recette \(attention à préserver les commits de merge\)

Les environnements de démo et de production son identique. La démo est une plateforme servant à découvrir le service ou à faire de la formation ou tester des configurations et scénario d'usage particulier.

La branche par défaut est « recette ».

