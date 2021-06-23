# Trabajo Practico N° 7  
## Ejercicio 1
- Objetos del tipo LinkedList y List, ¿Cuales son las diferencias que tienen?  
  - Clase List 
  Representa una lista de objetos fuertemente tipados a la que se puede obtener acceso por índice. Proporciona métodos para buscar, ordenar y manipular listas.

  ```
  List<T> parts = new List<T>()
  ```
    
  T representa el tipo de elementos de la lista y puede ser tanto una clase como variables primitivas.  

  - Clase LinkedList  
  Representa una lista doblemente enlazada.  

  ```
  LinkedList<T> parts = new LinkedList<T>()
  ```
  
  T representa el tipo de elementos de la lista y puede ser tanto una clase como variables primitivas. Cada nodo de la lista apunta tanto al Siguiente (Next) como al Anterior (Previous).  

  ###### Diferencias  
  List<T> está básicamente respaldado por una matriz que generalmente es más grande que el número actual de elementos. Los elementos se colocan en una matriz y se crea una nueva matriz cuando la anterior se queda sin espacio. Esto es rápido para el acceso por índice, pero lento para eliminar o insertar elementos dentro de la lista o al inicio. Agregar/eliminar entradas al final de la lista es razonablemente barato.  
  
  LinkedList<T> es una lista doblemente enlazada: cada nodo conoce su entrada anterior y la siguiente. Esto es rápido para insertar después/antes de un nodo particular (o la cabeza/cola), pero lento en el acceso por índice.

  ###### Concluciones
  Un List<T> es en realidad una matriz, lo que significa que su operación Add es O(1) al final y O(n) al frente, pero puedes indexarlo en O (1).  
  Un LinkedList<T> es, como se dice, una lista vinculada. Dado que está doblemente vinculado, puede agregar elementos al frente o atrás en O(1) pero indexarlo es O (n).  

  LinkedList<T> generalmente tomará más memoria que List<T> porque necesita espacio para todas esas referencias siguientes/anteriores, y los datos probablemente tendrán menos localidad de referencia, ya que cada nodo es Un objeto separado. Por otro lado, un List<T> tiene una matriz de respaldo que es mucho más grande que sus necesidades actuales.

- Objeto Diccionario.   
  Los diccionarios en C # implementan la interfaz IDictionary. Existen varios tipos de Diccionario, pero el más utilizado es el Diccionario genérico, a menudo denominado:  

  **Dictionary<TKey,TValue>**  
  Contiene una clave específica de tipo y un valor correspondiente específico de tipo. Esto es básicamente lo que separa un Diccionario de una Lista: los elementos de una lista vienen en un orden específico y se puede acceder a ellos mediante un índice numérico, donde los elementos de un Diccionario se almacenan con una clave única, que luego se puede utilizar para recuperar el Artículo de nuevo.

  ```
  Dictionary<string, int> users = new  Dictionary<string, int>();  
  users.Add("John Doe", 42);  
  users.Add("Jane Doe", 38);  
  users.Add("Joe Doe", 12);  
  users.Add("Jenna Doe", 12);  
  Console.WriteLine("John Doe is " + users["John Doe"] + " years old");

  ```  

- Beneficios de usar una biblioteca, por que pondria una clase en una biblioteca y cuando agregaria directamente la clase en su proyecto  

  Usar bibliotecas facilita al programador funciones que vienen implementadas en la misma, esto hace que no tenga que codificar desde 0 las mismas y solo tenga que preocuparse por usarlas para hacer funcional el programa que esté realizando. Ésto agiliza mucho el proceso de desarrollo de un proyecto y, en general, las bibliiotecas estan diseñadas de forma eficiente y con buenas prácticas de desarrollo.
	- Pondría una clase en una biblioteca cuando crea que pueda usar la misma en varios proyectos, de modo que no tenga que programarla cada vez que la use. En cambio, agregaría directamente la clase al proyecto cuando necesite que la clase tenga un comportamiento algo distinto al que especifiqué en la biblioteca y resultase mas fácil hacerla de 0 que adaptar la misma al proyecto.  

- Como se agrega la referencia a una biblioteca de clase en su proyecto  

	Para agregar una referencia a una biblioteca en un proyecto en Visual Studio, debemos hacer clic derecho en el nodo *Referencias* o *Dependencias* del explorador de soluciones y elegir la opción *Agregar Referencia*. O bien, poddemos hacer clic derecho en el nodo del proyecto y seleccionar *Agregar* > *Referencia*.



  







