---
layout: post
title:  "Angular Tips #9"
date:   2017-12-27 10:00:00 +0200
categories: Angular
---
# Angular : Template, condition, boucle

Avec angular il est possible de faire des templates dynamiques. En effet il existe des mots clés permettant d'afficher le contenu d'un tableau ou même de faire un affichage différent en fonction d'une variable. Nous allons introduire les mots clés les plus connus. 

## ngIF

Le mot clé ngIf permet d'afficher le template si la condition est remplie. Depuis la version 4, un second mot clé est venue compléter ce dernier, else


```html
<div *ngIf="isValid;then else othercontent">
	here is ignored
</div>
<ng-template #>
	content here...
</ng-template>
<ng-template #othercontent>
	other  here...
</ng-template>
```


## ngFor
Le mot clé ngFor permet d'afficher des élements en parcourant un tableau par exemple afin d'éviter la duplication de code. Pour cela on indique dans le ngFor, le code suivant let object in objectCollection Cela permet de parcourir tout les objets se trouvant dans la liste objectCollection Dans la boucle "object" permettra d'acceder de facon unitaire à ces différentes propriétés

```html
{% raw %}
<div *ngFor="let object in objectCollection">
	<tr>
		<td>{{object.properties1}}</td>
		<td>{{object.properties2}}</td>
		<td>{{object.properties3}}</td>
	</tr>
</div>
{% endraw %}
```