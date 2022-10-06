# Dapper
- Execute:
	se usa para realizar operaciones INSERT, UPDATE y DELETE.
- Query
	Por lo general, se utiliza para obtener varios objetos de la base de datos
- QueryFirst
	 Esto se usa cuando solo necesitamos un elemento que coincida con las especificaciones proporcionadas.
- QueryFirstOrDefault
	método de extensión al que se puede llamar desde cualquier objeto de tipo IDbConnection. Puede ejecutar una consulta y asignar el primer resultado, o un valor predeterminado si la secuencia no contiene elementos
- QuerySingle
	ejecuta una consulta y asigna el resultado siempre que solo haya un elemento en la secuencia. Si no hay exactamente un elemento en la secuencia
- QuerySingleOrDefault
	  este método funciona igual pero devuelve un valor predeterminado si no se devuelve ningún elemento de la base de datos.`QuerySingle`
- QueryMultiple
	este método puede ejecutar muchas consultas simultáneamente con un comando y mapear los resultados
	