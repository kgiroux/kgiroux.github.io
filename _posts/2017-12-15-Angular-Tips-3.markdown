---
layout: post
title:  "Angular Tips #3"
date:   2017-12-15 10:00:00 +0200
categories: Angular
---
# Ready for deployement

Lorsque l’on souhaite déployer une application Web, on souhaite plusieurs choses :

1. La stabilité
2. La sécurité
3. La performance

## Stabilité

Tout d’abord, il y a une détection des erreurs dans le TS, et dans le HTML. (Une variable privé dans les .ts, sans accesseur utilisé dans le HTML). Là ou JIT tolère ce principe, AOT ne le tolère pas. Cela permet d'avoir un code fonctionnel en production.

## Sécurité

Ensuite, AOT compile le HTML, ainsi que les components, rendant plus difficile les modifications de page HTML, ou de JavaScript.

## Performance

Enfin, AOT est plus performant car plus rapide. A contrario de JIT, il n’embarque par le Compilateur Angular (l’application partant en production, cela n’est pas nécessaire), Il s’agit de la moitié du code de Angular

### Just in time

![Just in time](/assets/jit.png)

### Ahead of time

![Ahead of time](/assets/aot.png)