## Verificación y Validación
# Escritura de test parametrizados para el problema de las secuencias de Collatz

Plantilla de proyecto de IntelliJ para resolver el 
[problema 14 de Project Euler](https://projecteuler.net/problem=14). 


### Secuencias de Collatz

Se define la siguiente secuencia iterativa sobre el dominio de los enteros positivos:

 - _n_ → _n_ / 2   (si _n_ es par)
 - _n_ → 3 _n_ + 1 (si _n_ es impar)
    
Utilizando dicha definición y empezando en 13, se genera la siguiente secuencia:

13 → 40 → 20 → 10 → 5 → 16 → 8 → 4 → 2 → 1.

Puede comprobarse que esta secuencia (que comienza en 13 y termina en 1), contiene
 10 términos. Pese a que no ha sido probado aún (Conjetura de Collatz), se cree
 que las secuencias generadas empezando en cualquier número terminan en 1.

¿Qué número inicial, por debajo de un millón, genera la secuencia más larga?

**Nota**: Una vez la secuencia ha comenzado, es posible que algunos términos
superen el límite de un millón.

### Tareas

 1. Descargad o clonad el proyecto «unizar-vv-collatz» de GitHub.
 2. El proyecto está configurado para poder utilizar tanto JUnit 4 como JUnit 5.
    Para evitar mezclar clases del mismo nombre que están en los dos entornos,
    se recomienda eliminar una de las dos dependencias (menú ``File > 
    Project Structure... > Project Settings > Modules``).
 2. Observad las clases `SecuenciaCollatz`,`Main` y sus métodos.
 3. Clase `SecuenciasCollatzTestSiguiente`
    - Diseñad pruebas basadas en la especificación para el método 
      `siguienteCollatz` aplicando particiones de equivalencia.
    - Por cada prueba diseñada:
        - Escribid un test en JUnit.
        - Ejecutad el test para comprobar que falla.
        - Añadid el código necesario para que el test pase.
        - Comprobad que la cobertura del método `siguienteCollatz` en modo 
          _tracing_ es del 100%.
    - Usad la secuencia de ejemplo del enunciado como _test basis_ para obtener
      casos de prueba adicionales, aunque sean redundantes.  
    - Convertid las pruebas diseñadas en un test JUnit parametrizado.
 
 4. Clase `SecuenciasCollatzTestLongitud`
    - Diseñad pruebas basadas en la especificación para el método 
      `longitud`.
      - Basaos, por una parte, en la secuencia de ejemplo del enunciado. 
        Se trata de una única secuencia, pero podemos distinguir 9 subsecuencias
        más que terminan en 1.
      - Completad los casos de prueba calculando _a mano_ las longitudes de las
        secuencias iniciadas por los números del 1 al 10.
    - Escribid un test parametrizado en el que ir incluyendo las pruebas diseñadas.
      Incluirlas de una en una y observad como va aumentando la cobertura del
      código conforme las vais añadiendo.
      
 5. Clase `IniciadorSecuenciaMasLargaTest`
    - Diseño de pruebas basadas en la especificación (basaos en las longitudes
      de las secuencias iniciadas por los números del 1 al 10 que habéis
      calculado antes).
    - Proponed los casos de prueba.
 
 6. Resto de métodos
    - Añadid pruebas hasta alcanzar una cobertura del 100% en modo _tracing_.