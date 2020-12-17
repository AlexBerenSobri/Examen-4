Guía de marcado para "Estructurar datos planetarios"

La siguiente guía describe una guía de calificación para el tema HTML del Área de aprendizaje de MDN: Estructuración de datos planetarios. Cada subtarea detallada en la evaluación se enumera a continuación, junto con una explicación de cuántas marcas vale la tarea.

Nota: Estas son pautas, no reglas escritas en piedra; por supuesto, usted es libre de usar su criterio sobre la concesión de calificaciones cuando se encuentra con un caso límite o algo que no está claramente definido.

La calificación general otorgada es de 34. Calcule su calificación final y luego divida por 34 y multiplique por 100 para obtener una marca de porcentaje. Como referencia, puede encontrar una página marcada terminada que recibiría las mejores calificaciones.
Semántica de bloques / estructural

Dar a la mesa una estructura básica de alto nivel: un contenedor exterior, un encabezado de mesa y un cuerpo de mesa (3 puntos).
    Esto es bastante simple. El estudiante solo necesita incluir un elemento <table> en la página, con <thead> y <tbody> como hijos.
Agregue el título provisto a su tabla. (2 puntos)
    Nuevamente, es simple, pero debe colocarse en el lugar correcto: el título proporcionado debe colocarse en un elemento <caption>, justo debajo de la etiqueta de apertura <table>.
Agregue una fila al encabezado de la tabla que contenga todos los encabezados de columna (5 puntos).
    El estudiante necesita:

        Coloque las celdas de la fila dentro de un elemento <tr> y use elementos <th> para las celdas porque son encabezados (2 marcas).
        Coloque el texto del encabezado de la columna en cada celda correctamente, copiado de los datos sin procesar (1 marca).
        Deje un espacio de dos columnas al comienzo de la fila; esto se hace mejor con una sola celda con colspan = "2", pero aceptaríamos dos celdas (2 puntos).

Nota: Se recomienda asignar a la columna de nombres de planetas un encabezado de "Nombre", pero no perderán una marca si lo olvidan.
Cree todas las filas de contenido dentro del cuerpo de la tabla, recordando convertir todos los encabezados de fila en encabezados semánticamente (15 puntos).
    Esta es la parte más difícil de la tabla: requiere colocar todos los encabezados de las filas del grupo en las filas correctas y hacer que abarquen el número correcto de filas y columnas.

        En primer lugar, cada fila debe colocarse dentro del <tbody> (1 marca).
        Cada fila debe contener un elemento <th> que contenga el nombre del planeta al principio seguido de nueve elementos <td> que contengan los datos del planeta (5 puntos). Otorgue la máxima puntuación si esto es en su mayoría correcto con un par de errores tipográficos, pero comience a reducir la marca a su discreción si los puntos de datos importantes están equivocados, mal ubicados u omitidos. Quite dos puntos si los nombres de los planetas no se colocan en los encabezados.
        La primera fila del cuerpo debe contener un elemento <th> adicional al principio, que contenga "planetas terrestres", con rowspan = "4" y colspan = "2" (2 puntos).
        La quinta fila de cuerpos debe contener dos elementos <th> adicionales al principio, que contengan "planetas jovianos" y "gigantes gaseosos" respectivamente. El primero necesita rowspan = "4" y el segundo necesita rowspan = "2" (3 puntos).
        La séptima fila del cuerpo debe contener un elemento <th> adicional al principio, que contenga "Gigantes de hielo", con rowspan = "2" (2 puntos).
        La novena fila del cuerpo debe contener un elemento <th> adicional al principio, que contenga "Planetas enanos", con colspan = "2" (2 puntos).

Agregue atributos para que los encabezados de fila y columna se asocien de manera inequívoca con las filas, columnas o grupos de filas para los que actúan como encabezados (5 puntos).
    El estudiante debe agregar el valor del alcance a todos los elementos <th>, dándoles los valores apropiados como se muestra a continuación:

        col: Todos los elementos <th> en la fila del encabezado de la tabla.
        fila: Todos los elementos <th> que contienen nombres de planetas y el que contiene "planetas enanos" (también es un encabezado sobre una sola fila).
        rowgroup: Los <th> elementos que contienen "planetas terrestres", "planetas jovianos", "gigantes gaseosos" y "gigantes de hielo".

Agregue un borde negro alrededor de la columna que contiene todos los encabezados de fila de nombres de planetas (4 puntos).
    La forma más sencilla de hacerlo es:

        Agregue un elemento <colgroup> justo debajo del elemento <caption>.
        Dentro de este, anide dos elementos <col>, uno con un atributo span = "2" y el otro con un atributo de estilo a lo largo de las líneas de style = "border: 2px solid black".
        Notas: Sería aceptable definir todas las columnas de la tabla dentro del colgroup, aunque no es necesario. Agregar el estilo a cada celda de la columna individual no sería aceptable; esto colocaría el estilo alrededor de cada celda de la columna, no de la columna.

