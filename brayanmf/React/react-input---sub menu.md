al hacer abrir un sub menu en material-react
y querer escribir se perdia el foco  lo raro era que con solo
ciertas teclas  por ello esta solucion me fue util



```


  const onKeyDown = (e) => {

    e.stopPropagation();

  };
 

    <MenuItem
open={open}

      >

    

      </MenuItem>

  

      <Menu

       
        {...props}

      >

        <MenuItem>

          <TextField    onKeyDown={onKeyDown}  />

        </MenuItem>

        <MenuItem>
```