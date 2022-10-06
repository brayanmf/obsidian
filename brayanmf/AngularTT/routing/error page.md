

para la ruta de error tenemos que colocar en nuestro  "app.module.ts" recordar que es en la parte mas baja 

app.module.ts
```
const appRoutes: Routes = [

  ...,

  { path: '**', component: ErrorPageComponent }

]
```

component.html
```
<div>Error <div>
```