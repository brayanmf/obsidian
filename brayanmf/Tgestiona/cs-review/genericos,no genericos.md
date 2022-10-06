### no genéricos
#### Problemas :/  :
1. Las clases de colección no genéricas como **ArrayList**, **Hashtable**, **SortedList**, **Stack** y **Queue** se trabajan en el tipo de datos de objeto. Eso significa que los elementos agregados a la colección son de tipo objeto. Como estas clases de recopilación no genéricas funcionaban en el tipo de datos de objeto, podemos almacenar cualquier tipo de valor que pueda conducir a una excepción en tiempo de ejecución debido a la falta de coincidencia de tipos.
2. El segundo problema con las clases de recopilación no genéricas es que obtenemos una sobrecarga de rendimiento. La razón de esto es el boxeo y el unboxing.

> Nota: Boxear significa convertir un tipo de valor en un tipo de objeto y Unboxing significa convertir un tipo de objeto de nuevo al tipo de valor.
### genéricos
Los dos problemas anteriores de las colecciones no genéricas son superados por las colecciones genéricas en C#. .NET Framework ha vuelto a implementar todas las clases de colección existentes**, como ArrayList, Hashtable, SortedList, Stack** y **Queue**, etc. en colecciones genéricas como **ArrayList<T>, Dictionary<TKey, TValue>, SortedList<TKey, TValue>, Stack<T>** y **Queue<T>**.
	
>Nota:Aquí el < T > se refiere al tipo de valores que queremos almacenar debajo de ellos.
	
```
	List<int> listOfInteger=new List<int>();
	List<float> listOfFloat=new List<float>();
	List<string> listOfString=new List<string>();
```

Las clases Generic Collection se implementan en el espacio **de nombres System.Collections.Generic**. Las clases que están presentes en este espacio de nombres son las siguientes.
1.  **[Lista<T>](https://dotnettutorials.net/lesson/list-collection-csharp/):** Representa una lista fuertemente tipada de objetos a los que se puede acceder por índice. Proporciona métodos para buscar, ordenar y manipular listas. Crece automáticamente a medida que le agrega elementos.
2.  **[HashSet<T>](https://dotnettutorials.net/lesson/generic-hashset-collection-class-in-csharp/):** Representa un conjunto de valores. Elimina elementos duplicados
3.**SortedSet<T>:** De forma predeterminada, almacena los elementos en orden ascendente y no almacena elementos duplicados. Se recomienda utilizar si tiene que almacenar elementos únicos.
4.   **Queue**<T>:** La clase generic Queue<T> Collection en C# se utiliza para los elementos Enqueue y Dequeue en orden FIFO (First In First Out). La operación Enqueue agrega un elemento en una colección, mientras que la operación Dequeue se usa para quitar el elemento agregado en primer lugar de la colección de colas.
5.  **Dictionary<TKey, Tvalue>:** Representa una colección de claves y valores.
6.  **SortedDictionary<TKey, TValue>:** Representa una colección de pares clave/valor que se ordenan en la clave.
7.  **SortedList<TKey, TValue>:** Representa una colección de pares clave/valor que se ordenan por clave en función de la implementación System.Collections.Generic.IComparer asociada. Agrega automáticamente los elementos en orden ascendente de clave de forma predeterminada.
8.  **LinkedList< T >:** Representa una lista doblemente enlazada.


