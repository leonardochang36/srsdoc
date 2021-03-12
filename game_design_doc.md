# Documento de diseño del juego

## The sTEAM:
- Lourdes Badillo, A01024232
- Valeria Pineda, A01023979
- Eduardo Villalpando, A01023646

<b>Videojuego diseñado para Movimiento STEAM </b>

# Índice
- [Diseño del Juego](#diseño-del-juego)
  * [Resumen](#resumen)
  * [Dinámica del juego](#dinámica-del-juego)
  * [Mentalidad](#mentalidad)
- [Técnico](#técnico)
  * [Pantallas](#pantallas)
  * [Controles](#controles)
- [Mecánicas](#mecánicas)
- [Diseño de niveles](#diseño-de-niveles)
  * [Temas](#temas)
  * [Características de cada nivel](#características-de-cada-nivel)
- [Desarrollo](#desarrollo)
- [Gráficos](#gráficos)
  * [Atributos del estilo](#atributos-del-estilo)
  * [Gráficos](#gráficos-1)
    + [Personaje](#personaje)
    + [Planetas](#planetas)
    + [Naves](#naves)
    + [Satélites artificiales](#satélites-artificiales)
    + [Satélites naturales](#satélites-naturales)
    + [Asteroides](#asteroides)
    + [Fondos espaciales](#fondos-espaciales)
- [Sonido/Música](#sonido-música)
  * [Atributos del estilo](#atributos-del-estilo-1)
  * [Sonidos requeridos](#sonidos-requeridos)
- [Calendario](#calendario)

<br> 

#  Diseño del Juego

## Resumen
Uno de los mayores logros de la humanidad ha sido llegar al espacio. En este juego, el usuario tendrá que poner naves espaciales en la órbita de distintos planetas, comprendiendo el impacto de STEM en el mundo.

## Dinámica del juego
        Se generarán niveles de forma automática en los que el jugador ajustará la potencia de la nave, así como el ángulo de su trayectoria con el objetivo de que se mantenga en órbita. Para cada nivel se variará la masa de la nave y fuerza de gravedad, y se incluirán obstáculos con el fin de que el jugador use pensamiento crítico y análisis para resolver la problemática.  

## Mentalidad
        El propósito del juego es generar interés en las ciencias, especialmente cuando están siendo aplicadas al viaje interestelar. Para esto, se tiene que estar en un estado calmado y enfocado. Al ir viviendo la dinámica del juego el jugador se sentirá inspirado con las posibilidades que abre la ciencia, con ganas de avanzar al siguiente nivel para descubrir nuevos retos y soluciones a distintos problemas. Esto se va a lograr con gráficos que llaman la atención y con niveles que van cambiando poco a poco. Estos cambios constantes, junto con pequeñas piezas de información en cada nivel, van atrapando la atención del jugador y le informan sobre las aplicaciones de diferentes ramas de la ciencia.

# Técnico

## Pantallas
1.  Pantalla título: Mostrará el puntaje del jugador, así como información del juego.
2.  Registro de usuario: Permitirá al jugador registrar datos relevantes
3.  Juego
4.  Desafío de poner un objeto en órbita: Se mostrarán los controles para interactuar, así como los planetas y objetos. Igualmente se mostrarán las vidas disponibles y la puntuación.
5.  Datos relevantes de una carrera STEM: Con botones para saber si le interesó al jugador
6.  Créditos Finales

## Controles

        Trayectoria y potencia: El jugador podrá mover la nave a partir de un punto pivote (estilo Angry Birds). 
<br>
Una flecha punteada desde la nave indicará la trayectoria y velocidad de la misma. Éstas puede ser ajustadas por el jugador arrastrando la nave. <br> Cuando ésta se suelte, la nave seguirá la trayectoria y velocidades establecidas.

        Menú: Se incluirá un menú para pausar el juego, ver el puntaje y leer información relevante.

# Mecánicas        

Física:

-   Movimiento orbital ([https://www.bbc.co.uk/bitesize/guides/zg638mn/revision/4](https://www.google.com/url?q=https://www.bbc.co.uk/bitesize/guides/zg638mn/revision/4&sa=D&source=editors&ust=1614291589977000&usg=AOvVaw3CUijghEJDNfacpGyMtOQj))
-   Movimiento circular uniforme

Reglas:

-   El jugador cuenta con tres oportunidades para poner el objeto en órbita.
-   Se puede ajustar el ángulo de lanzamiento y la propulsión inicial.
-   Con cada nivel varía la masa de la nave, su distancia y la gravedad de cada planeta.
-   Si no se logra poner la nave en órbita, esta choca contra el planeta o se va a la lejanía.
-   La cantidad de puntos otorgados dependen de la cantidad de revoluciones orbitales conseguidas.
-   Existen _power-ups_, los cuales están relacionados con avances STEM y le dan al jugador puntos extra. Una vez que junta diez, consigue una vida extra.

![](pantallas/dinamica.png?AAAA)

# Diseño de niveles
## Temas

- Espacio
    - Mood
        - Divertido, interesante, misterioso
    - Objetos
        - Ambiente
            - Fondo oscuro
            - Estrellas, galaxias, cometas
        - Interactivos
            - Naves espaciales 
            - Satélites artificiales
            - Satélites naturales
            - Planetas

## Características de cada nivel
-   Objeto que se lanza: En cada nivel el jugador tiene como objetivo poner un objeto en órbita, este puede ser una nave espacial, un satélite de comunicación o incluso un satélite natural.
-   Planeta: Todos los niveles tienen un planeta para el cual varía su masa, tamaño y color.
-   Obstáculos: La dificultad de cada nivel va incrementando y se empezarán a añadir obstáculos, los cuales son otros objetos orbitantes con los que se puede hacer colisión. 
-   En niveles avanzados puedes orbitar más de un objeto, el de mayor dificultad te dará más puntos.

    ![](images/image11.png)

# Desarrollo
 ## Clases Abstractas / Componentes
- Pantallas
    - Generador de niveles
    - Pasar al siguiente nivel 

- Planetas 
    - Colisión
    - Generación aleatoria

- Cohete
    - Movimiento de arrastre
    - Lanzamiento
    - Gravedad
    
- Power-ups y obstáculos
    - Movimiento circular uniforme
    - Modificar puntuación
    - Modificar vidas


# Gráficos

## Atributos del estilo
Nos inspiramos en los gráficos que utiliza Kurzgesagt para sus vídeos, ya que estos son muy atractivos para el segmento objetivo de nuestro juego. La imagen de abajo es nuestra fuente de inspiración:

<img src="images/image14.png" alt="Kurzgesagt Planets" width="300"/>

## Gráficos

### Personaje 
<img src="images/ajolote.png" alt="ajolote" width="200">

### Planetas
- Distintos colores y rayas

    <img src="images/image1.png" alt="Graphic" width="100"/>
    <img src="images/image15.png" alt="Graphic" width="100"/>
    <img src="images/image18.png" alt="Graphic" width="100"/>
    <img src="images/image16.png" alt="Graphic" width="100"/>
    <img src="images/image12.png" alt="Graphic" width="100"/>
    <img src="images/image8.png" alt="Graphic" width="100"/>
    <img src="images/image5.png" alt="Graphic" width="100"/>
    <img src="images/image3.png" alt="Graphic" width="100"/>
    <img src="images/image9.png" alt="Graphic" width="100"/>
    <img src="images/image10.png" alt="Graphic" width="100"/>
    <img src="images/image21.png" alt="Graphic" width="100"/>
<br><br>

- Con anillos

    <img src="images/image7.png" alt="Graphic" width="150"/>

### Naves

<img src="images/image20.png" alt="Graphic" width="150"/> <img src="images/rocket7.png" alt="Graphic" width="150"/> <img src="images/rocket3.png" alt="Graphic" width="150"/> <img src="images/rocket4.png" alt="Graphic" width="150"/> <img src="images/rocket5.png" alt="Graphic" width="150"/> <img src="images/rocket6.png" alt="Graphic" width="150"/> <img src="images/rocket2.png" alt="Graphic" width="150"/>

### Satélites artificiales

- Con dos páneles solares

    <img src="images/satellite1.png" alt="Graphic" width="200"/>
    <img src="images/satellite2.png" alt="Graphic" width="200"/>
    <img src="images/satellite3.png" alt="Graphic" width="200"/>

### Satélites naturales

- Forma de papa

    <img src="images/moon2.png" alt="Graphic" width="100"/>

- Circulares

    <img src="images/image6.png" alt="Graphic" width="100"/>

### Asteroides

<img src="images/asteroid1.png" alt="Graphic" width="150"/> <img src="images/asteroid2.png" alt="Graphic" width="150"/>

### Fondos espaciales

- Degradado radial

    <img src="images/image19.png" alt="Graphic" width="200"/>

- Degradado vertical

    <img src="images/image4.png" alt="Graphic" width="200"/>

    <img src="images/image13.png" alt="Graphic" width="200"/>


# Sonido/Música

## Atributos del estilo

        Queremos incluir música de fondo, inspirándonos en el soundtrack de Interstellar, compuesta por Hans Zimmer. Esto le agregará un sentimiento de misterio. Tomar como inspiración el siguiente audio: [https://youtu.be/IqiTJK\_uzUY?t=231](https://www.google.com/url?q=https://youtu.be/IqiTJK_uzUY?t%3D231&sa=D&source=editors&ust=1614291589987000&usg=AOvVaw1QD_ZHMADao77bPACILcH2) 

## Sonidos requeridos

1.  Efectos
    -  Despegue de la nave
    - Explosión

2.  Feedback
    - Happy chime (Se logró el nivel)
    - Sad chime (Colisión o se perdió la nave)

# Calendario

1.  ✅ Definir idea del videojuego
2.  ✅ Establecer la dinámica y mecánica
3.  ✅ Elaborar ilustraciones
4.  ⌛ Programar el videojuego
    - ⌛ Realizar scripts con parámetros físicos
    - ⌛ Incorporar interacciones entre objetos
    - ⌛ Incorporar interacción con el usuario
5.  🔜 Investigar y agregar datos curiosos
    - 🔜 Realizar script para leer los datos y mostrar durante el juego
6.  ⏸ Realizar conexión con la base de datos
    - 🔜 Definir estructura y tablas necesarias
    - ⏸ Programar servidor con base de datos
    - ⏸ Programar conexión en el juego con base de datos
    - ⏸ Actualización de datos
6.  ⏸ Generar dashboard donde se muestran los datos recolectados
7.  ⏸ Incluir música y efectos de sonido
