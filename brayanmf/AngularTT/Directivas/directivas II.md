<ng-template></ng-template> 
-- definir una etiqueta que no renderiza por defecto util para else
<div *ngIf="registrado;else sinRegistrar">estoy registrado</div>

<ng-template #sinRegistrar >
 	no registrado
</ng-template>
```
html:5

no registrado
```
