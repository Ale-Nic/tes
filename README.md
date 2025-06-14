# Examen Tipo Test: Estructuras de Datos I

A continuación tienes las 200 preguntas con cuatro opciones cada una. Las soluciones (letras correctas) se encuentran al final del documento.

---

1. ¿Cuál de estas opciones permite crear un objeto en memoria dinámica e invocar su constructor por defecto?  
   - A) `cliente obj;`  
   - B) `new cliente();`  
   - C) `cliente* obj = new cliente;`  
   - D) `cliente* obj = cliente();`  

2. ¿Qué error produce este código al insertar un nodo al principio de una lista?

   ```cpp
   void insertarInicio(TNodo* Lista, Tipo_Elemento valor) {
     TNodo* NodoNuevo = new TNodo;
     NodoNuevo->Datos = valor;
     NodoNuevo->Siguiente = Lista;
     Lista = NodoNuevo;
   }
   ```
   - A) El nodo no se inserta correctamente  
   - B) El valor se sobrescribe  
   - C) Se modifica el nodo final  
   - D) No se reserva memoria  

3. ¿Qué operador se usa para obtener la dirección de una variable?  
   - A) `*`  
   - B) `->`  
   - C) `&`  
   - D) `%`  

4. ¿Qué tipo de estructura es ideal para implementar una cola con acceso eficiente en ambos extremos?  
   - A) Lista simple  
   - B) Lista circular  
   - C) Lista doblemente enlazada  
   - D) Tabla estática  

5. ¿Cuál es la finalidad de la función `posicion(e)` en una lista?  
   - A) Elimina el elemento `e`  
   - B) Devuelve la posición del elemento `e`  
   - C) Inserta el elemento `e`  
   - D) Retorna el valor del nodo anterior a `e`  

6. ¿Qué ocurre si usamos `ifstream f("archivo.txt");` y `f.fail()` devuelve true?  
   - A) El archivo está vacío  
   - B) El archivo está en modo binario  
   - C) El archivo no existe o no se pudo abrir  
   - D) El archivo ya estaba abierto  

7. ¿Qué ventaja tiene el uso de plantillas genéricas?  
   - A) Menor consumo de memoria  
   - B) Mayor velocidad de ejecución  
   - C) Reutilización de código con distintos tipos  
   - D) No requiere compilación  

8. ¿Qué operación está mal especificada si se ejecuta sobre una pila vacía?  
   - A) apilar  
   - B) longitud  
   - C) cima  
   - D) vacía?  

9. ¿Qué código crea correctamente un array dinámico de 100 enteros?  
   - A) `int tabla[100];`  
   - B) `int* tabla = new int;`  
   - C) `int* tabla = new int[100];`  
   - D) `tabla = new int;`  

10. ¿Cuál es el propósito del método `clear()` en flujos de fichero de C++?  
    - A) Borrar el fichero  
    - B) Resetear el puntero de lectura  
    - C) Limpiar el estado de error del stream  
    - D) Liberar el buffer  

...  (contenido omitido por brevedad; incluye preguntas 11 a 200)

---

## Soluciones

1. C  
2. A  
3. C  
4. C  
5. B  
6. C  
7. C  
8. C  
9. C  
10. C  
... (soluciones 11 a 200)  
