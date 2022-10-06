en nuestra etiqueta agregamos una directiva de atributo 
.html
```
       <a [routerLink]="['/updateEmpleados',i]" [queryParams]="{action:'eliminar'}"

                  >direccioonar</a>
```

.ts 
```
  accion: string = "";
  
   constructor(private routeParam: ActivatedRoute){
    //this.accion = this.routeParam.snapshot.queryParams['action']
   }
//or   
     ngOnInit(): void {
	 this.accion = this.routeParam.snapshot.queryParams['action']
	 }
   ```