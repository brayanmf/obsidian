+-
recibimos el string
una consulta con QueryAsync
```
var formato =  
    (await cn.QueryAsync<GrupoParametrosDto>(  
        @"select *  
from core.grupo_parametros where nombreFormato = @nombreFormato",  
        new { nombreFormato = nombreFormat })).ToList();
```

separamos los agrupamos seccion y grupo por nombre 

```
var grupo = formato.GroupBy(x => x.NombreGrupo);  
var seccion = formato.GroupBy(x => x.NombreSeccion);
```

para responder tenemoe el general

```
  
var formatoResp = new FormatoDto();
```

,lo tenemos que armar pero a lo inverso
ya que recibe el name :" strgin"

```
var formatoResp = new FormatoDto();  
  
formatoResp.secciones = seccion.Select(x => new SeccionDto()  
{  
      
    nombre = x.FirstOrDefault().NombreSeccion,  
    grupos= grupo.Select(y => new GrupoDto  
    {  
          
        nombre = y.FirstOrDefault().NombreGrupo,  
        parametros = y.Select(z=> new ParametroDto  
        {  
            field_placeholder = z.Placeholder,  
            field_label = z.Label,  
            field_visible = z.Visible,  
            field_mandatory = z.Obligatorio,  
            field_editable = z.Editable,  
            field_min_caracteres = z.minCaracteres,  
            field_max_caracteres = z.maxCaracteres,  
            field_row = z.fila,  
            field_column = z.columna,  
            field_value = z.dato  
        }).ToList()  
          
          
    }).ToList()  
}).ToList();
```
 y nuestro servicio
 ```
   
return new Response<FormatoDto> { Body =formatoResp , Success = true, Code = 200 };
```
