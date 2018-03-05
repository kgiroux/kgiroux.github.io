---
layout: post
title:  "Angular Tips #10"
date:   2017-12-29 10:00:00 +0200
categories: Angular
---
# Angular : Services, condition, boucle

Avec angular il est possible de créer des services réutilisable par plusieurs composants afin d'éviter la duplication de code, ou simplement afin de rassembler les fonctionnalités identiques. 
Pour cela on utilise l'annotation

```typescript
@Injectable()
```


```typescript
import { environment } from '../../../../environments/environment';
import { TypeData} from '../../dto/typeData.dto'
import { Inject, Injectable } from '@angular/core';
import { Headers, Http, Response} from '@angular/http';
import { AuthHttp } from 'angular2-jwt';
import { Observable} from 'rxjs/Rx';
 
@Injectable()
export class SubmenuLathService {
private _headers: Headers = new Headers({
 'Content-Type': 'application/json',
 'Access-Control-Allow-Origin': '*',
 'Access-Control-Allow-Methods': 'POST, GET, OPTIONS, DELETE, PUT',
 'Access-Control-Allow-Headers': 'content-type,accept'
 });
 
get headers(): Headers {
  return this._headers;
 
}
set headers(headers: Headers) {
  this._headers = headers;
 
}
 
constructor(  private http: Http, private authHttp: AuthHttp) {}
public updateMessage(data: TypeData): Observable {
  lath.date = new Date().getTime();
  return this.authHttp
    .post(myUrlPost, 
      JSON.stringify(lath), { headers: this.headers })
    .map((res: Response) => res, { headers: this.headers });
}
}
```

## Services
L'utilisation des services à une place importante dans le Projet SmartDisplay. En effet ce dernier, utilise les services dans le cadre d'un client HTTP, en exposant les différentes méthodes HTTP. En faisant cela, les différentes méthodes sont utilisables dans différents composants. Pour utiliser les services, il faut les inclures dans la déclaration du module. (Voir plus loin). Dans le code ci-dessus, on déclare une méthode qui permet de faire un requeste POST, sur une Url.