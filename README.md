# Examen Tipo Test: Estructuras de Datos I

Este documento contiene 200 preguntas tipo test. Los fragmentos de codigo se muestran en recuadros y las soluciones se encuentran al final.

---

## Bloque 1: Preguntas 1-20
**1. ¿Qué característica define mejor a una estructura de tipo lista según su especificación algebraica?**

A) Acceso únicamente al primer y último elemento

B) Posibilidad de contener elementos de diferentes tipos

C) No tener restricciones de acceso a sus elementos

D) Tener un número fijo de elementos

**2. ¿Cuál es el resultado de esta operación según la especificación del TAD lista?**

```
longitud(+izq(3, +izq(2, [ ])))
```

A) 1

B) 2

C) 3

D) Error de sintaxis

**3. ¿Cuál es el error en este código?**

```cpp
int* datos = new int[100];
//...
delete datos;
```

A) No hay error

B) Falta liberar con delete[]

C) No se inicializa la variable

D) El puntero debería ser void*

**4. ¿Cuál es el comportamiento de seekp(0, ios::end) en un fichero abierto en modo binario?**

A) Lee el último byte del archivo

B) Sitúa el puntero de escritura al inicio del archivo

C) Sitúa el puntero de escritura al final del archivo

D) Elimina el contenido del archivo

**5. ¿Qué operación de la especificación algebraica del TAD pila no está definida para una pila vacía?**

A) vacía?

B) apilar

C) desapilar

D) creaPila

**6. ¿Cuál de estas estructuras requiere más memoria adicional?**

A) Lista estática

B) Lista doblemente enlazada

C) Cola circular

D) Pila sobre vector

**7. ¿Qué error comete este código de listas?**

```cpp
void insertar(TNodoLista* Lista, Tipo_Elemento valor) {
  TNodoLista* NodoNuevo = new TNodoLista;
  NodoNuevo->Datos = valor;
  NodoNuevo->Siguiente = Lista;
  Lista = NodoNuevo;
}
```

A) El puntero Lista no se modifica fuera de la función

B) No se reserva memoria

C) Se accede a memoria no inicializada

D) Falta liberar memoria

**8. ¿Cuál es la función del método Anterior(int i) en una implementación de lista dinámica?**

A) Localiza el nodo i-ésimo

B) Devuelve el nodo siguiente al i-ésimo

C) Devuelve el nodo anterior al i-ésimo

D) Inicializa el nodo i-ésimo

**9. ¿Qué tipo de acceso permite seekg(0, ios::end)?**

A) Escritura directa

B) Posicionamiento de lectura al final del archivo

C) Inserción al principio

D) Lectura secuencial

**10. ¿Cuál de estas implementaciones permite una reducción dinámica de memoria?**

A) Lista sobre vector

B) Lista simplemente enlazada

C) Pila sobre vector sin decremento de tamaño

D) Pila con realloc

**11. ¿Qué instrucción indica si una pila dinámica está vacía?**

A) Tope == 0

B) elementos == NULL

C) n == 0

D) !elementos->Siguiente

**12. ¿Qué característica describe mejor a una lista circular?**

A) Cada nodo apunta a NULL

B) El último nodo apunta al primero

C) Usa índices negativos

D) No permite inserciones al final

**13. ¿Qué ventaja ofrecen las listas enlazadas respecto a las tablas?**

A) Acceso directo por índice

B) Menor complejidad

C) Flexibilidad en inserciones

D) Menor uso de memoria

**14. ¿Qué operador se usa para acceder a miembros de estructuras a través de punteros?**

A) .

B) &

C) ->

D) *.

**15. ¿Cuál es la salida del siguiente código si Valor = 5.0?**

```cpp
float *PValor = &Valor;
cout << *PValor;
```

A) Dirección de Valor

B) 0.0

C) 5.0

D) NULL

**16. ¿Qué define mejor a un TAD genérico?**

A) Solo puede almacenar enteros

B) No puede ser sobrecargado

C) Usa plantillas para admitir múltiples tipos

D) Solo se usa en programación funcional

**17. ¿Qué ocurre al usar delete en un array dinámico?**

A) Libera toda la memoria

B) Solo libera el primer elemento

C) No invoca destructores correctamente

D) Provoca un error de compilación

**18. ¿Cuál es el propósito del método Anterior() en listas genéricas?**

A) Buscar el elemento más reciente

B) Retornar el índice anterior

C) Localizar el nodo anterior a una posición dada

D) Comparar nodos consecutivos

**19. ¿Qué indica cola::esvacia()?**

A) Que fin == inicio

B) Que ne == 0

C) Que inicio == NULL

D) Que no se han escrito datos

**20. ¿Qué error lógico puede causar este código?**

```cpp
ofstream f("datos");
if (!f) { ... }
```

A) Siempre evalúa como falso

B) ofstream no puede usarse así

C) El operador ! no es válido

D) La comprobación está bien

## Bloque 2: Preguntas 21-40
**21. ¿Cuál de estas opciones permite crear un objeto en memoria dinámica e invocar su constructor por defecto?**

A) cliente obj;

B) new cliente();

C) cliente* obj = new cliente;

D) cliente* obj = cliente();

**22. ¿Qué error produce este código al insertar un nodo al principio de una lista?**

```cpp
void insertarInicio(TNodo* Lista, Tipo_Elemento valor) {
  TNodo* NodoNuevo = new TNodo;
  NodoNuevo->Datos = valor;
  NodoNuevo->Siguiente = Lista;
  Lista = NodoNuevo;
}
```

A) El nodo no se inserta correctamente

B) El valor se sobrescribe

C) Se modifica el nodo final

D) No se reserva memoria

**23. ¿Qué operador se usa para obtener la dirección de una variable?**

A) *

B) ->

C) &

D) %

**24. ¿Qué tipo de estructura es ideal para implementar una cola con acceso eficiente en ambos extremos?**

A) Lista simple

B) Lista circular

C) Lista doblemente enlazada

D) Tabla estática

**25. ¿Cuál es la función del método posicion(e) en una lista?**

A) Elimina el elemento e

B) Devuelve la posición del elemento e

C) Inserta el elemento e

D) Retorna el valor del nodo anterior a e

**26. ¿Qué ocurre si usamos ifstream f("archivo.txt"); y f.fail() devuelve true?**

A) El archivo está vacío

B) El archivo está en modo binario

C) El archivo no existe o no se pudo abrir

D) El archivo ya estaba abierto

**27. ¿Qué ventaja tiene el uso de plantillas genéricas?**

A) Menor consumo de memoria

B) Mayor velocidad de ejecución

C) Reutilización de código con distintos tipos

D) No requiere compilación

**28. ¿Qué operación está mal especificada si se ejecuta sobre una pila vacía?**

A) apilar

B) longitud

C) cima

D) vacía?

**29. ¿Qué código crea correctamente un array dinámico de 100 enteros?**

A) int tabla[100];

B) int* tabla = new int;

C) int* tabla = new int[100];

D) tabla = new int;

**30. ¿Cuál es el propósito del método clear() en ficheros C++?**

A) Borrar el fichero

B) Resetear el puntero de lectura

C) Limpiar el contenido de errores lógicos

D) Liberar el buffer

**31. ¿Qué se indica con ofstream salida("datos", ios::app | ios::binary);?**

A) Apertura de un fichero para lectura binaria

B) El fichero será creado si no existe

C) El fichero será truncado

D) Escritura en modo texto desde el final

**32. ¿Cuál es el objetivo de Anterior(i) en la clase TLista genérica?**

A) Acceder al último nodo

B) Retornar un puntero al nodo anterior al índice i

C) Retornar la posición de i

D) Borrar el nodo i

**33. ¿Qué método de la especificación del TAD cola permite observar el primer elemento?**

A) cima

B) primero

C) inicial

D) cabeza

**34. ¿Qué produce este código?**

```cpp
delete [] tabla;
```

A) Elimina solo el primer elemento

B) Elimina un puntero

C) Libera correctamente un array creado con new[]

D) Crea una fuga de memoria

**35. ¿Qué ocurre si usamos tabla++ en un puntero a array dinámico?**

A) Accede al siguiente byte

B) Accede al siguiente elemento

C) Borra el contenido

D) Lanza un error

**36. ¿Qué método de la clase cola decrementa el número de elementos?**

A) esvacia

B) encolar

C) desencolar

D) reset

**37. ¿Qué error produce este código de listas?**

```cpp
Nodo_Ant->Siguiente = Nodo_Aux->Siguiente;
delete Nodo_Aux;
```

A) Acceso ilegal a memoria

B) Borrado correcto de un nodo intermedio

C) Se pierde el puntero a Nodo_Aux

D) Nodo_Ant queda apuntando a NULL

**38. ¿Cuál de estas afirmaciones es verdadera sobre una cola circular?**

A) El puntero fin siempre es menor que inicio

B) El puntero fin vuelve a 0 cuando llega al final

C) No puede llenarse completamente

D) No permite acceso directo

**39. ¿Qué ocurre si en una cola se igualan los índices inicio y fin?**

A) Cola llena

B) Cola vacía

C) Ambiguo: puede ser ambas

D) Error de punteros

**40. ¿Cuál es una solución para evitar que se inserte mal un nodo al inicio con paso por puntero?**

A) Usar un nodo centinela

B) Pasar puntero por referencia o puntero a puntero

C) Usar malloc en lugar de new

D) Evitar listas vacías

## Bloque 3: Preguntas 41-60
**41. ¿Cuál es la finalidad de gcount() en ficheros binarios en C++?**

A) Devuelve la posición actual del cursor

B) Mide la longitud total del archivo

C) Indica cuántos bytes se han leído realmente

D) Cuenta el número de líneas

**42. ¿Qué diferencia principal hay entre delete y delete[]?**

A) delete no puede usarse con punteros

B) delete[] es para arrays y llama a destructores múltiples

C) delete[] elimina solo un elemento

D) Ambas son equivalentes en C++

**43. ¿Qué estructura de lista enlazada tiene nodos que apuntan tanto al anterior como al siguiente?**

A) Lista simplemente enlazada

B) Lista doblemente enlazada

C) Lista circular simple

D) Lista recursiva

**44. ¿Cuál es el comportamiento del siguiente código?**

```cpp
fichero.seekg(0, ios::end);
long tam = fichero.tellg();
```

A) Devuelve 0 si el fichero está vacío

B) Obtiene la cantidad de líneas

C) Calcula el número de bloques

D) Devuelve la posición final: tamaño en bytes

**45. ¿Qué condición permite eliminar correctamente el primer nodo en una lista doblemente enlazada?**

A) El nodo tiene más de un hijo

B) El puntero Anterior del segundo nodo debe actualizarse a NULL

C) No debe apuntar a NULL

D) Solo se actualiza el puntero de cabecera

**46. En el TAD pila especificado algebraicamente, ¿qué patrón representa cualquier pila con al menos un elemento?**

A) creaPila

B) apilar(p, e)

C) desapilar(p)

D) longitud(p)

**47. ¿Qué implementación es más adecuada para una pila con necesidad de crecer dinámicamente?**

A) Array estático

B) Vector con incremento

C) Lista enlazada

D) Lista circular

**48. ¿Qué problema puede surgir al pasar objetos por valor a funciones en C++?**

A) No se copia el contenido

B) No se puede acceder a sus métodos

C) Se invoca el destructor y se pierde la memoria dinámica compartida

D) Se pasa la dirección en lugar del valor

**49. ¿Qué método permite escribir directamente sobre una posición concreta en un fichero binario?**

A) write()

B) seekp()

C) open()

D) flush()

**50. ¿Qué elemento define en una plantilla genérica el tipo de datos a usar?**

A) #define

B) class o typename dentro de template<>

C) auto

D) typeid

**51. ¿Cuál es la salida del siguiente fragmento si Dato = 400?**

```cpp
void Multiplica(float* PDatos) {
  *PDatos = *PDatos * 2;
}
int main() {
  float Dato = 400;
  Multiplica(&Dato);
  cout << Dato;
}
```

A) 800

B) 400

C) Dirección de memoria

D) Error en compilación

**52. ¿Qué ocurre si no se establece elementos = NULL después de borrar todos los nodos de una lista?**

A) No afecta

B) Se libera memoria

C) El puntero apunta a memoria liberada

D) El programa se compila pero no enlaza

**53. ¿Qué resultado produce el siguiente código?**

```cpp
int* v = new int[3]{1, 2, 3};
v++;
cout << *v;
```

A) 1

B) 2

C) Error

D) Dirección de memoria

**54. ¿Qué operador permite acceder a campos de una estructura a través de un puntero?**

A) .

B) *

C) ->

D) &

**55. ¿Qué condición permite realizar eliminar(i) en una lista según su especificación algebraica?**

A) i = longitud(l)

B) 1 ≤ i ≤ longitud(l)

C) i > longitud(l)

D) i == 0

**56. ¿Qué es una cola de prioridad?**

A) Una cola normal ordenada por inserción

B) Cola que encola siempre por el frente

C) Cola donde se elige el siguiente elemento según un criterio de prioridad

D) Cola circular que nunca se llena

**57. ¿Qué significa que Gen(g) sea un conjunto no libre?**

A) Que no se puede construir ningún valor válido

B) Que todas las operaciones son equivalentes

C) Que diferentes términos generadores producen el mismo valor

D) Que el género no tiene observadores

**58. ¿Qué ocurre al usar strcmp(s1, s2) > 0 en una función genérica especializada para cadenas?**

A) Se invierte el orden

B) Devuelve true si s1 es mayor que s2

C) Devuelve false si son iguales

D) Produce un error con punteros

**59. ¿Qué ventaja aporta declarar un método insertar() dentro de un template<class T>?**

A) Evita uso de new

B) Solo sirve para enteros

C) Permite reutilizar el método con distintos tipos de datos

D) El método es estático

**60. ¿Cuál es el comportamiento esperado de la función esvacia() en una clase genérica de lista?**

A) Devuelve la dirección del primer nodo

B) Devuelve true si elementos == NULL o n == 0

C) Elimina todos los nodos

D) Devuelve el tamaño máximo

## Bloque 4: Preguntas 61-80
**61. ¿Qué indica Tope == -1 en una pila implementada con array?**

A) Que hay un error de desbordamiento

B) Que la pila está llena

C) Que la pila está vacía

D) Que hay un único elemento

**62. ¿Qué diferencia hay entre ofstream y fstream?**

A) ofstream solo escribe; fstream puede leer y escribir

B) ofstream solo funciona con texto

C) fstream no permite modos binarios

D) No hay diferencia práctica

**63. En listas dinámicas, ¿qué condición permite recorrer la lista hasta el final?**

A) Nodo_Aux != NULL

B) Nodo_Aux->Siguiente == NULL

C) Nodo_Aux == NULL

D) Nodo_Aux->Anterior == NULL

**64. ¿Qué permite template<class T> en la definición de una clase en C++?**

A) Crear múltiples clases en un solo archivo

B) Heredar clases de distintos tipos

C) Declarar una clase genérica para cualquier tipo T

D) Evitar el uso de punteros

**65. ¿Cuál de estas instrucciones libera correctamente un array dinámico de objetos?**

A) delete array;

B) free(array);

C) delete [] array;

D) array = NULL;

**66. ¿Qué se indica con vacía?(creaCola) = verdad en la especificación algebraica?**

A) Que la cola siempre está vacía

B) Que una cola recién creada no tiene elementos

C) Que todas las colas tienen elementos

D) Que la cola es infinita

**67. ¿Qué tipo de acceso permiten las funciones seekg() y seekp()?**

A) Solo acceso secuencial

B) Acceso directo a posiciones de lectura y escritura

C) Modificación simultánea de múltiples archivos

D) Acceso aleatorio a variables

**68. ¿Cuál es la operación correcta para eliminar el primer nodo de una lista simple enlazada?**

```cpp
Nodo_Aux = elementos;
elementos = Nodo_Aux->Siguiente;
delete Nodo_Aux;
```

A) No elimina nada

B) Elimina el último nodo

C) Elimina correctamente el primero

D) Borra toda la lista

**69. ¿Qué operador se usa para declarar un puntero en C++?**

A) &

B) *

C) ->

D) ::

**70. ¿Qué condición permite insertar un nodo al principio de una lista circular doblemente enlazada?**

A) El nodo anterior del primer nodo debe ser NULL

B) No se permite en listas circulares

C) El nuevo nodo apunta al actual y el anterior del actual se actualiza

D) No se actualiza el puntero de fin

**71. ¿Qué error lógico produce pasar un objeto como parámetro sin constructor de copia adecuado?**

A) Compila pero no ejecuta

B) Se elimina su memoria dinámica compartida al salir del método

C) Se bloquea el sistema

D) Se crean múltiples copias del objeto

**72. ¿Qué ocurre al ejecutar cola::encolar(e) cuando la cola dinámica está llena?**

A) Produce error

B) Se duplica el elemento

C) Se redimensiona la cola dinámicamente

D) Pierde el puntero fin

**73. ¿Cuál es el patrón generador mínimo para el TAD pila?**

A) cima

B) creaPila

C) apilar(p, e)

D) Ambas B y C

**74. ¿Qué propiedad se cumple para la operación insertar(l, i, e) según su dominio de definición?**

A) Solo es válida si i > longitud(l)

B) Solo es válida si 1 ≤ i ≤ longitud(l)+1

C) Solo si i == 1

D) Es total, siempre está definida

**75. ¿Cuál es la principal ventaja de las listas circulares frente a las simplemente enlazadas?**

A) No usan memoria

B) Pueden acceder al primer nodo desde el último directamente

C) Son más fáciles de implementar

D) Solo se usan en TADs genéricos

**76. ¿Qué ocurre si no se usa el método Anterior() al insertar en posición intermedia?**

A) El nodo se inserta al principio

B) Se pierde el enlace previo

C) Se reemplaza el nodo anterior

D) No compila

**77. ¿Cómo se puede evitar un error al liberar una lista dinámica con paso por puntero?**

A) Usando un puntero local

B) Usando paso por puntero a puntero

C) Eliminando solo el último nodo

D) No se puede evitar

**78. ¿Qué ventaja tiene una implementación con nodos frente a tablas dinámicas en TAD pila?**

A) Mejor acceso por índice

B) Menor complejidad

C) Reducción de uso de punteros

D) Mayor eficiencia y menor uso de memoria para operaciones frecuentes

**79. ¿Qué resultado devuelve esta especificación?**

```algebra
pos(e1, +izq(e2, l)) = si e1 == e2 entonces 1
                       sino suc(pos(e1, l))
```

A) Siempre devuelve 1

B) Si e1 no está, devuelve -1

C) Devuelve la posición del elemento e1

D) Es una operación total

**80. ¿Qué ocurre al ejecutar desencolar() en una cola dinámica vacía?**

A) Elimina NULL

B) Puede liberar memoria no válida

C) La operación está indefinida

D) Se reinicia el puntero fin

## Bloque 5: Preguntas 81-100
**81. ¿Qué ocurre si se invoca modificar(i, e) cuando i > longitud de la lista?**

A) Se inserta al final

B) Se sobrescribe el último nodo

C) La operación no está definida

D) Se borra el nodo anterior

**82. ¿Qué estructura es más eficiente para implementar una pila en cuanto a coste de operaciones y memoria?**

A) Lista doblemente enlazada

B) Array con tamaño fijo

C) Lista simplemente enlazada

D) Lista circular

**83. ¿Qué instrucción permite averiguar el tamaño de un archivo binario en bytes?**

A) ifstream.tellg()

B) seekp(0)

C) seekg(0, ios::end); tellg();

D) gcount()

**84. ¿Qué operador permite acceder al campo Edad de un objeto Cliente apuntado por PCli?**

A) PCli::Edad

B) *PCli.Edad

C) PCli->Edad

D) PCli*.Edad

**85. ¿Qué propiedad caracteriza a la operación desapilar en la especificación algebraica de una pila?**

A) Es una operación total

B) Es generadora

C) Es parcial y solo válida si la pila no está vacía

D) No modifica la pila

**86. ¿Qué significa que una lista esté vacía en C++ usando punteros?**

A) elementos == elementos

B) elementos == 0

C) elementos == NULL

D) elementos == -1

**87. ¿Qué ocurre al intentar acceder a tabla[100] si tabla fue creado con new int[100]?**

A) Accede al último elemento

B) Accede a una posición no definida

C) Lanza una excepción automáticamente

D) Es equivalente a tabla[-1]

**88. ¿Qué hace seekp(0, ios::end)?**

A) Coloca el puntero de escritura al inicio

B) Cierra el archivo

C) Posiciona el puntero de escritura al final del archivo

D) Lee desde el final

**89. ¿Qué propiedad cumple la operación concatenar(l1, l2)?**

A) Solo se puede aplicar entre listas vacías

B) Devuelve la longitud máxima

C) Añade los elementos de l2 al final de l1

D) Reemplaza los valores de l1 por los de l2

**90. ¿Qué permite una cola circular frente a una estática lineal?**

A) Acceso aleatorio a posiciones

B) Aumentar la eficiencia del espacio disponible

C) Reutilizar memoria con punteros dobles

D) Apilar elementos en ambas direcciones

**91. ¿Qué condición se debe verificar antes de usar Nodo_Aux->Siguiente?**

A) Nodo_Aux == NULL

B) Nodo_Aux != NULL

C) Nodo_Aux == 0

D) Nodo_Aux->Siguiente != 0

**92. ¿Cuál es el propósito del método Anterior(int i) en una lista genérica?**

A) Obtener el nodo i

B) Obtener el nodo anterior a i

C) Insertar un nodo en i

D) Buscar el valor máximo

**93. ¿Qué tipo de error se evita usando paso por puntero a puntero en funciones que modifican listas?**

A) Pérdida de memoria

B) Escritura fuera de rango

C) Que los cambios no se reflejen fuera de la función

D) Que se modifique la lista original

**94. ¿Qué ocurre si no se usa delete[] con arrays dinámicos?**

A) Se invoca el destructor igualmente

B) No hay diferencia

C) Solo se libera parcialmente la memoria

D) Se produce una fuga de memoria

**95. ¿Cuál es el objetivo de la clase TLista<T>?**

A) Crear listas de enteros exclusivamente

B) Implementar listas genéricas para cualquier tipo de datos

C) Definir listas para tipos primitivos únicamente

D) Encapsular operaciones de vectores

**96. ¿Qué garantiza template<class T> cuando se aplica correctamente en una función?**

A) Que solo funcione con enteros

B) Que se pueda usar la función con cualquier tipo

C) Que se optimice la ejecución

D) Que se genere una sola instancia del código

**97. ¿Cuál es la operación más costosa en una lista implementada como array estático?**

A) Insertar al final

B) Leer en una posición concreta

C) Insertar al principio

D) Borrar el último elemento

**98. ¿Qué ocurre con el método observar(i) si i está fuera del rango de la lista?**

A) Devuelve NULL

B) Devuelve el último elemento

C) La operación está indefinida

D) Crea un nuevo nodo

**99. ¿Qué representa +dch(l, e) en la especificación algebraica de listas?**

A) Inserción por la izquierda

B) Concatenación

C) Inserción por la derecha

D) Reemplazo del primer elemento

**100. ¿Qué ocurre si el constructor de copia de una clase no está bien definido y se pasa el objeto por valor?**

A) Se copia parcialmente

B) No se puede compilar

C) Se destruye la memoria dinámica compartida

D) Se duplica el puntero

## Bloque 6: Preguntas 101-120
**101. ¿Qué ocurre si se aplica delete a un puntero que ya ha sido liberado sin asignarlo a NULL?**

A) El compilador lo detecta

B) Se vuelve a liberar correctamente

C) Puede producir un error en tiempo de ejecución

D) El valor se conserva

**102. ¿Qué tipo de acceso tiene una lista enlazada simple?**

A) Directo

B) Aleatorio

C) Secuencial

D) Circular

**103. ¿Qué permite la sobrecarga de plantillas?**

A) Usar variables globales

B) Definir múltiples versiones genéricas de una misma función

C) Hacer casting automático

D) Definir clases abstractas

**104. ¿Qué método permite acceder al primer elemento de una cola genérica?**

A) ultimo()

B) inicio()

C) primero()

D) frente()

**105. ¿Qué condición debe cumplirse para eliminar un nodo intermedio en una lista doblemente enlazada?**

A) El nodo anterior debe ser NULL

B) El nodo siguiente debe ser NULL

C) Actualizar ambos enlaces: anterior y siguiente

D) No se puede eliminar nodos intermedios

**106. ¿Qué representa este fragmento algebraico?**

```algebra
+dch([ ], e) = +izq(e, [ ])
```

A) Inserción por la izquierda y por la derecha son equivalentes en listas vacías

B) Se elimina el nodo

C) Se concatena

D) Se modifica el nodo

**107. ¿Qué ocurre con el array dinámico int* a = new int[10]; si luego se hace delete a;?**

A) Se libera completamente

B) Solo se libera el primer elemento

C) Provoca pérdida de memoria

D) Se borra con delete[] automáticamente

**108. ¿Qué clase de operaciones se definen como “observadoras” en especificaciones algebraicas?**

A) Las que devuelven un valor del mismo tipo

B) Las que modifican el TAD

C) Las que devuelven un valor de tipo distinto al género

D) Las que construyen el TAD

**109. ¿Qué ventaja tiene una lista con nodo cabecera?**

A) No necesita constructor

B) Permite múltiples accesos directos

C) Evita problemas en inserciones/eliminaciones en la primera posición

D) Es más rápida al recorrer

**110. ¿Cuál es el significado de esta ecuación en el TAD pila?**

```algebra
desapilar(apilar(p, e)) = p
```

A) La pila se duplica

B) La operación es no determinista

C) Se deshace la última inserción

D) El valor se mantiene

**111. ¿Qué permite la palabra reservada typename en una plantilla?**

A) Declarar una clase derivada

B) Es sinónimo de class para tipos genéricos

C) Crear punteros

D) Definir variables locales

**112. ¿Qué propiedad se cumple en cima(apilar(p, e)) = e?**

A) El elemento insertado queda en el fondo

B) El último elemento insertado está en la cima

C) No se puede observar la cima

D) El valor e se pierde

**113. ¿Qué representa ++ en la operación genérica sobre secuencias?**

A) Borrado

B) Concatenación

C) Modificación

D) Inversión

**114. ¿Cuál es el comportamiento de este fragmento?**

```cpp
TLista<float> l;
l.insertar(1, 3.14);
cout << l.observar(1);
```

A) Error de compilación

B) Muestra 0.0

C) Muestra 3.14

D) Se sale de rango

**115. ¿Qué se necesita para usar strcmp en una plantilla especializada para cadenas?**

A) Definir el operador <

B) Declarar los strings como char*

C) Incluir <cstring>

D) Ambas B y C

**116. ¿Qué error lógico produce este código si fichas no está en modo binario?**

```cpp
salida.write((char*)fichas, 3*sizeof(ficha));
```

A) No escribe los datos correctamente

B) Da error de compilación

C) No se puede compilar sin casting

D) Es idéntico a uso en texto

**117. ¿Cuál es la condición de parada para buscar en una lista circular?**

A) Nodo == NULL

B) Nodo->Siguiente == NULL

C) Nodo == inicio o se cumple condición

D) Nodo == fin

**118. ¿Qué operación devuelve el número de nodos en una lista genérica?**

A) longitud()

B) tam()

C) dimension()

D) contar()

**119. ¿Qué ocurre si se elimina una lista dinámica sin liberar su memoria?**

A) El programa se detiene

B) Se destruye automáticamente

C) Se genera una fuga de memoria

D) Se reemplaza por NULL

**120. ¿Qué estructura permite inserción por un extremo y eliminación por otro?**

A) Pila

B) Lista circular

C) Cola

D) Árbol

## Bloque 7: Preguntas 121-140
**121. ¿Qué propiedad debe cumplir la operación eliminar(l, i) según su dominio de definición?**

A) 1 ≤ i ≤ longitud(l)

B) i < 1

C) i = 0

D) i ≥ longitud(l)

**122. ¿Cuál es el resultado de evaluar izq(+izq(e, l))?**

A) l

B) e

C) Elimina el primer nodo

D) Inserta al final

**123. ¿Qué ocurriría si en una cola circular no se lleva un contador de elementos?**

A) Nunca se llena

B) No se puede saber si está vacía o llena

C) Se pierden elementos

D) Es más eficiente

**124. ¿Qué especifica vacía?(apilar(p, e)) = falso?**

A) Que una pila con un elemento no está vacía

B) Que una pila vacía no se puede apilar

C) Que siempre es vacía

D) Que apilar no modifica la pila

**125. ¿Qué significa la operación l[i] en la especificación algebraica?**

A) Inserta un elemento en la posición i

B) Observa el elemento i-ésimo

C) Devuelve una lista con un solo elemento

D) Elimina el elemento i

**126. ¿Cuál es una desventaja del uso de listas estáticas?**

A) Acceso lento a los elementos

B) No permite acceso por índice

C) Desperdicio de memoria si no se llena completamente

D) Es difícil implementar inserciones

**127. ¿Qué ocurre en una pila enlazada cuando se desapila?**

A) Se borra el nodo final

B) Se borra el primer nodo y se actualiza el puntero

C) Se borra toda la pila

D) Se reordena la memoria

**128. ¿Cuál es la salida del siguiente código?**

```cpp
int a = 3, b = 7;
cout << mayor(a, b);  // usando una plantilla genérica
```

A) 3

B) 7

C) Error de compilación

D) Depende del sistema

**129. ¿Qué requiere una clase TAD genérica en su fichero de cabecera?**

A) Métodos estáticos

B) Implementación inline

C) Definición de métodos en el .h (no en .cpp)

D) Uso exclusivo de arrays

**130. ¿Qué define una función generadora?**

A) Una operación de entrada/salida

B) Una operación que devuelve un valor del mismo género

C) Una operación que consulta datos

D) Una función que modifica el tipo

**131. ¿Qué condición se cumple en desapilar(creaPila)?**

A) Está definido

B) Devuelve el mismo valor

C) No está definido (es parcial)

D) Elimina un nodo

**132. ¿Qué condición es necesaria para usar modificar(l, i, e)?**

A) Que la lista esté vacía

B) i = longitud(l)

C) 1 ≤ i ≤ longitud(l)

D) i = 0

**133. ¿Qué ventaja tienen las listas con nodos respecto a tablas dinámicas?**

A) Mejor acceso por índice

B) Uso constante de memoria

C) Capacidad de crecer sin necesidad de reubicar memoria

D) Uso menor de punteros

**134. ¿Qué función cumple Anterior(i) en la implementación de insertar(i, e)?**

A) Devuelve el siguiente nodo

B) Devuelve el nodo i

C) Localiza el nodo previo para enlazar el nuevo nodo

D) Modifica el valor i

**135. ¿Cuál es el contenido de la pila tras las siguientes operaciones?**

```algebra
p1 = apilar(creaPila, 5)
p2 = apilar(p1, 8)
cima(p2)
```

A) 5

B) 8

C) 0

D) Error

**136. ¿Qué ocurriría si se ejecuta eliminar(1) sobre una lista vacía?**

A) Borra toda la lista

B) Inserta un elemento

C) Provoca un comportamiento indefinido

D) Está fuera del dominio de definición

**137. ¿Cuál es la condición de fin para destruir una lista dinámica?**

A) Nodo->Siguiente == NULL

B) Nodo == NULL

C) Nodo->Anterior == NULL

D) Nodo->Datos == 0

**138. ¿Qué ocurre al ejecutar delete Nodo_Borr si Nodo_Borr == NULL?**

A) Error de compilación

B) Se libera correctamente

C) No pasa nada (seguro en C++)

D) El programa se detiene

**139. ¿Qué operador permite construir objetos dinámicos invocando su constructor?**

A) malloc()

B) &

C) new

D) constructor()

**140. ¿Cuál es la principal diferencia entre read() y >> en lectura de archivos?**

A) read() solo funciona en texto

B) >> es binario

C) read() permite lectura binaria con control de bytes

D) >> necesita casting

## Bloque 8: Preguntas 141-160
**141. ¿Qué ocurre si en una lista simplemente enlazada se olvida actualizar el puntero del nodo anterior al eliminar un nodo intermedio?**

A) La lista se ordena

B) Se crea un ciclo

C) Se pierde el acceso al resto de la lista

D) No se modifica la lista

**142. ¿Qué operador se utiliza en C++ para acceder al miembro de un objeto apuntado por un puntero?**

A) *.

B) ->

C) ::

D) .

**143. ¿Qué condición define una función como modificadora en una especificación algebraica?**

A) Devuelve un valor del mismo género y no pertenece al conjunto generador

B) Devuelve un valor de género distinto

C) No modifica el estado

D) Solo se aplica a enteros

**144. ¿Qué ocurre al aplicar desencolar() cuando la cola dinámica está vacía?**

A) Se reordena la cola

B) La operación no está definida

C) Se borra el primer nodo

D) Se reinicia la cola

**145. ¿Qué ocurre con la memoria si se llama delete sobre un puntero no inicializado?**

A) Se libera correctamente

B) Se ignora

C) Puede producir comportamiento indefinido

D) Se reinicia el puntero

**146. ¿Qué ventaja ofrece la implementación con listas enlazadas frente a tablas?**

A) Mejor acceso por índice

B) Menor uso de punteros

C) Posibilidad de insertar y eliminar sin mover elementos

D) Mayor eficiencia en búsquedas binarias

**147. ¿Qué tipo de puntero se usa para pasar la dirección de un puntero a una función?**

A) Puntero doble **

B) Puntero constante

C) Referencia &

D) Puntero void

**148. ¿Qué ocurre al usar seekg(pos) en un fichero?**

A) Se borra el contenido

B) Se posiciona el puntero de lectura en la posición indicada

C) Se crea un nuevo fichero

D) Se actualiza el buffer

**149. ¿Qué función algebraica indica si una pila está vacía?**

A) vacia?()

B) longitud()

C) esvacia()

D) cima()

**150. ¿Cuál es el propósito del método gcount()?**

A) Contar líneas de un fichero

B) Obtener el tamaño del archivo

C) Devolver cuántos bytes se leyeron en la última operación binaria

D) Estimar la memoria ocupada por una variable

**151. ¿Cuál es el valor de longitud(+izq(3, +izq(5, [ ])))?**

A) 0

B) 1

C) 2

D) 3

**152. ¿Qué característica tiene una lista circular doblemente enlazada?**

A) El último nodo apunta a NULL

B) Se recorre en un único sentido

C) El último nodo apunta al primero, y viceversa

D) No permite inserciones al principio

**153. ¿Qué ocurre si se accede a array[-1] en C++?**

A) Devuelve el primer valor

B) Lanza una excepción

C) Accede a memoria fuera del array (error lógico)

D) Devuelve 0

**154. ¿Qué define mejor a un TAD?**

A) Es un algoritmo

B) Es una clase concreta

C) Es un modelo abstracto de datos con operaciones definidas algebraicamente

D) Es una estructura estática

**155. ¿Qué ocurre al insertar un nodo al principio de una lista circular simple?**

A) No se actualiza el puntero fin

B) Se rompe la circularidad

C) Se deben actualizar los punteros del último nodo

D) Solo se actualiza el primer nodo

**156. ¿Qué propiedad caracteriza a una pila?**

A) FIFO

B) LIFO

C) FILO

D) LILO

**157. ¿Qué se obtiene al ejecutar TLista<int> lista; lista.longitud(); justo tras crearla?**

A) 0

B) 1

C) NULL

D) -1

**158. ¿Qué se logra con fichero.clear();?**

A) Borra el contenido del archivo

B) Cierra el fichero

C) Elimina los flags de error de lectura/escritura

D) Vacía el buffer de memoria

**159. ¿Qué propiedad tiene el conjunto Gen(g) si es libre?**

A) Genera un número finito de términos

B) Todos los términos construidos con generadoras son distintos

C) Permite alias de elementos

D) Genera términos redundantes

**160. ¿Qué permite la palabra clave template<class T> en C++?**

A) Crear clases abstractas

B) Reutilizar código con distintos tipos

C) Sobrecargar operadores

D) Crear subclases automáticamente

## Bloque 9: Preguntas 161-180
**161. ¿Qué ocurre si se usa new para reservar un objeto pero nunca se llama a delete?**

A) El compilador lo corrige

B) El objeto se elimina al final del programa

C) Se produce una fuga de memoria

D) Se lanza una excepción

**162. ¿Qué valor devuelve la función posicion(e) si e no está en la lista?**

A) 0

B) -1

C) longitud de la lista

D) 1

**163. ¿Cuál de los siguientes es un constructor generador en el TAD pila?**

A) creaPila

B) desapilar

C) longitud

D) cima

**164. ¿Qué ocurre si se llama delete[] sobre un puntero que no fue creado con new[]?**

A) Se libera correctamente

B) Puede generar comportamiento indefinido

C) Da error de compilación

D) Lo convierte en NULL

**165. ¿Cuál es el propósito de la función anadirDch(e) en listas?**

A) Eliminar el último elemento

B) Reemplazar el primero

C) Insertar el elemento al final

D) Ordenar la lista

**166. ¿Qué ocurre al recorrer una lista circular con condición Nodo->Siguiente != elementos?**

A) No termina nunca

B) No recorre todos los nodos

C) Recorre todos excepto el primero

D) Recorre todos menos el último

**167. ¿Qué ocurre si observar(i) se ejecuta con i > longitud()?**

A) Devuelve NULL

B) Lanza excepción

C) Comportamiento indefinido

D) Está fuera del dominio de definición

**168. ¿Qué ventaja ofrece una cola dinámica frente a una implementada con array?**

A) Acceso directo por índice

B) Requiere menos código

C) Permite crecer sin límite fijo

D) Permite acceso en ambos extremos

**169. ¿Qué ocurre si se usa ifstream para abrir un archivo y se intenta escribir en él?**

A) Se escribe correctamente

B) Se lanza error de compilación

C) No se escribe nada

D) El archivo se borra

**170. ¿Qué representa esta plantilla de clase?**

```cpp
template <class T>
class Pila {
  T elementos[100];
};
```

A) Clase que solo almacena enteros

B) Clase que almacena elementos de cualquier tipo

C) Clase abstracta

D) Clase derivada

**171. ¿Qué ocurre si seekp(pos) apunta fuera del tamaño actual del archivo?**

A) Se amplía el archivo automáticamente

B) Se lanza una excepción

C) El puntero se reinicia

D) Da error de compilación

**172. ¿Qué hace el destructor de una pila dinámica correctamente implementada?**

A) Elimina el primer nodo

B) Libera todos los nodos

C) Borra los datos pero deja los punteros

D) Cierra el programa

**173. ¿Cuál es el resultado de aplicar insertar(1, e) en una lista vacía?**

A) Error

B) Inserta e como único nodo

C) Elimina el nodo anterior

D) Lo coloca al final

**174. ¿Qué tipo de estructura necesita dos punteros: Inicio y Fin?**

A) Pila

B) Cola

C) Lista simple

D) Vector

**175. ¿Qué se debe hacer tras liberar todos los nodos de una lista?**

A) Nada más

B) Inicializar elementos = NULL

C) Insertar NULL en cada nodo

D) Aplicar realloc

**176. ¿Qué especifica fespec en las especificaciones algebraicas?**

A) Que es una función recursiva

B) Que es una especificación formal

C) Que la especificación está cerrada y completa

D) Que se trata de una clase abstracta

**177. ¿Cuál es la operación correcta para insertar un nodo en una lista doblemente enlazada en posición intermedia?**

A) Solo se enlaza al anterior

B) Solo se enlaza al siguiente

C) Se enlaza al anterior y al siguiente

D) Se reemplaza el nodo siguiente

**178. ¿Cuál es el principal riesgo de no verificar que new devuelve distinto de NULL?**

A) No se reserva memoria

B) Se reserva memoria dos veces

C) Se lanza una excepción

D) Nada, C++ lo maneja automáticamente

**179. ¿Qué tipo de archivo permite acceder a una posición concreta sin recorrer todo el contenido?**

A) Archivo de texto

B) Archivo secuencial

C) Archivo con acceso directo

D) Archivo lógico

**180. ¿Qué ocurre si Inicio == NULL y Fin != NULL en una cola dinámica?**

A) Cola vacía

B) Inconsistencia grave

C) Cola con un único nodo

D) Error de compilación

## Bloque 10: Preguntas 181-200
**181. ¿Qué valor devuelve la operación longitud(creaPila) en la especificación algebraica?**

A) 1

B) 0

C) -1

D) indefinido

**182. ¿Qué se necesita para insertar un nodo en una lista circular simplemente enlazada al principio?**

A) Solo actualizar elementos

B) Que la lista esté vacía

C) Actualizar elementos y el Siguiente del último nodo

D) Eliminar el nodo anterior

**183. ¿Qué representa la especificación insertar(l, i, e) cuando l está vacía?**

A) Devuelve una lista vacía

B) Es indefinido

C) Inserta e en la primera posición

D) Requiere dos inserciones previas

**184. ¿Qué operación permite insertar un elemento al inicio de una pila enlazada?**

A) anadirDch()

B) pushFront()

C) apilar()

D) insertar(1, e)

**185. ¿Qué ocurre si se ejecuta eliminarIzq() en una lista vacía?**

A) Se elimina NULL

B) No está definida la operación

C) Devuelve el primer elemento

D) Se reinicia la lista

**186. ¿Qué hace la función esvacia() en una pila dinámica?**

A) Devuelve la cima

B) Comprueba si el puntero elementos es NULL

C) Borra todos los nodos

D) Siempre devuelve false

**187. ¿Qué se necesita para insertar un nodo entre dos existentes en una lista doble?**

A) Un solo puntero

B) Dos punteros y actualizar 3 enlaces

C) Solo el nodo anterior

D) Solo el nodo siguiente

**188. ¿Qué ocurre si Inicio == Fin == NULL en una cola dinámica?**

A) Cola llena

B) Cola vacía

C) Error de puntero

D) Cola circular

**189. ¿Qué ocurre si un objeto genérico se pasa por valor y luego se destruye?**

A) Nada, se copia todo correctamente

B) Puede eliminar la memoria compartida con el original

C) Se crea una copia independiente

D) Se destruye solo el puntero

**190. ¿Qué condición permite recorrer una lista hasta el nodo anterior al actual?**

A) Nodo_Aux->Siguiente == Nodo_Act

B) Nodo_Aux == Nodo_Act

C) Nodo_Aux->Anterior == Nodo_Act

D) Nodo_Act == NULL

**191. ¿Qué operador se debe usar en una función genérica que recibe arrays?**

A) *

B) []

C) &

D) Ninguno, se usa TIPO[] en los parámetros

**192. ¿Qué implica usar ios::app al abrir un fichero?**

A) Se borra el contenido anterior

B) Se abre en modo binario

C) Se escribe solo al final del archivo

D) Solo se puede leer

**193. ¿Cuál es el resultado de la operación -dch(+izq(e, [ ]))?**

A) []

B) [e]

C) Error

D) NULL

**194. ¿Qué función recorre una lista buscando la posición donde insertar un nuevo nodo ordenado?**

A) insertarOrdenado()

B) Anterior()

C) buscar()

D) Nodo_Tmp = Nodo_Tmp->Siguiente dentro de un bucle

**195. ¿Qué tipo de error puede surgir al pasar un array como puntero a una función sin verificar el tamaño?**

A) Error de compilación

B) Desbordamiento de memoria

C) Acceso fuera de rango

D) B y C son correctas

**196. ¿Qué representa el tipo Cadena en las implementaciones de pila/cola del temario?**

A) Un alias para string

B) Una clase definida en otro fichero

C) Un array de char

D) Una estructura personalizada

**197. ¿Qué ocurre al usar delete Nodo_Aux dentro de un bucle que recorre una lista?**

A) Se elimina solo el primer nodo

B) Se eliminan todos correctamente si se actualiza el puntero

C) Da error de compilación

D) Se elimina el último nodo repetidamente

**198. ¿Qué función recorre una lista para buscar un nodo con un valor dado?**

A) insertar()

B) eliminar()

C) pertenece() o posicion()

D) modificar()

**199. ¿Qué ocurre si el nodo auxiliar se destruye antes de actualizar el puntero principal?**

A) Se pierde acceso al resto de la lista

B) No afecta a la lógica

C) Se recupera en el siguiente ciclo

D) Se vuelve a inicializar

**200. ¿Qué representa la instrucción Inicio = Fin = NULL; en una cola dinámica?**

A) Eliminación lógica de todos los nodos

B) Reinicialización de la cola vacía

C) Error de punteros

D) Finalización del recorrido

---

## Soluciones
1. C. Las listas son estructuras ordenadas sin restricciones en la localización de inserción o borrado de elementos [Tema 3, pág. 4].
2. B. Cada operación +izq incrementa en uno la longitud [Tema 3, pág. 6].
3. B. Los arrays creados con new[] deben liberarse con delete[] [Tema 1.1, pág. 7].
4. C. seekp posiciona el puntero de escritura al final [Tema 1.2, pág. 16].
5. C. desapilar es parcial y no está definida para pilas vacías [Tema 3, pág. 18].
6. B. Requiere almacenamiento de dos punteros por nodo [Tema 4, pág. 7].
7. A. Lista se pasa por valor y no modifica a la original [Tema 4, pág. 40].
8. C. Anterior devuelve el nodo anterior al i-ésimo [Tema 4, pág. 21].
9. B. seekg coloca el puntero de lectura al final [Tema 1.2, pág. 16].
10. B. La lista enlazada permite liberar nodos individualmente [Tema 4, pág. 31].
11. B. La pila vacía se indica con elementos == NULL [Tema 4, pág. 27].
12. B. El último nodo apunta al primero [Tema 4, pág. 7].
13. C. Permiten insertar o eliminar sin desplazamientos [Tema 4, pág. 2].
14. C. El operador -> accede a miembros apuntados [Tema 1.1, pág. 5].
15. C. *PValor vale 5.0 [Tema 1.1, pág. 5].
16. C. Los TAD genéricos se implementan con plantillas [Tema 5, pág. 2].
17. C. delete no invoca destructores correctamente en arrays [Tema 1.1, pág. 7].
18. C. Devuelve un puntero al nodo anterior [Tema 5, pág. 10].
19. B. esvacia() devuelve true si ne == 0 [Tema 4, pág. 38].
20. D. !f verifica correctamente la apertura [Tema 1.2, pág. 12].
21. C. Se crea un objeto dinámicamente con new [Tema 1.1, pág. 7].
22. A. La inserción no modifica el puntero original [Tema 4, pág. 40].
23. C. El operador & obtiene direcciones [Tema 1.1, pág. 4].
24. C. La lista doblemente enlazada permite acceso eficiente [Tema 4, pág. 7].
25. B. Devuelve la posición del elemento o -1 [Tema 3, pág. 6].
26. C. fail() indica error en la apertura [Tema 1.2, pág. 12].
27. C. Reutilización de código con distintos tipos [Tema 5, pág. 3].
28. C. cima no está definida para pila vacía [Tema 3, pág. 18].
29. C. new int[100] crea el array [Tema 1.1, pág. 6].
30. C. clear() limpia el estado de error del stream [Tema 1.2, pág. 12].
31. B. ios::app añade al final y crea si no existe [Tema 1.2, pág. 11].
32. B. Devuelve el nodo anterior al índice i [Tema 5, pág. 9].
33. B. primero devuelve el elemento de la cabecera [Tema 3, pág. 27].
34. C. delete[] libera correctamente un array [Tema 1.1, pág. 7].
35. B. Incrementa el puntero al siguiente elemento [Tema 1.1, pág. 8].
36. C. desencolar decrementa ne [Tema 4, pág. 37].
37. B. Es la forma correcta de eliminar un nodo intermedio [Tema 4, pág. 18].
38. B. El puntero fin vuelve a 0 al llegar al final [Tema 4, pág. 31].
39. C. Puede significar cola vacía o llena [Tema 3, pág. 30].
40. B. Se debe pasar puntero por referencia (**) [Tema 4, pág. 41].
41. C. gcount() indica los bytes leídos [Tema 1.2, pág. 15].
42. B. delete[] es para arrays y llama a los destructores [Tema 1.1, pág. 7].
43. B. Lista doblemente enlazada [Tema 4, pág. 7].
44. D. tellg() devuelve el tamaño en bytes [Tema 1.2, pág. 17].
45. B. El segundo nodo debe apuntar a NULL [Tema 4, pág. 17].
46. B. apilar(p, e) representa una pila no vacía [Tema 3, pág. 19].
47. C. La lista enlazada permite crecer sin límite [Tema 4, pág. 27].
48. C. Se pierde memoria dinámica compartida [Tema 4, pág. 41].
49. B. seekp() posiciona antes de escribir [Tema 1.2, pág. 16].
50. B. Se define con template <class T> [Tema 5, pág. 4].
51. A. El valor final es 800 [Tema 4, pág. 39].
52. C. El puntero quedaría apuntando a memoria liberada [Tema 4, pág. 39].
53. B. v++ apunta al segundo elemento, 2 [Tema 1.1, pág. 8].
54. C. El operador -> [Tema 1.1, pág. 5].
55. B. Solo válida si 1 ≤ i ≤ longitud(l) [Tema 3, pág. 6].
56. C. Cola donde se elige según prioridad [Tema 3, pág. 34].
57. C. Distintos términos pueden generar el mismo valor [Tema 2, pág. 10].
58. B. strcmp devuelve >0 si s1 > s2 [Tema 5, pág. 8].
59. C. Permite usar insertar con distintos tipos [Tema 5, pág. 10].
60. B. Devuelve true si n == 0 o elementos == NULL [Tema 5, pág. 11].
61. C. Tope == -1 indica pila vacía [Tema 3, pág. 23].
62. A. ofstream solo escribe; fstream lee y escribe [Tema 1.2, pág. 10].
63. A. Se recorre mientras el puntero no sea NULL [Tema 4, pág. 10].
64. C. Declara una clase genérica [Tema 5, pág. 5].
65. C. delete[] array [Tema 1.1, pág. 7].
66. B. Una cola recién creada está vacía [Tema 3, pág. 28].
67. B. Permiten acceso directo a posiciones [Tema 1.2, pág. 16].
68. C. Elimina correctamente el primero [Tema 4, pág. 17].
69. B. Se declara con * [Tema 1.1, pág. 2].
70. C. Se actualizan los enlaces circularmente [Tema 4, pág. 14].
71. B. Se elimina la memoria compartida del objeto [Tema 4, pág. 41].
72. C. Se redimensiona la cola dinámicamente [Tema 4, pág. 33].
73. D. creaPila y apilar forman el conjunto generador [Tema 3, pág. 19].
74. B. Definida si 1 ≤ i ≤ long(l) + 1 [Tema 3, pág. 6].
75. B. Permite volver al inicio directamente [Tema 4, pág. 8].
76. B. Se pierde el enlace previo [Tema 4, pág. 21].
77. B. Usar puntero a puntero para modificar el original [Tema 4, pág. 40].
78. D. Mayor eficiencia y menor memoria [Tema 4, pág. 27].
79. C. Devuelve la posición del elemento e1 [Tema 3, pág. 7].
80. C. desencolar no está definida para colas vacías [Tema 3, pág. 27].
81. C. La operación modificar no está definida [Tema 3, pág. 6].
82. C. Lista simplemente enlazada es más eficiente [Tema 4, pág. 27].
83. C. seekg al final y tellg [Tema 1.2, pág. 17].
84. C. PCli->Edad [Tema 1.1, pág. 5].
85. C. desapilar es parcial [Tema 3, pág. 18].
86. C. elementos == NULL indica lista vacía [Tema 4, pág. 9].
87. B. Acceso fuera de rango [Tema 1.1, pág. 8].
88. C. Posiciona el puntero de escritura al final [Tema 1.2, pág. 16].
89. C. concatena añadiendo l2 al final de l1 [Tema 3, pág. 15].
90. B. Reutiliza posiciones liberadas [Tema 3, pág. 30].
91. B. Verificar que Nodo_Aux no sea NULL [Tema 4, pág. 9].
92. B. Devuelve el nodo anterior [Tema 5, pág. 9].
93. C. Garantiza que los cambios se reflejen [Tema 4, pág. 40].
94. D. Provoca fuga de memoria [Tema 1.1, pág. 7].
95. B. Implementar listas genéricas [Tema 5, pág. 9].
96. B. Permite usar la función con cualquier tipo [Tema 5, pág. 4].
97. C. Insertar al principio es la más costosa [Tema 3, pág. 9].
98. C. La operación está indefinida [Tema 3, pág. 6].
99. C. Inserta el elemento a la derecha [Tema 3, pág. 7].
100. C. Se destruye la memoria dinámica compartida [Tema 4, pág. 41].
101. C. Puede causar errores en tiempo de ejecución [Tema 4, pág. 39].
102. C. Solo acceso secuencial [Tema 4, pág. 7].
103. B. Permite versiones alternativas de una función genérica [Tema 5, pág. 7].
104. C. primero() devuelve el primer elemento [Tema 4, pág. 38].
105. C. Se actualizan ambos enlaces [Tema 4, pág. 18].
106. A. Inserción a la izquierda y derecha equivalentes en lista vacía [Tema 3, pág. 7].
107. C. Provoca pérdida de memoria [Tema 1.1, pág. 7].
108. C. Devuelven valores de otro género [Tema 2, pág. 9].
109. C. Facilita inserciones en la cabeza [Tema 4, pág. 8].
110. C. Se deshace la última inserción [Tema 3, pág. 18].
111. B. typename es sinónimo de class [Tema 5, pág. 4].
112. B. cima devuelve el último insertado [Tema 3, pág. 18].
113. B. ++ es concatenación [Tema 2, pág. 10].
114. C. Muestra 3.14 [Tema 5, pág. 10].
115. D. Declarar char* e incluir <cstring> [Tema 5, pág. 8].
116. A. No escribe correctamente sin modo binario [Tema 1.2, pág. 15].
117. C. Parar al volver al inicio o cumplir la condición [Tema 4, pág. 10].
118. A. longitud() devuelve el número de elementos [Tema 5, pág. 11].
119. C. Se produce una fuga de memoria [Tema 4, pág. 11].
120. C. Cola (FIFO) [Tema 3, pág. 26].
121. A. 1 ≤ i ≤ longitud(l) [Tema 3, pág. 6].
122. B. El resultado es e [Tema 3, pág. 7].
123. B. No se puede saber si está vacía o llena [Tema 3, pág. 30].
124. A. Al apilar la pila deja de estar vacía [Tema 3, pág. 18].
125. B. Devuelve el i-ésimo elemento [Tema 3, pág. 6].
126. C. Puede sobrar espacio [Tema 3, pág. 9].
127. B. Se borra el primer nodo y se actualiza el puntero [Tema 4, pág. 30].
128. B. 7 [Tema 5, pág. 3].
129. C. Definir métodos en el .h [Tema 5, pág. 6].
130. B. Devuelve un valor del mismo género [Tema 2, pág. 9].
131. C. desapilar no está definido [Tema 3, pág. 18].
132. C. 1 ≤ i ≤ longitud(l) [Tema 3, pág. 6].
133. C. Puede crecer sin reubicar memoria [Tema 4, pág. 2].
134. C. Localizar el nodo previo [Tema 4, pág. 21].
135. B. cima(p2) devuelve 8 [Tema 3, pág. 18].
136. D. Fuera del dominio de definición [Tema 3, pág. 6].
137. B. Se recorre hasta que el puntero sea NULL [Tema 4, pág. 11].
138. C. delete en NULL es seguro [Tema 4, pág. 11].
139. C. new invoca el constructor [Tema 1.1, pág. 6].
140. C. read() permite control de bytes [Tema 1.2, pág. 15].
141. C. Se pierde el acceso al resto de la lista [Tema 4, pág. 18].
142. B. Se usa -> [Tema 1.1, pág. 5].
143. A. Devuelve un valor del mismo género y no generador [Tema 2, pág. 9].
144. B. La operación no está definida [Tema 3, pág. 27].
145. C. Puede producir comportamiento indefinido [Tema 4, pág. 39].
146. C. Permite insertar y eliminar sin mover elementos [Tema 4, pág. 2].
147. A. Puntero doble ** [Tema 4, pág. 40].
148. B. Posiciona el puntero de lectura [Tema 1.2, pág. 16].
149. A. vacia?(pila) [Tema 3, pág. 18].
150. C. gcount() devuelve los bytes leídos [Tema 1.2, pág. 15].
151. C. El resultado es 2 [Tema 3, pág. 6].
152. C. El último nodo apunta al primero y viceversa [Tema 4, pág. 8].
153. C. Acceso a memoria fuera del array [Tema 1.1, pág. 8].
154. C. Modelo abstracto con operaciones [Tema 2, pág. 2].
155. C. Se actualizan los punteros del último nodo [Tema 4, pág. 14].
156. B. Política LIFO [Tema 3, pág. 17].
157. A. 0 [Tema 5, pág. 11].
158. C. Elimina los flags de error [Tema 1.2, pág. 12].
159. B. Todos los términos construidos son distintos [Tema 2, pág. 10].
160. B. Reutilizar código con distintos tipos [Tema 5, pág. 4].
161. C. Se produce una fuga de memoria [Tema 1.1, pág. 7].
162. B. Devuelve -1 [Tema 4, pág. 5].
163. A. creaPila es generador [Tema 3, pág. 18].
164. B. Comportamiento indefinido [Tema 1.1, pág. 7].
165. C. Insertar el elemento al final [Tema 4, pág. 6].
166. C. Recorre todos excepto el primero [Tema 4, pág. 10].
167. D. Fuera del dominio de definición [Tema 3, pág. 6].
168. C. Puede crecer sin límite fijo [Tema 4, pág. 36].
169. C. No se escribe nada [Tema 1.2, pág. 10].
170. B. Clase que almacena elementos de cualquier tipo [Tema 5, pág. 5].
171. A. El archivo se expande al escribir [Tema 1.2, pág. 16].
172. B. Libera todos los nodos [Tema 4, pág. 30].
173. B. Inserta e como único nodo [Tema 4, pág. 4].
174. B. Cola necesita inicio y fin [Tema 4, pág. 34].
175. B. Dejar elementos = NULL [Tema 4, pág. 11].
176. C. La especificación está cerrada y completa [Tema 3, pág. 8].
177. C. Enlazar al anterior y al siguiente [Tema 4, pág. 15].
178. A. Puede no reservar memoria [Tema 4, pág. 4].
179. C. Archivo con acceso directo [Tema 1.2, pág. 18].
180. B. Inconsistencia grave [Tema 4, pág. 36].
181. B. La pila recién creada tiene longitud 0 [Tema 3, pág. 18].
182. C. Hay que actualizar también el último nodo [Tema 4, pág. 14].
183. C. Inserta e en la primera posición [Tema 3, pág. 6].
184. C. apilar() inserta en el tope [Tema 4, pág. 30].
185. B. No está definida la operación [Tema 4, pág. 6].
186. B. Comprueba si elementos es NULL [Tema 4, pág. 27].
187. B. Se necesitan dos punteros y actualizar tres enlaces [Tema 4, pág. 15].
188. B. Cola vacía [Tema 4, pág. 34].
189. B. Puede eliminar la memoria del original [Tema 4, pág. 41].
190. A. Nodo_Aux->Siguiente == Nodo_Act [Tema 4, pág. 12].
191. D. Se usa TIPO[] como parámetro [Tema 5, pág. 7].
192. C. Escribir solo al final del archivo [Tema 1.2, pág. 11].
193. A. Lista vacía [Tema 3, pág. 8].
194. D. Se recorre con un puntero auxiliar [Tema 4, pág. 15].
195. D. Posibles desbordamientos y accesos fuera de rango [Tema 1.1, pág. 8].
196. B. Cadena es una clase definida aparte [Tema 4, pág. 24].
197. B. Se liberan todos los nodos si se actualiza el puntero [Tema 4, pág. 11].
198. C. pertenece() o posicion() recorren la lista [Tema 4, pág. 6].
199. A. Se pierde acceso al resto de la lista [Tema 4, pág. 11].
200. B. Reinicialización de la cola vacía [Tema 4, pág. 36].
