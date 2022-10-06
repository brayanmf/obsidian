para poder irnos a la ruta que queremos mediante una etiqueta a,necesitaremos una directiva de atributo


component.html
```

    <a [routerLink]="['/updateEmpleados',title]"> {{title}}</a>
```
.app.module.ts

```
appRoutes:Routes=[
...,
{path:'updateEmpleados/:titulo',component:components}

]
```

component.ts

```
  constructor( private routeParam: ActivatedRoute) { }
    ngOnInit(): void {

    this.id = this.routeParam.snapshot.params['id'];
	}
```