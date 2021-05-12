# Outils d'analyse

* Le code source [https://github.com/betagouv/rdv-solidarites.fr/](https://github.com/betagouv/rdv-solidarites.fr/)
* déployé sur Scalingo [https://scalingo.com/fr](https://scalingo.com/fr) dont voici la page de status [https://scalingostatus.com/](https://scalingostatus.com/)
* Updown pour la production [https://updown.io/feom](https://updown.io/feom) et pour la démo [https://updown.io/x4tw](https://updown.io/x4tw)
* Analyse de performance sur Skylight [https://oss.skylight.io/app/applications/RgR7i58P67xN/recent/6h/endpoints](https://oss.skylight.io/app/applications/RgR7i58P67xN/recent/6h/endpoints)
* Les remontées d'erreurs du serveur sur Sentry [https://sentry.io/organizations/rdv-solidarites/issues/?project=1811205](https://sentry.io/organizations/rdv-solidarites/issues/?project=1811205)
* Le tableau de bord d'analyse de sécurité, de conformité partiel au RGAA, et autres outils compilés par les équipes Beta.Gouv sur Dashlord [https://dashlord.incubateur.net/\#/url/https%3A%2F%2Fwww.rdv-solidarites.fr](https://dashlord.incubateur.net/#/url/https%3A%2F%2Fwww.rdv-solidarites.fr)
* L'analyse de trafic sur Matomo [https://stats.data.gouv.fr/index.php?module=CoreHome&action=index&idSite=123&period=range&date=previous30&updated=1\#?idSite=123&period=range&date=previous30&category=Dashboard\_Dashboard&subcategory=1](https://stats.data.gouv.fr/index.php?module=CoreHome&action=index&idSite=123&period=range&date=previous30&updated=1#?idSite=123&period=range&date=previous30&category=Dashboard_Dashboard&subcategory=1)

Nous utilisons aussi un linter spécifique à Ruby dans notre CI. Rubocop avec les extensions Rspec et Rails. Voir les fichiers de configuration [https://github.com/betagouv/rdv-solidarites.fr/blob/master/.rubocop.yml](https://github.com/betagouv/rdv-solidarites.fr/blob/master/.rubocop.yml) et, temporairement, [https://github.com/betagouv/rdv-solidarites.fr/blob/master/.rubocop\_todo.yml](https://github.com/betagouv/rdv-solidarites.fr/blob/master/.rubocop_todo.yml) sur lequel nous travaillons

L'intégration continue se fait via Github Action. Voir [https://github.com/betagouv/rdv-solidarites.fr/blob/master/.github/workflows/ci.yml](https://github.com/betagouv/rdv-solidarites.fr/blob/master/.github/workflows/ci.yml) pour la configuration, et [https://github.com/betagouv/rdv-solidarites.fr/actions/workflows/ci.yml](https://github.com/betagouv/rdv-solidarites.fr/actions/workflows/ci.yml) pour le journal des déclenchements.





