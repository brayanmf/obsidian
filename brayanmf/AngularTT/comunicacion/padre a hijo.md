para poder comunicarnos usamos @Input
### parent
.html parent  .ts =>old:number=5 ;child:string="hi"
```
<div>
{{name}}

{{old}} </div>

<app-child [name1]=name [old1]=old ></app-child>
```

### child
```
child.ts
@input name1:string=""
@input old1:number=0

child.html
<div>
hi
5
<div>

```