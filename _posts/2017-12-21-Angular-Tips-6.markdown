---
layout: post
title:  "Angular Tips #6"
date:   2017-12-21 10:00:00 +0200
categories: Angular
---
# Angular : Les déclarations

Afin de pouvoir utiliser le composant dans la page Web HTML, il est nécessaire de lui fournir des informations qui lui permet d'être défini.

## Component

## La déclaration

Voici un exemple de déclaration

```typescript
@Component ({
 selector: 'app-root',
 templateUrl: './app.component.html',
 styleUrls: ['./app.component.css'] })
```

Décomposons le code précédent

```typescript
@Component
```

qui est une annotation permettant au framework Angular de comprendre que l’élément en cours est un component.

Dans cette annotation, on définit un certain nombre d’éléments. Il est composé au minimum de 3 éléments:

```typescript
selector: 'app-root'
```

Cet élément permet de définir la balise HTML qui sera dans le code HTML afin d’utiliser le component. Avec cette balises, Angular completera le contenu de cette balise avec le HTML associé

```typescript
templateUrl: './app.component.html'
```

Cet élément permet de définir le fichier contenant le template du composant. Il s’agit de code HTML

```typescript
styleUrls: ['./app.component.css']
```

Cet élément permet de définir le fichier contenant le style du composant (la couleur de l’arrière-plan …)
