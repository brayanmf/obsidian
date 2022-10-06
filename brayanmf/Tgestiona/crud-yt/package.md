> program.cs ``` global using SuperHeroAPI.Data;
  
la trinidad entitiy recordar que con el core tenemos relacionamos Dto

- DbContext->Microsft.EntityFrameworkCore
//UseSqlServer
- ->Microsoft.EntityFrameworkCore.Design
- ->Microsoft.EntityFrameworkCore.SqlServer

ver comandos 
```
dotnet ef
```

listar pacquetes 
```
dotnet list package
```

create app for api
```
dotnet new webapi -n NAME
```


install entityframework.core 

```
 dotnet add package   Microsft.EntityFrameworkCore
```

install entityframework.design 6.0.6  - 6/2022

```
dotnet add package Microsoft.EntityFrameworkCore.Design --version 6.0.6
```


install entityframework.sqlserver  7.0.0 - 6/2022
```
dotnet add package Microsoft.EntityFrameworkCore.SqlServer --version 7.0.0-preview.5.22302.2
```

models.Dto

```
>dotnet tool install -g dotnet-ef
// permite hacer la migracion con entityframewokr 

//en la instancia de nuestro proyecto 
>dotnet ef migrations add CreateInitial --project nameproject
>dotnet ef migrations add Initial

// prepara nuestro objeto para la migracion
>dotnet ef database update --project nameproject
// sube a la base de datos :]
```

cors from angularjs


```
programs.cs
builder.Services.AddCors(options=>options.AddPolicy(name:"SuperHeroOrigins",
policy=>{
	policy.WithOrigins("http://localhost:4200")
	.AllowAnyMethod()
	.AllowAnyHeader();
}
));
...
app.UseCors("SuperHeroOrigins");

```

