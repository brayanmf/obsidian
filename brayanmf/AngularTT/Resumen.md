> Formularios:
 texto dinamicos ejemplos:
```

#name : nombre del input(variable de plantilla)   <input type="text" #texto>

name.value: valor del input  <div>{{texto.value}}<div/>

input or button:---    <input type="button" value="enviar" (click)="funcion(text.value)"/ >  
en el .ts:
funcion(value:String){}


```


-  Interpolación
la interpolación no es nada mas que el paso de propiedades en .ts hacia el html  ~= estate React
- Property Binding(unión,vínvulo,puente)
el enlace que hay entre .ts y html
> union entre  propiedades 
```
<input [disabled]="bolAuxi">
{{stateBol()}}
.ts
	bolAuxi=false
	stateBol(){
	this.bolAuxi=true
	}
	
```
- Event Binding
> union de eventos 
```
<input type="checkbox" [checked]="bolAuxi" (click)="setCheck()">

<input type="text" #dinamicText2 [disabled]="bolAuxi" [value]="txtCheck"  >
.ts 
	txtCheck="";
  	setCheck(){
    this.bolAuxi=!this.bolAuxi;
    this.txtCheck= this.bolAuxi? "Disabled":""

  }
```

>casting and event binding

```
<input type="radio" name="textRadio" value="Sii" (click)="setTextRadio($event)" >

<input type="radio" name="textRadio" value="Noo" (click)="setTextRadio($event)" checked>

<p>Cansado?: {{textRadio}}  </p>
.ts
	
	textRadio="Noo";
  	setTextRadio(event:Event){
 	const radioElement=(<HTMLInputElement>event.target).value//casting
   	this.textRadio=radioElement==="Sii"?radioElement:"Noo";

  }
```