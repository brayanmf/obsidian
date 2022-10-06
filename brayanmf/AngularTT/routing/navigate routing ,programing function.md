### routing programatico


.html 
```
<a (click)="irHome()" >click me <a>
```

.ts

```
construct(private route:Route){}


irHome():void{
this.route.navigate(["home"])// where your home it in route => path:"home"
}
```