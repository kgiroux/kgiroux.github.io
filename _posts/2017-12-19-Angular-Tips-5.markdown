---
layout: post
title:  "Angular Tips #5"
date:   2017-12-19 10:00:00 +0200
categories: Angular
---
# Angular : Les imports

Afin de comprendre le fonctionnement d'Angular, il est nécessaire de revenir les principes de ce framework.
Le principe le plus important d'Angular est la vision composant (Component) qu'il met en avant. On va créer une page en la composant de divers parties qui seront réutilisable par la suite.

## Component

Un Component est facilement assimillable à une Classe en Java. Chaque component est composé de plusieurs parties.
Les principales parties nécessaire pour la déclaration d'un composant sont les suivantes :

* Les imports.
* Les déclarations
* Le contenu du composant.


## Les imports

```typescript
import { Component } from '@angular/core';
```

Cette partie permet d’importer l’ensemble des librairies, composants, interfaces et autres pour la création de votre component.
Elle est composé de :

```typescript
import
```

Ce mot clé permet de définir que l’on souhaite ajouter cette dépendance au component

```typescript
{ Component }
```

Il s'agit du nom du classe que l’on souhaite importé. Les élements importés sont mis entre {} , et spéraré par des ","

```typescript
from '@angular/core';
```

 Enfin, la dernière partie définie le module dans lequel se trouve cet élément que l'on importe, ici le module est @angular/core