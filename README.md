###  Introducción

Esta segunda asignación de programación requerirá que escriba una R
función que es capaz de almacenar en caché cálculos que pueden consumir mucho tiempo. por
Por ejemplo, tomar la media de un vector numérico es típicamente una
función que es capaz de almacenar en caché cálculos que pueden consumir mucho tiempo.
Por ejemplo, tomar la media de un vector numérico es típicamente una
operación. Sin embargo, para un vector muy largo, puede llevar demasiado tiempo
calcular la media, especialmente si tiene que calcularse repetidamente (p. ej.
en un bucle). Si el contenido de un vector no cambia, puede hacer
sentido almacenar en caché el valor de la media para que cuando lo necesitemos de nuevo,
se puede buscar en la caché en lugar de volver a calcular. En esto
Asignación de programación, se beneficiará de las reglas de alcance de la R
lenguaje y cómo se pueden manipular para preservar el estado dentro de un
Objeto R.
Asignación de programación, se beneficiará de las reglas de alcance de
el lenguaje R y cómo se pueden manipular para preservar el estado dentro
de un objeto R.

###  Asignación: Almacenamiento en caché de la inversa de una matriz
La inversión de matrices suele ser un cálculo costoso y puede haber algunos
Beneficio de almacenar en caché la inversa de una matriz en lugar de calcularla
repetidamente (también hay alternativas a la inversión de matriz que
no discutir aquí). Tu tarea es escribir un par de funciones que
almacenar en caché la inversa de una matriz.
Escribe las siguientes funciones:
1.   `makeCacheMatrix` : Esta función crea un objeto especial de" matriz "
    que puede almacenar en caché su inverso.
2.   `cacheSolve` : esta función calcula la inversa de la especial
    "matriz" devuelta por `makeCacheMatrix` arriba. Si la inversa tiene
    ya se ha calculado (y la matriz no ha cambiado), entonces el
    ` Cachesolve ` debe recuperar la inversa de la caché.
    ya se ha calculado (y la matriz no ha cambiado), entonces
    ` CacheSolve ` debe recuperar la inversa de la caché.

Calcular la inversa de una matriz cuadrada se puede hacer con el "solve"
función en R. Por ejemplo, si `X` es una matriz cuadrada invertible, entonces
`solve (X)` devuelve su inverso.
Para esta asignación, suponga que la matriz proporcionada siempre es
invertible.
Para completar esta tarea, debe hacer lo siguiente:
1.   Bifurque el repositorio de GitHub que contiene los archivos stub R en
    [ https://github.com/rdpeng/ProgrammingAssignment2 ] (https://github.com/rdpeng/ProgrammingAssignment2)
    para crear una copia con su propia cuenta.
2.   Clone su repositorio de GitHub bifurcado en su computadora para que pueda
    edite los archivos localmente en su propia máquina.
3.   Edite el archivo R contenido en el repositorio de git y coloque su
    solución en ese archivo (no cambie el nombre del archivo).
4.   Confirme su archivo R completo en SU ​​repositorio git y envíe su
    git al repositorio de GitHub en su cuenta.
5.   Envíe a Coursera la URL de su repositorio de GitHub que contiene
    el código R completo para la asignación.
###  Calificación
Esta tarea se calificará mediante una evaluación de pares.
