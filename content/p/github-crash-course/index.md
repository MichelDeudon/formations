---
title: Cours sur Github pour data scientists
date: 2022-01-24
---

De A à Z, tout ce que vous devez savoir

<!--more-->

J'ai toujours eu un syndrome de l'imposteur en travaillant sur Github, jusqu'à récemment. Je me souviens de la première fois que j'ai ouvert un terminal, j'avais l'impression d'être sur le point de pirater le monde 🐱‍💻 Avec le temps et la pratique, j'ai finalement compris les concepts clés derrière Github. Maintenant, je me sens plus à l'aise de travailler avec des ingénieurs et des développeurs ou d'encadrer des pairs, et c'est amusant. J'ai écrit ce tuto au moment où j'ai postulé chez Vinted pour un poste en science des données et j'ai décidé de le partager car c'est peut-être ce que vous recherchez 😊. Super, alors qu'est-ce que Github ?

{{< figure src="git/blog-git-1.jpg" caption="git/Photo de Tatiana Syrikova sur Pexels" numbered="true" >}}

Git est un système de contrôle de version, open source, distribué et Github est une plate-forme d'hébergement et de collaboration sur les projets Git. <b>Github aide les gens à collaborer à travers le monde</b> - apprendre, partager, contribuer et construire ensemble en synchronisant le travail sur différentes machines pour résoudre divers types de problèmes liés à l'intelligence artificielle, à l'apprentissage automatique ou à des applications. En d'autres termes, Github est comme un bac à sable distribué et c'est gratuit !

Que vous travailliez ou que vous postuliez pour un emploi en tant qu'analyste, data scientist ou décisionnaire, développeur, ingénieur, consultant ou manager et que vous ayez besoin d'un rappel sur Github ou que vous en ayez entendu parler et que vous devez l'utiliser pour collaborer, ce <b>guide pratique pour maîtriser Github en 7 étapes</b> est probablement pour vous. Je supposerai seulement que vous avez installé Git et un compte Github, sinon vérifiez [comment installer Git pour votre système d'exploitation](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) (Mac, Windows, Linux/Ubuntu) et [créez un compte Github](https://github.com/) 🚀

Avant de plonger dans des cas d'utilisation pratiques et des commandes Git, voici un peu de <b>terminologie</b> anglaise pour vous familiariser avec les concepts :

> `Repository`: Un dossier avec des fichiers dont nous voulons garder une trace <br>
> `Remote`: Un dossier commun que tous les membres de l'équipe utilisent pour échanger leurs modifications <br>
> `Origin`: Votre dossier local <br>
> `Index`: Une zone où Git contient les fichiers qui ont été modifiés, ajoutés ou supprimés <br>
> `Commit`: Une entrée dans l'historique de Git, représentant une modification apportée à un ensemble de fichiers à un moment donné, un instantané compressé de l'ensemble de votre dossier <br>
> `Branch`: Une version d'un dossier, un pointeur mobile léger vers un commit, qui représente l'état du dossier<br>
> `HEAD`: Le commit le plus récent sur une branche. Il représente votre répertoire de travail actuel et peut être déplacé vers différentes branches, balises ou commits lors de l'utilisation de git checkout

## Cas d'utilisation et commandes Git pratiques

### 1. Commencer

La première étape lorsque vous commencez à travailler avec Git consiste à configurer vos informations d'utilisateur (nom et e-mail). Vous pouvez le faire pour tous les dossiers locaux en tapant les commandes ci-dessous dans un terminal

```sh
git config — global user.name "votre_nom"
git config — global user.email "votre_email"
```

Facile, non ? Vous pouvez également afficher des informations d'aide sur Git en utilisant

```sh
git help
```

### 2. Démarrer une zone de travail

Maintenant que vos dossiers locaux sont configurés, vous pouvez créer un projet sur Github et le cloner (télécharger) localement avec

```sh
git clone "url"
```

Le fichier <b>.gitignore</b> est utile pour exclure les fichiers du suivi avec Git, tels que les informations d'identification, les jetons ou les données. Vous pouvez trouver des modèles sur [github.com/github/gitignore](https://github.com/github/gitignore).

### 3. Examiner l'historique et l'état du dossier de travail

À partir de votre dossier cloné, vous pouvez répertorier l'historique des versions de la branche actuelle avec

```sh
git log
```

Pour inspecter et comparer plus en détail l'évolution des fichiers de projet, utilisez

```sh
git diff
```

Cela montrera les changements par rapport au commit précédent (ce qui a été ajouté, supprimé ou modifié). Vous pouvez en outre spécifier des branches ou des commits pour modifier le résultat par défaut.

{{< figure src="git/blog-git-2.jpg" caption="git/Photo de James Wheeler sur Pexels" numbered="true" >}}

### 4. Apporter des modifications et les valider

À ce stade, vous pouvez inspecter l'historique des versions. Il est maintenant temps de contribuer au projet ! Ajoutez, supprimez ou modifiez un fichier dans votre dossier, par exemple, un script Python <i>hello-world.py</i>.

Les modifications que vous avez apportées à votre dossier local et les fichiers qui sont suivis/non suivis sur votre branche sont accessibles avec

```sh
git status
```

Pour ajouter du contenu à l'index et créer une "capture" des fichiers sur lesquels vous avez travaillé, utilisez simplement

```sh
git add [fichier1][fichier2][fichier3]
```

Ou pour ajouter tous les fichiers et modifications directement (attention cependant), utilisez

```sh
git add .
```

La dernière étape pour enregistrer les changements dans votre historique de version se fait avec

```sh
git commit -m "message descriptif"
```

Votre message doit contenir des informations spécifiques, [ce que font les changements, pas ce que vous avez fait pour le changement](https://vinted.engineering/2015/01/02/proper-git/) (par exemple, <i>"bug corrigé”</i> 🙈). Demandez-vous si d'autres personnes ou vous-même dans 6 mois comprendront de quoi il s'agit sans regarder le code ? Envisagez de diviser un grand commit en plusieurs commits si cela facilite la compréhension et n'oubliez pas que Github est un outil de collaboration et doit être utilisé comme tel.

### 5. Se balancer de branche en branche

Supposons que vous ayez un premier prototype et que vous souhaitiez développer des fonctionnalités en parallèle. C'est là que les branches entrent en jeu. Les branches sont une partie importante du travail avec Git. Tous les commits que vous faites seront faits sur la branche sur laquelle vous êtes actuellement et vous pouvez voir les différentes branches en utilisant

```sh
git branch -l
```

Vous pouvez créer une nouvelle branche localement, par exemple appelée <i>"feature/x"</i>, en utilisant

```sh
git branch feature/x
```

Et vous pouvez supprimer cette même branche en ajoutant le drapeau `-d` après `git branch`

Vous pouvez maintenant basculer vers une branche ou un commit spécifique (cela mettra à jour votre répertoire de travail local) avec la première ou la deuxième ligne de commande ci-dessous

```sh
git checkout feature/x
git checkout commit_id
```

{{< figure src="git/blog-git-3.jpg" caption="git/Photo de Leah Kelley sur Pexels" numbered="true" >}}

Chaque branche a tendance à diverger naturellement avec des caractéristiques différentes. Vous pouvez reconstituer leur historique de développement en « fusionnant » les branches, c'est-à-dire en incorporant les changements d'une branche à l'autre. Par défaut,

```sh
git merge
```

combine la branche suivi à distance dans la branche locale actuelle et

```sh
git merge origin [branch]
```

combine l'historique de la branche spécifiée dans la branche actuelle. Cela se fait généralement dans les "pull requests" (plus d'informations à ce sujet dans la section suivante).

Enfin, quelques mots sur `git rebase`. Rebase applique les commits d'une branche au-dessus du HEAD d'une autre branche (c'est aussi connu sous le nom de fast forwarding). Il doit être utilisé avec précaution car il modifie les commits eux-mêmes et peut donc devenir problématique s'il est effectué sur une branche avec de nombreux collaborateurs. Personnellement, je trouve la commande utile pour nettoyer l'historique des versions d'une branche ou pour intégrer des modifications apportées à la branche principale (`-i` signifie mode interactif)

```sh
git rebase -i master
```

### 6. Synchroniser les modifications

À ce stade, vous avez apporté quelques modifications à votre dosser local et modifié l'historique des versions de votre branche locale <i>"feature/x"</i>. Entre-temps, votre ami et collègue a également modifié l'historique des versions de la même branche distante. Que faire maintenant?

La première étape consiste à télécharger tout l'historique des branches de suivi à distance. Vous pouvez le faire avec

```sh
git fetch
```

Ensuite, vous devez réellement fusionner ces branches de suivi à distance dans vos branches locales. Vous pouvez simplement utiliser

```sh
git pull origin feature/x
```

en tant que combinaison de `git fetch` et `git merge` pour obtenir les modifications du dossier distant. Si vous avez de la chance, tout a bien fonctionné. Sinon, si `git merge` renvoie <i>"Automatic merge failed; fix conflicts and then commit the result"</i>, cela signifie que votre ami et vous avez tous les deux modifié le même code et que les conflits doivent être résolus manuellement. Dans ce cas, `git status` vous aidera à trouver quels fichiers sont modifiés sur les deux branches et git diff vous montrera où se trouvent les conflits. Ceux-ci sont marqués et délimités dans le code par `>>>>`, `====`, `<<<<` ce qui facilite la détection et la modification avec un éditeur de texte, jusqu'à ce que tous les conflits soient résolus. Lorsque vous avez terminé, votre branche de travail locale est à jour avec tous les nouveaux commits de la branche distante correspondante sur GitHub.

Enfin, vous pouvez envoyer votre commit au dossier distant et prendre une collation. Félicitations!

```sh
git push origin feature/x
```

Remarque : Dans certaines situations, par exemple, toutes les modifications ont été effectuées sur master mais devaient être effectuées sur la branche <i>"feature/x"</i>, il est pratique de <i>"cacher"</i> les modifications. dans un répertoire de travail modifié avant de les ajouter à l'historique des versions. Vous pouvez le faire et appliquer la modification sur la bonne branche en utilisant

```sh
git stash
git checkout feature/x
git stash apply
```

### 7. Taguez vos commits

Git est un système de contrôle de version et aide à garder une trace des différentes versions. Vous voudrez peut-être marquer certains d'entre eux avec un nom lisible tel que "alpha", "beta", "v0.0.1" ou "v0.0.2". La syntaxe est donnée ci-dessous. Bien que cette étape soit entièrement facultative, c'est une belle façon de célébrer les jalons et les victoires 🎉

```sh
git tag [label] [commit]
```

## Derniers mots

Vous avez terminé avec ce cours, bravo ! Vous êtes prêt à collaborer avec des personnes du monde entier. N'oubliez pas qu'il faut du temps et de la pratique pour maîtriser un outil comme Github et si vous souhaitez aller plus loin, consultez la référence ci-dessous ou demandez simplement de l'aide autour de vous.

{{< figure src="git/blog-git-4.png" caption="git/Visual Git Cheatsheet par Andrew Perterson" numbered="true" >}}

[1] [Documentation Git](https://git-scm.com/doc) <br>
[2] [GitHub Git Cheatsheet](https://training.github.com/downloads/github-git-cheat-sheet/) <br>
[3] [Visual Git Cheatsheet](https://ndpsoftware.com/git-cheatsheet.html) <br>
[4] [Vinted Proper Git](https://vinted.engineering/2015/01/02/proper-git/)
