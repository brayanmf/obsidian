

[directivas](https://angular.io/guide/structural-directives) :
- directivas integradas :
Las directivas son clases que agregan comportamiento adicional a los elementos en sus aplicaciones Angular. Use las directivas integradas de Angular para administrar formularios, listas, estilos y lo que ven los usuarios.
- directivas de atributo :
Cambie la apariencia o el comportamiento de los elementos DOM y los componentes angulares con directivas de atributos.
- directivas  estructurales
Las directivas estructurales son directivas que cambian el diseño del DOM agregando y eliminando elementos DOM.

- Directivas de plantilla [Angular - AngularJS a Conceptos angulares: Referencia rápida](https://angular.io/guide/ajs-quick-reference#template-directives): eventos II template directives
 como eventos etc Click 


- Recordar que nuestro appmodule reconocera nuestros componentes y subcomponentes si esta declarado en ella
("al crear componentes manuales")
> crear componentes: ng generate component --name || ng g c name        +  -s -t(component inline) 

```
App Angular			Módulo raíz				Componente 		Subcomponentes
(main)                       =>	(AppModule)			=>	principal		=> decorador {
modulo principal de carga	Definicióm del componente		(AppComponent) 		- selector
				 principal a cargar						-template (html)
												- stylos (css)  }
												
																		
```
cuando y donde(quien) acciones 

> crear un servicio pero tambien --quiero saltarme las test : ng g s name  --skip-tests

 