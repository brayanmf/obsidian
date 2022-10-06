para crear y prepara nuestro objeto a recibir
 creamos  2 archivos
-BaseDto:esta es la base cosas comunes que se repiten en tods ya que lo heredan
ejem
```
public class BaseDto  
{  
    public int Id { get; set; }  
    public string? Codigo { get; set; }  
    public DateTime FechaReg { get; set; }  
    public DateTime FechaMod { get; set; }  
    public int IdUsuario { get; set; }  
    public string? Nombre { get; set; }  
    public string? Descripcion { get; set; }  
    public int Tipo { get; set; }  
    public bool Activo { get; set; }  
}

```

-FormatoDto
```
public class FormatoDto : BaseDto  
{  
   
      
    public List<SeccionDto> Secciones { get; set; }  
}
```
-secciones
```
public class SeccionDto : BaseDto  
{  
    public List<GrupoDto> Grupos { get; set; }  
}
```

-grupos
```
public class GrupoDto : BaseDto  
{  
    public List<ParametroDto> Parametros { get; set; }  
}


```
-parametros

```

namespace inspecciones_core.Model.Core;  
  
public class ParametroDto : BaseDto  
{  
    public string? Placeholder { get; set; }  
    public string? Label { get; set; }  
    public bool Visible { get; set; }  
    public bool Obligatorio { get; set; }  
    public bool Editable { get; set; }  
      
    public int Columna { get; set; }  
      
    public  int fila { get; set; }  
      
      
    public string? dato { get; set; }  
}
```


esto se mirara de la siguente forma

```
```json
{
  "id": 0,
  "codigo": "string",
  "fechaReg": "2022-07-31T18:46:56.192Z",
  "fechaMod": "2022-07-31T18:46:56.192Z",
  "idUsuario": 0,
  "nombre": "secciones",
  "descripcion": "string",
  "tipo": 0,
  "activo": true,
  "secciones": [
    {
      "id": 0,
      "codigo": "string",
      "fechaReg": "2022-07-31T18:46:56.193Z",
      "fechaMod": "2022-07-31T18:46:56.193Z",
      "idUsuario": 0,
      "nombre": "seccion name",
      "descripcion": "string",
      "tipo": 0,
      "activo": true,
      "grupos": [
        {
          "id": 0,
          "codigo": "string",
          "fechaReg": "2022-07-31T18:46:56.193Z",
          "fechaMod": "2022-07-31T18:46:56.193Z",
          "idUsuario": 0,
          "nombre": "grupo name",
          "descripcion": "string",
          "tipo": 0,
          "activo": true,
          "parametros": [
            {
              "id": 0,
              "codigo": "string",
              "fechaReg": "2022-07-31T18:46:56.193Z",
              "fechaMod": "2022-07-31T18:46:56.193Z",
              "idUsuario": 0,
              "nombre": "string",
              "descripcion": "string",
              "tipo": 0,
              "activo": true,
              "placeholder": "string",
              "label": "string",
              "visible": true,
              "obligatorio": true,
              "editable": true,
              "columna": 0,
              "fila": 0,
              "dato": "string"
            }
          ]
        }
      ]
    }
  ]
}
```

entonces en el controlador o servicio


```
public async Task<Response<FormatoDto>> GuardarFormato(FormatoDto req){}
```