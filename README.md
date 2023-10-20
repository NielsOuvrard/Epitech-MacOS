# Epitech sur MacOS

## Table of Contents
- [Epitech sur MacOS](#epitech-sur-macos)
  - [Table of Contents](#table-of-contents)
- [Problèmes avec MacOS](#problèmes-avec-macos)
  - [Les difficultées que vous allez rencontrer :](#les-difficultées-que-vous-allez-rencontrer)
  - [Ce que je vous recommande :](#ce-que-je-vous-recommande)
  - [Installation :](#installation)
- [Solution 1 : Docker](#solution-1--docker)
  - [Points positifs :](#points-positifs-)
  - [Points Négatifs :](#points-négatifs-)
  - [Installation :](#installation-1)
- [Solution 2 : Machine Virtuelle (VM)](#solution-2-machine-virtuelle-vm)
  - [Points Positifs :](#points-positifs)
  - [Points Négatifs :](#points-négatifs--1)
  - [Installation :](#installation-)
- [Solution 3 : Machine à distance / Server](#solution-3-machine-à-distance--server)
  - [Points positifs :](#points-positifs--1)
  - [Points Négatifs :](#points-négatifs--2)
  - [Installation :](#installation--1)

# Problèmes avec MacOS

Les projets Epitech seront corrigés sur un ordinateur sur Linux Fedora.\
Si vos programmes ne sont pas parfaits, certaines erreurs peuvent
survenir.\
Celles-ci seront peut-être corrigés par MacOS. Votre programme
fonctionnera sur votre mac, mais une fois corrigé... il y a tout qui
crash ! ­­­­­­

Pour repérer les erreurs, vous allez utiliser le logiciel Valgrind.\
Ce logiciel existe pour les Mac avec les processeurs Intel (les anciens)
mais pas avec les M1, M2...

## Les difficultées que vous allez rencontrer :

Certains projets ne seront juste pas faisables sans un réel PC Linux (à
ma connaissance) : Need4Stek

Pour les projets graphiques, vous devrez passer par votre Mac
directement

## Ce que je vous recommande :

Je vous invite tous à installer **la solution sur Docker**, c'est la
plus rapide et la plus simple a installer.\
Ensuite, si vous souhaiter plus de confort après la piscine, je vous
recommande d'essayer une VM.\
De plus, avec un autre étudiant nous allons réaliser un cours (workshop)
sur l'installation d'un server Ubuntu après votre piscine.

## Installation :

Pour les logiciels suivants, ouvrez votre terminal et copiez les
commandes en vert.

**HomeBrew** : gestionnaire de paquets, permet d'installer CSFML, SFML
et bien d'autres\
/bin/bash -c \"\$(curl -fsSL
https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)\"

**CSFML et SFML** (projets jeu vidéo)

brew install csfml

brew install sfml

Facultatif : Un beau terminal avec **oh-my-zsh** :\
sh -c \"\$(curl -fsSL
https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)\"

# Solution 1 : Docker

Avec Docker, votre mac va simuler le **processeur**, et le **système
d'exploitation** linux Fedora.

## Points positifs :

Tout ce qui fonctionnera dessus fonctionnera sur la mouli, et vous aurez
accès à Valgrind !

## Points Négatifs :

C'est leeeeeeeeent ! Compiler sur Docker, surtout avec un processeur ARM
est très lent, on parle de x10 à x50 en temps...

Cela peut dépanner, mais compilez pas en permanence avec.

Pas d'affichage graphique, donc pour les projets de jeu vidéo, il faudra
faire sans.

## Installation :

Commencez par créer votre clé ssh :\
<https://www.youtube.com/watch?v=X40b9x9BFGo>

Docker :

<https://www.docker.com/>

Lancez Docker une fois installé.

Epitech Container:\
<https://github.com/LucasLeRay/EpitechDocker>

Clonez le repo à la racine de votre espace de travail.

Dans le dossier du container, executez les commandes suivantes :

make build

make run

Vous êtes dans un environnement Fedora.

Essayez la commande « valgrind \--version », celle-ci devrait
fonctionner, comme sur un Linux.\
Lorsque vous souhaiterez relancer le container, ne faites que la
commande « make run ».

# Solution 2 : Machine Virtuelle (VM)

Une machine virtuelle, c'est bien différent d'un Docker.\
Comme dit précédemment, Docker simule le système d'exploitation, et le
processeur !**\
**Une VM quant à elle, ne simule **que le système d'exploitation**.
Ainsi, vous verrez bien votre linux avec un processeur « M1 ».

## Points Positifs :

Valgrind existe bien sur les Linux ARM, hourra !

Affichage graphique (mais je n'ai jamais réussi à faire tourner SFML
dessus...)

## Points Négatifs :

J'ai eu l'occasion de faire ma tek1 en grande partie sur Parallèle
Desktop avec Fedora 16\
C'est un logiciel payant

J'ai eu de nombreux crash (je n'avais pas la dernière version de
Parallèle Desktop), peut-être 1 crash toutes les 5 heures

De nombreuses fonctionnalités de MacOS ne sont plus accessibles (pas de
copié collé entre les systèmes)

J'ai eu des soucis avec le clavier, entre ctrl et cmd

J'ai eu des soucis de couleurs, et de plein écran\
\
C'est très demandeur en ressources -\> ça chauffe, ça consomme de la
batterie...

Et cela peut être lent

## Installation :

Choisissez le logiciel de votre choix, et installez-le :

Parallèle Desktop :\
<https://www.youtube.com/watch?v=QO2C14FiUMM>

Virtual Box :

<https://www.youtube.com/watch?v=7RwS6WgLthk>

Autre...

# Solution 3 : Machine à distance / Server

Quoi de mieux pour **développer des logiciels sur linux**, que de
**développer des logiciels sur linux **?

On parle d'un vieux pc (j'ai utilisé pendant 6 mois le PC du conseil
général, pas besoin de puissance...). On le formate avec un linux server
(Ubuntu server, Fedora server... peu importe). On le relie au réseau
avec un câble Ethernet, on bidouille et TADAM !

Avec une commande, on se connecte de notre Mac (a Epitech) avec notre PC
(chez nous), et on peut coder (même avec VScode)

## Points positifs :

Tout ce qui fonctionnera dessus fonctionnera sur la mouli, et vous aurez
accès à Valgrind !

C'est rapide ! Même avec un vieux pc, compiler du C est très rapide.\
(Si vous choisissez un PC un peu puissant (i3, i5), c'est encore mieux)

Vscode grâce à cette extension :\
<https://marketplace.visualstudio.com/items?itemName=ms-vscode.remote-explorer>

## Points Négatifs :

Pas d'affichage graphique, donc pour les projets de jeu vidéo, il faudra
faire sans.

Besoin d'internet en permanence

## Installation :

Nous réaliserons un cours (workshop) à ce sujet après votre piscine, en
espérant vous y retrouver. Cependant, si vous souhaitez tout de même le
faire de votre côté, voici quelques indications sur comment s'y
prendre :

1 : Clé bootable -\> installez le système d'exploitation, puis
connectez-le au réseau

2 : Ouvrez un port sur le server (Ubuntu server : avec **UFW**), le port
22 par exemple

3 : Ouvrez un port sur votre box internet, et redirigez les vers le port
(22) de votre server

Et on est bon, vous vous y connectez avec cette commande :

ssh user@ip -p port

(Mettez bien l'adresse IP de votre box, pas votre IP local)

**Par exemple :**

ssh <admin@192.168.0.1> -p 22
