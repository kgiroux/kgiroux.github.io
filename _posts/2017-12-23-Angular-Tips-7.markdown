---
layout: post
title:  "Angular Tips #7"
date:   2017-12-23 10:00:00 +0200
categories: Angular
---
# Angular : Création du composant

La troisième partie est la création de la classe représentant le composant. 

```typescript
export class MyComponent { 
 private _mymemberofclass: type; 
 public get mymemberofclass():type{ 
   return this._mymemberofclass
 } 
 public set mymemberofclass(myaffectation:type){ 
  this._mymemberofclass = myaffectation
 } 
 constructor(){ } 
}
```

Certains mots clés se rapproche du langage Java.

Le mot clé

```typescript
export
```

fait référence au mot clé

```typescript
public
```

en java. Ils ont une signification assez proche.
Lorsqu'on déclare une classe public en Java, celle ci est visible de l'ensemble des autres classes.
En TypeScript, ou en JavaScript en suivant la norme ES6, cette objet est utilisable en utilisant le mot clé

```typescript
inport
```

Le mot clé

```typescript
class
```

fait référence au mot clé

```typescript
 class
```

en java. Ils ont la même signification.
On représente un objet qui possèdera des propriétés ainsi que des méthodes. (attribut d'une classe ainsi que les accesseurs)

```typescript
Interface
```

, et

```typescript
Type
``` 

sont d'autres types de mot clé existant et que l'on peut utiliser.

Le mot clé
```typescript
constructor
```

 est la méthode permettant de créer un objet du type de la classe. Ici seront initialisés l'ensemble des propretiés par défaut d'un objet.

Le méthode ou le mot clé

```typescript
get
```

 &

```typescript
 set
 ```
  apparaisse, sont des méthodes qui permette d'accéder, et de modifier les valeurs d'un attribut de classe. Il s'agit des getter/setter classique Java. Une petite différence notamenet dans l'écriture, le type de retour de la méthode se trouve après les () à l'inverse du Java ou cela se trouve au début
