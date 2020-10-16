# Hébergement & sécurité

 Nous hébergeons l'application \(donnée et programmes\) chez Scalingo. Scalingo est une entreprise française \(basé à Strasbourg\) [https://scalingo.com/fr](https://scalingo.com/fr)

Eux même utilisent les data center de Outscale. Outscale est un fournisseur de Data Center et solution d'informatique en nuage \([https://fr.outscale.com/](https://fr.outscale.com/)\) français.

{% embed url="https://scalingo.com/fr/press-releases/20200623-secnumcloud" %}

Outscale est qualifié SecNumCloud par l'ANSSI \([https://www.ssi.gouv.fr/uploads/liste-produits-et-services-qualifies.pdf](https://www.ssi.gouv.fr/uploads/liste-produits-et-services-qualifies.pdf) et [https://www.ssi.gouv.fr/uploads/2019\_4577\_np.pdf](https://www.ssi.gouv.fr/uploads/2019_4577_np.pdf)\)

Outscale est par ailleurs certifié HDS \(Hébergeur de données de santé\) [https://fr.outscale.com/certificates/hds-hebergeur-de-donnees-de-sante/](https://fr.outscale.com/certificates/hds-hebergeur-de-donnees-de-sante/)

Scalingo est en train de passer la certification \(prévu pour avant la fin de l'année\).

Notre équipe fera les démarche une fois Scalingo certifié.



### Déploiement

Les environnements de production et de pré-production \(démo\) sont hébergés sur [Scalingo](https://scalingo.com/)

La CI est configurée pour déployer automatiquement la branche `master` vers un un environnement de [démo](https://demo.rdv-solidarites.fr) et **vers la production**.

> _Note : Éviter de merger des PR simultanément_
>
> Il faut éviter de merger sur master des PRs trop rapprochées \(quelques minutes\) pour éviter que ça ne s'emmêle et déploie la mauvaise
>
> ou alors, il faut merger la première PR -&gt; annuler le build CircleCI tout de suite -&gt; puis merger la deuxième PR

#### 

#### Déploiement manuel \(vers la demo ou la production\)

`scalingo integration-link-manual-deploy -a demo-rdv-solidarites master`

Pré-requis :

* être ajouté en tant que collaborateur sur l'application Scalingo, demandez à un membre de l'équipe
* Installer le [CLI Scalingo](https://doc.scalingo.com/platform/cli/start)
* Connectez votre machine avec `scalingo login --api-token SOME_TOKEN` que vous pourrez créer ici : [https://my.scalingo.com/profile](https://my.scalingo.com/profile)



\_\_





