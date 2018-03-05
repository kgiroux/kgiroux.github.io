---
layout: post
title:  "Angular Tips #11"
date:   2017-12-31 10:00:00 +0200
categories: Angular
---
# Angular : Modules

Un module est Angular, l'équivalent d'un package en Java. Il permet de regrouper l'ensemble les composants, les services, et des les exposer si nécessaire. Il regroupe également les modules à importer pour les utiliser dans les composants. Par example pour créer un composant HTTP, on doit importer le module HTTPClient qui permet d'avoir accès aux principales méthodes HTTP (get, post, put, delete ... etc)

Afin de créer une application Angular, il est nécessaire d'avoir un RootModule. Ce dernier sera le point d'entrée de l'application, et possède des caractéristiques un peu différentes des autres modules

On déclare un module, en utilisant l'annotation

```typescript
@NgModule()
```

Cette annotation contient différents types de paramètres :

Le mot clé

```typescript
bootstrap
```

 permet d'indiquer le component de démarrage. Il n'est utilisé que dans le cas du RootModule. Il s'agit d'un équivalent au Main en Java.
Le mot clé

```typescript
declaration
```

 permet de déclarer dans le module les différents components. Cela permet des les enregister afin de les utiliser dans d'autre component, en important uniquement les modules.
Le mot clé

```typescript
import
```

 permet d'importer les autres modules nécessaire au fonctionnement des components. Par exemple lorsqu'on souhaite utiliser les requêtes Http, il est nécessaire d'ajouter le module HTTP fournit par Angular.
Le mot clé


```typescript
export
```


 permet d'exporter des components afin que ceci soit disponible dans d'autres components.
Le mot clé

```typescript
providers
```

 permet d'importer et d'initialiser les services pour les components.
Voici un exemple de déclaration de module

```typescript
@NgModule({
	declarations: [
		MyFirstComponent,
		MySecondComponent,
		...
	],
	exports:[
		MyFirstComponent,
		MySecondComponent,
		...
	]
	imports: [
		BrowserModule,
		FormsModule,
		HttpModule,
		...
	],
	providers:[
		MyFirstService,
		MySecondService,
		MyThirdService,
		...
	]
})
export class MyModule{}
```