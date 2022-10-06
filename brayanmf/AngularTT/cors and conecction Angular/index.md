- en app.module.ts agregar e importar

```
import {HttpClientModule} form '@angular/common/http' 

imports:[...,HttpClientModule]

```
-  declarar una variable en tu archivo de  service 
```

import {HttpClient} from "@angular/common/http";
import {modeldata} from 'models/ClassModel';
import {environment}from 'src/envornments/environment'
import {Observable} from 'rxhs/internal/Observable


private url="addList"
construct(private http:HttpClient){}

public getDataAsync():Observable<modeldata[]>{
	return this.http.get<modeldata[]>(`${environment.val}/${this.url}`)
}

```
component.name.ts
```
import {Service} from 'service/classService';
import {modeldata} from 'models/classModel'



constructor(private service:Service)
ngOnInit();void{
	this.service
	.getDataAsync()
	.subcribe((result:modeldata[])=>(this.heroes=result))
}

```

