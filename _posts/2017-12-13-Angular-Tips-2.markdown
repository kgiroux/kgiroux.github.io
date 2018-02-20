---
layout: post
title:  "Angular Tips #2"
date:   2017-12-13 10:00:00 +0200
categories: Angular
---


# Angular (2+) vs Angular

1. La principale différence entre Angular 1 et Angular X, est la vision Composant de l’architecture. On va créer des composants qui vont constituer une Page et directement les ajoutés comme élément HTML (non native aux HTML). 
2. Une autre différence c’est le support de multilangage de programmation. Il est possible de développer une application en JavaScript, Dart, TypeScript (ce dernier est recommandé par Google). 
3. Enfin afin d’en citer trois c’est le support des plateformes mobiles nativement. 

# Deux modes de compilation JIT vs AOT

De plus, Angular X, introduit deux modes : JIT, et AOT. Il s’agit de deux modes de compilation dédié et fait pour le développement. 
1. JIT : Just In Time, permet de prendre à chaud les modifications que l’on peut faire sur le code, sans rien avoir à faire. Fini le redéploiement sur des servers ou le reload. Tout ceci est pris en charge par le mode JIT. (Lors de la compilation JIT, le server, va mettre des « observers » sur les fichiers afin de détecter les changements.)
2. AOT : Ahead of Time permet à contrario de préparer une application production ready. Il s’agit d’une compilation des sources afin de gagner en performance. Le code devient « statique ».    