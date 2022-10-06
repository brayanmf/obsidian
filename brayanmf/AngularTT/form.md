

- use formulary for the class models
```
import { ..., Input } from '@angular/core';


@Input() hero?:SuperHero;
```

in file app.module.ts
```
import {FormsModule} from  '@angular/forms'

imports:[
...,
FormsModule
]
```
.html
```
 <div *ngIf="hero" class="card m-5 p-3" style="width: 30rem;"> //exist hero?

    <h2>{{hero.name}}</h2>

    <div>

      Name:

      <input class="form-control" [(ngModel)]="hero.name"  placeholder="Name" />

    </div>

    <div>

      First Name:

      <input class="form-control" [(ngModel)]="hero.firstName"   placeholder="First Name" />

    </div>

    <div>

      Last Name:

      <input class="form-control" [(ngModel)]="hero.lastName"  placeholder="Last Name" />

    </div>
```