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

###  Ejemplo: almacenamiento en caché de la media de un vector

En este ejemplo introducimos el operador `<< -` que se puede usar para
asignar un valor a un objeto en un entorno que es diferente del
entorno actual. A continuación se muestran dos funciones que se utilizan para crear un
objeto especial que almacena un vector numérico y almacena en caché su media.
La primera función, `makeVector` crea un" vector "especial, que es
realmente una lista que contiene una función para
1.   establece el valor del vector
2.   obtener el valor del vector
3.   establecer el valor de la media
4.   obtener el valor de la media
<! -  ->
    makeVector <- función (x = numeric ()) {
            m <- NULO
            set <- función (y) {
                    x << - y
                    m << - NULO
            }
            obtener <- función () x
            setmean <- función (media) m << - media
            getmean <- función () m
            lista (establecer = establecer, obtener = obtener,
                 setmean = setmean,
                 getmean = getmean)
    }
La siguiente función calcula la media del "vector" especial
creado con la función anterior. Sin embargo, primero verifica si el
la media ya se ha calculado. Si es así, `GET` es la media de la
caché y omite el cálculo. De lo contrario, calcula la media de
los datos y establece el valor de la media en la caché a través de `setmean`
función.
    cachemean <- función (x, ...) {
            m <- x $ getmean ()
            if (! is.null (m)) {
                    mensaje ("obteniendo datos en caché")
                    volver (m)
            }
            datos <- x $ get ()
            m <- media (datos, ...)
            x $ setmean (m)
            metro
    }
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
