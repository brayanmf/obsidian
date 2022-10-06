### config routing

en angular router gestiona nuestras rutas , ya lo tiene internamente

1ro crear un objeto donde relacione mis rutas y componentes 
app.module.ts
```
const appRoutes: Routes = [

  {

    path: '', component: CrudHeroComponent

  },

  {

    path: 'formInput', component: PracticeComponent

  },

  {

    path: 'calculator', component: CalculatorComponent

  },

  

]
```

2do. importamos el modulo pasando argumento nuestro objeto

```
  imports: [
  ...,
    RouterModule.forRoot(appRoutes)

  ],
```

