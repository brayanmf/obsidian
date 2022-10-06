para poder comunicarnos usamos @Output

## child
child.ts
```
@Output() itemEvent=new EventEmitter<string>()
//prepara un evento ,del hijo. El padre lo detecta al ejecutarse el evento y lo recibe 


addNewItem(value:string){

this.itemEvent.emit(value)
}


```
child.html

```
<label>caracteristica<label>
<input type="text"  #item  />
<button (click)="addNewItem(item.value)" >Add parent</button>

```

## parent
parent.ts
```
  listCharacteristic: Array<string> = [];
  
  addCharacteristicList(value: string) {//for binding

    this.listCharacteristic.push(value)

  }
```
parent.html
```
     <app-edit-empleado (characteristic)="addCharacteristicList($event)">
	 (characteristic)->exec event ===> exect funtion addCharaceteristList($event)
	 ///new eventemmit ->is create callback funtion for detect variable changeable 
	 //// characeterist(e=>{addcharacteristList(e)})
	          
	 </app-edit-empleado>

        <ul>

            <li *ngFor="let characterist of listCharacteristic ">{{characterist}}</li>

        </ul>

```