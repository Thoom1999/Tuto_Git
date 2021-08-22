# Tuto_Git

## Introduction

Git est un outils pour versionner du code. C'est un incontournable pour les projets open source et libre. L'idée derrière git est plutôt simple.

Imaginons que je souhaite contribuer à un projet déjà existant. Supposons que j'ai repéré un problème et que je sais comment le résoudre ou bien que je souhaite y ajouter une nouvelle fonctionnalité. La procédure est simple : 
* je clone le `repository`
* je crée une `branche`
* j'écris ma contribution dans la branche
* je fais une `pull request` 

Pull request signifie soumettre ma proposition aux personnes gérant le projet et ceux-ci adopteront ou non ma contribution. S'ils acceptent ils `merge` ma branche sur la branche principale et mon travail et alors pris en compte dans le projet.

## Comment installer git ? 

Il suffit de le télécharger à cette adresse : https://git-scm.com/downloads Il faut bien penser à se créer un user en donnant son mail et son pseudo

Pour vérifier que git est bien installé il faut ouvrir l'invité de commande et taper `git --version`

## Workflow 

On utilisera pour notre projet un système de branche appelé gitflow. Il y a trois types de branches : main, develop et feature (j'ai menti il y en a cinq mais les deux autres ne serviront pas)
* La branche main comporte la version la plus stable de notre travail
* La branche develop porte très bien son nom
* Les branches feature sont les branches où seront développées les différentes fonctions de notre logiciel. Une fois qu'une branche est finie et vérifiéé elle sera merge sur la branche develop

## Commande clone

Elle sert à cloner un repository c'est à dire télécharger le projet sur votre ordinateur. 
`git clone [lien]`

## Créer une branche

Dans notre cas il faudra uniquement créer des brancches feature. Pour ce faire il y a deux commandes à executer : 

`git checkout develop`

`git branch feature/nom-de-ma-branche`

__Rq__ : 
* checkout permet de changer de branche
* `git branch` permet de connaître toutes les branches et de savoir sur laquelle on est.

## Sauvegarder son travail sur la branche (commit)

Il y a deux grandes étapes : 
1. Dire à git quel fichier sauvegarder via la commande 
`git add les-fichier-que-je-veux-ssauvegarder`
1. Sauvegarder son travail via la commande `git commit -m 'message de commit décrivant le travail effectué'`

__Attention :__ Bien veiller à être sur la bonne branche lorsque l'on fait la commande git commit

__Rq :__ 
* `git add .` permet de prendre en compte tous les fichiers modifiés
* `git status` permet de voir les fichiers pris en compte ou non
* `git log` permet de voir les derniers commit ainsi que leur message de commit

![](https://github.com/Thoom1999/Tuto_Git/blob/17f72e1bf235e52a0732e242e70aa3146de70eaf/images/2021-08-13_11h26_31.png?raw=true)

## Publier sa branche sur GitHub 

Pour diverses raisons, on peut vouloir publier sa branche pour que les autres contributeurs du projet puissent la voir. 
Il suffit simplment d'utiliser la commande : `git push -u origin nom-de-ma-branche`

## Merge sa branche sur develop 

Une fois qu'une nouvelle fonctionnalité est finie, il faut la merge sur la branche develop. 
Pour ce faire, il faut publier sa branche (cf partie précédente) puis utiliser github.com pour effectuer la pull request.

![](https://github.com/Thoom1999/Tuto_Git/blob/40ef4569b99d05e55e0802c5276e0775ca59d169/images/2021-08-12_19h59_44.png?raw=true)

A l'issue de la pull request, d'autres personnes vont relire le travail et en fonction du cas soit refuser la PR (pas dans notre cas), soit faire part d'amélioration ou soit l'accepter.

## Voir l'arbre git

Pour voir l'arbre git, il faut utiliser la commande `git log --all --decorate --oneline --graph`, moyen mnémotechnique : a dog

## Exercice 

Clonez ce repo et ajoutez votre nom à la fin de ce document. Pour ce faire créez une branche (branche-de-mon-nom), faite le nécessaire, publiez la branche et faire une PR pour que vos modifications apparaissent dans la branche main.

Thomas
Martin
