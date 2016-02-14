##Comment créer mon premier Ghost Blog <img src="emoji/ghost" width="18"/> !

![Comment créer votre Ghost Blog](https://ksr-ugc.imgix.net/projects/487539/photo-original.jpg?v=1397813310&w=1536&h=1152&fit=crop&auto=format&q=92&s=53679cf8026115204cd9315b99be9fe8)

je ne sais pas si vous avez déjà entendu parler de la nouvelle plateforme de blogging 100% destiné au blogging lancé par [John O'Nolan](https://twitter.com/JohnONolan)

[Ghost](https://ghost.org/) est open source ecrit en Javascript et distribué sous licence [MIT](https://fr.wikipedia.org/wiki/Licence_MIT), Le 29 avril 2013, O'Nolan publie une vidéo du prototype lors d'une campagne de financement participatif sur [Kickstarter](https://www.kickstarter.com/projects/johnonolan/ghost-just-a-blogging-platform) avec un objectif de 25 000 £ pour financer le développement du projet

Techniquement, il est codé en [Node.js](https://nodejs.org/en/) et peut utiliser plusieurs moteurs de base de données SQL : MySQL, Postgres ou SQLLite. 

Ghost est open source disponible en telechargement sur [GitHub](https://github.com/tryghost/Ghost), de plus autour l'on trouve une communauté très active  


## # Qu'est-ce que Node.js? :

![image description](https://nodejs.org/static/images/logos/nodejs.png)

[Node.js](https://nodejs.org/en/) est une plateforme moderne pour créer des applications web rapides, évolutives et efficaces. Ces 20 dernières années, le web a évolué, en partant d'une collection d'images statiques pour aller vers une plateforme capable de supporter des applications web complexes comme Gmail et Facebook. Javascript est le langage de programmation qui a permis ce progrès.


## # Démarrage

Vous allez avoir besoin d'un hébergement qui dispose déjà ou vous permet d'installer [Node.js](https://nodejs.org/en/). C'est à dire quelque chose comme une instance ou n'importe quel autre hébergement disposant d'un accès [SSH](https://fr.wikipedia.org/wiki/Secure_Shell) et qui vous permet d'installer [Node.js](https://nodejs.org/en/). Il en existe beaucoup et ils peuvent être peu chers.

Ce qui ne fonctionnera pas pour le moment, ce sont les hébergements mutualisés dans le style cPanel, qui sont habituellement spécifiques à l'hébergement de fichiers PHP. Malgré tout, certains de ces hébergements offrent déjà Ruby, et sont donc susceptibles d'offrir Node.js dans un futur proche.

Il y a plusieurs options pour installer simplement Ghost via des installateurs:

- [Ghost(Pro) ($10/mois)](https://ghost.org/pricing/)
- [DigitalOcean ($5/mois)](https://www.digitalocean.com/pricing/)
- [Amazon - (gratuit la première année)](https://aws.amazon.com/fr/free/)
- [Windows Azure - (gratuit pour une instance F1) ](https://azure.microsoft.com/fr-fr/pricing/details/app-service/)
- [Rackspace - ($16/mois)](https://www.rackspace.com/)
- [Openshift - (gratuit pour 3 web applications) ](https://www.openshift.com/pricing/index.html)
- [Servermule - ($10/mois)](http://www.servermule.com.au/vps-hosting/)
- [Citycloud - ($20/mois)](https://www.citycloud.com/pricing/)

### Paramétrage

Pour installer [Node.js](https://nodejs.org/en/) et [Ghost](https://github.com/tryghost/Ghost) sur votre Mac, vous devez tout d'abord ouvrir un terminal. Vous pouvez en obtenir un en ouvrant la recherche rapide en tappant "Terminal".

![image description](http://i.imgur.com/GUDeIBV.png)


### Installer Node JS

- Sur http://nodejs.org cliquez sur install, un fichier '.pkg' va être téléchargé
- Une fois téléchargé, cliquez dessus pour ouvrir l'installeur, cela va installer node et npm
- Entrez votre mot de passe et cliquez sur 'installer le logiciel'
- Une fois l'installation terminée, allez sur le terminal et tappez echo **$PATH** pour verifier que (**/usr/local/bin/**) est référencé dans le path

> **Note:** Si '/usr/local/bin' n'apparaît pas dans la variable d'environnement $PATH, visitez [la page](http://docs.ghost.org/fr/installation/mac/#export-path) de résolution des problèmes pour trouver une façon de corriger ça

### Création d’un compte OpenShift

[Openshift](https://www.openshift.com/app/account/new) est une solution Cloud PaaS (Platform as a Service) produite par Red Hat. L’offre est gratuite pour trois « gears » (un gears équivaut à une application) et elle n’est pas limité à Node.js. Vous pouvez installer des environnements Java, PHP, Python, Ruby, Perl et Go.

Maintenant, on doit crée un compte OpenShift, pour cela rendez-vous sur [le site officiel](https://www.openshift.com/app/account/new) et choisissez l’offre Online. Remplissez les champs demandés, cliquez sur le lien de vérification dans l’e-mail de confirmation, puis accepter les conditions d’utilisation.

![image description](http://i.imgur.com/rBdsEM8.png)


### Création de notre premiére application
En suite on va crée notre premiere application sur OpenShift pour déployer notre Ghost blog :

![image description](http://i.imgur.com/IJppV2W.png)
![image description](https://i.imgur.com/jN3X51a.png)

Comme indiqué sur ce screenshot, on va choisir le nom de votre blog suivie de votre utilisateur, pour moi ca sera **«monblog»** et **«elmehdi»** :

![image description](http://i.imgur.com/9T4W6SI.png)

Pour ma part, je vais choisir [PostgreSQL](https://fr.wikipedia.org/wiki/PostgreSQL) comme base de donne et pour la region je vais choisir **aws-us-east-1** 
![image description](http://i.imgur.com/bOKOOlC.png)

En suite au bout de quelque minutes notre ghost blog sera pret a utuliser:

![image description](http://i.imgur.com/foZLl9e.png)

Une fois notre blog est creee, on doit allez configuer l'administration de notre blog en ajoutant (Votre Blog URL/Ghost)

**Exemple:**
```
http://monblog-elmehdi.rhcloud.com/ghost
```

![image description](http://i.imgur.com/H636KrQ.png)
![image description](http://i.imgur.com/jWwByXN.png)

Et Voila notre ghost blog est créé, maintenant on va voir comment en peut changer le theme et la personnalisation de votre nom de domaine, pour se faire il nous faut installer Git et Ruby sur notre ordinateur si ce n’est pas déja fait pour qu'on puisse installer le clients openshift.




#### Pour tester Ruby :
```
ruby -e 'puts "Welcome to Ruby"'
```

#### Pour tester Git :
```
git --version
```

#### Pour installer Node.js :
```
https://nodejs.org/en/
```

#### Pour installer Git :
```
sudo apt-get update
sudo apt-get install git rubygems
```

#### Pour installer l’outil Openshift :
```
sudo gem install rhc
sudo gem update rhc
```

Une fois installé, on va configurer l’outil avec votre compte OpenShift :

```
rhc setup -l votre@email.com
```

```
Entrer et puis mettez votre Mots de passe Openshift 
```
en suite on va creer un dossier ou on va cloner notre ghost blog sur notre ordinateur pour ajouter ou modifer notre blog

#### Crée notre cléf SSH
```
rhc ssh <nom de votre blog>
```
Exemple: 

```
rhc ssh monblog
```

```
rhc set-env NODE_ENV=production --<nom de votre blog>
```

```
rhc app restart
```
![image description](http://i.imgur.com/owISvdI.png)

#### Ajouter mon nom de domaine

Maintenant je vais ajouter mon nom de domaine personnel, pour se faire cliquez sur l’onglet Settings, remplissez le champ Domain name.

![image description](https://i.imgur.com/7wK1Z9i.png)


### Cloner notre dépôt existant
```
git clone ssh://56bf536789f5cf221900017e@monblog-elmehdi.rhcloud.com/~/git/monblog.git/
```

```
cd monblog
```
Dans cette etape, on va ajouter notre theme et en meme temps 
configurer notre fichier **config.js** pour ajouter notre variable.

on commence par localiser notre dépôt et puis ouvrir le fichier config.js dans votre editeur pour changer la variable actuel par la nouvelle qui va forcer a utuliser notre alias 

![image description](http://i.imgur.com/OuuDi0A.png)
```
http://'+process.env.OPENSHIFT_APP_DNS 
```
à
```
http://'+process.env.OPENSHIFT_APP_DNS_ALIAS
```

Maintenant on va choisir le theme pour notre blog, il exite des themes gratuits et d'autres payants, pour mon cas je vais choisir un theme gratuit, je vous laisse quelque liens pour choisir le theme de votre choix :

- [http://marketplace.ghost.org/themes/free/](http://marketplace.ghost.org/themes/free/)
- [http://www.allghostthemes.com/tag/free/](http://www.allghostthemes.com/tag/free/)
- [https://www.gavick.com/free-ghost-themes](https://www.gavick.com/free-ghost-themes)

Une fois vous avez fait votre choix, vous devez ajouter votre theme au dossier dépôt **/content/themes/**

### Ajouter une variables d’environnements

Maintenant on va ajouter notre variable pour que l'environnement pointe vers mon domaine: 
```
rhc set-env OPENSHIFT_APP_DNS_ALIAS=www.elmehdi.mobi -a monblog. 
```
### Déployer notre Ghost Blog

Une fois le projet prêt, nous pouvons le déployer et pour se faire on aura besoin des commandes suivantes:
```
git add -A
```

```
git commit -m "Ajouter notre Theme"
```

```
git push origin master
```

```
rhc app restart monapp
```

Voilà les étapes que j'ai suivie pour créer mon premier Ghost Blog et l'heberger gratuitement, J'espère que ce nouveau tuto vous a plu et n'hesiter pas a me poser vos question sur twitter.

ElMehdi [@ElMehdiMobi](https://twitter.com/ElMehdiMobi)


### Reference

- [developers.openshift.com](https://developers.openshift.com/en/getting-started-osx.html)
- [docs.ghost.org](http://docs.ghost.org/fr/)
- [www.elmehdi.mobi](http://www.elmehdi.mobi)
