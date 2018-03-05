---
layout: post
title:  "Angular Tips #8"
date:   2017-12-25 10:00:00 +0200
categories: Angular
---
# Angular : Data-binding

```html
<div>
	<input type="text" [(ngModel)]="mavariable">
	<p>{{mavariable}}</p>
</div>
```

Il est possible de faire du data-binding avec Angular. Le data-binding permet de mettre à jour les valeurs dès que l’on détecte un changement. L’objectif est de représenté la vue pour l’utilisateur en fonction des données que l’on récupère d’un serveur par exemple. Pour cela, il suffit de déclarer un binding entre la vue (le template HTML), et le composant, et le reste est fait par le Framework. Il existe plusieurs moyens de faire du data-binding :
Des données vers la vue :
```javascript
{% raw %}
{{myvalue}}
{% endraw %}
```

signifie que l’on souhaite évaluer l’expression. Cela est pratique pour l’affichage de données.

```html
[target]="expression"
```

est une affectation dans des balises html par exemple.
Ces deux version permette d'afficher sur la page des données en lecture seul provenant d'une source de données (serveur, ...).
De la vue vers le composant :

```html
(target)="statement"
```

est utilisé par exemple dans le remplissage d'un formulaire sur une page web. Le changement des valeurs remplira l'objet qui sera envoyé vers le serveur.
Data-binding bidirectionnel

```html
[(target)]="expression"
```

represente le data-binding bidirectionnel. Il combine l'écriture des deux autres version du data-binding.