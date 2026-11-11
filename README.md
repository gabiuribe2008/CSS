# CSS
# Catálogo semántico y jerarquía CSS

## Descripción del proyecto

En esta actividad se aplican conceptos básicos de CSS para mejorar la apariencia de una página web, comprender la herencia de estilos, utilizar selectores combinados y reconocer cómo funcionan la cascada y la especificidad.

## 1. Herencia en CSS

La herencia permite que algunos elementos HTML reciban automáticamente determinadas propiedades de sus elementos padres.

Se establece una tipografía y un color de texto general en la etiqueta body. De esta manera, los encabezados, párrafos y listas pueden heredar estas propiedades sin necesidad de definirlas individualmente.

## 2. Selectores combinados

Los selectores combinados permiten aplicar estilos a elementos según su ubicación dentro de la estructura HTML.

Esta técnica permite asignar diferentes colores a los enlaces del encabezado, la barra lateral y el pie de página. Así, cada zona de la página puede modificarse de forma independiente, evitando cambios innecesarios en otras áreas.

## 3. Cascada y especificidad

La especificidad determina qué selector tiene mayor prioridad cuando varias reglas intentan modificar la misma propiedad de un elemento.

El sistema de puntuación de especificidad es el siguiente:

| Tipo de selector | Puntuación |
|---|---:|
| Etiqueta | 1 punto |
| Clase | 10 puntos |
| Identificador | 100 puntos |

Los identificadores tienen mayor especificidad que las clases, y las clases tienen mayor especificidad que las etiquetas. Cuando varios selectores compiten por una misma propiedad, la especificidad ayuda a determinar cuál prevalece.

## 4. Refactorización de estilos

La refactorización consiste en reorganizar y mejorar el código para facilitar su mantenimiento y evitar conflictos entre reglas CSS.

Para ello, se eliminan los selectores basados en identificadores y se prioriza el uso de etiquetas y clases. Esto facilita la reutilización de estilos y permite mantener una estructura más organizada.

También se deben evitar las reglas duplicadas y resolver los conflictos mediante una correcta organización de los selectores, sin utilizar la propiedad !important.

## 5. Control de versiones con Git

Para registrar los cambios realizados en los estilos y enviarlos al repositorio remoto, se utilizan los comandos de Git correspondientes.

El proceso consiste en preparar los archivos modificados, registrar los cambios mediante un commit y enviarlos a la rama develop del repositorio remoto mediante un push.

El mensaje del commit utilizado para identificar esta

## “Hallazgos: El Modelo de Caja”
(1) La diferencia práctica entre Margin y Padding, 

Margin: Es el espacio externo que separa el borde de un elemento respecto a otros elementos que lo rodean. No cuenta para el tamaño interno de la caja y permite valores negativos o auto

Padding:Es el espacio interno que hay entre el contenido de un elemento y su propio borde. 
(2) Por qué es obligatorio usar box-sizing: border-box

Porque nos permite alteral el modelo de caja del navegador para que el ancho (width) y el alto (height) de un elemento incluyan su relleno (padding) y su borde (border)

 (3) Cómo se ven afectados los elementos hermanos cuando le aplicas un margen grande a uno de ellos.

 Cuando aplicas un margen grande a un elemento, afectas directamente la posición de sus elementos hermanos porque el margen empuja el espacio disponible a su alrededor
 ## Hallazgos: Centralización de Identidad Visual y Espaciado

(1) La lista completa de variables declaradas 


gracias root cree una lista de variables la cual no ayudo a definir y organizar de manera mas practicas los valores de los diseños de las pagina
--colorprimary:  #ffc8df;
  --colorsecundario: #e9588b;
  --colorterciario: #b45387;
  --colorcuarto: #58102776;
  --colorquinto: #0d0004; 
  --sextocolor:  #473696; 
  --septimocolor: #530019;
  --coloroctavo: #ffffff;
  --colornoveno: #fbbcd048;
  --tipografia1: "Crafty Girls", cursive;
  --espacemedio: 25px;
  --espaciogrande: 50px ;
  


(2) La ventaja de reutilizar medidas de margen y relleno en lugar de inventar valores en cada selector
La ventaja de reutilizar medidas de margen (margin) y relleno (padding) en lugar de inventar valores en cada selector es mantener la consistencia y uniformidad del diseño.

Esto permite:

Mantener la coherencia visual: los elementos conservan espacios similares en toda la página.
Facilitar el mantenimiento: si se necesita cambiar el espaciado, basta con modificar los valores reutilizables.
Evitar errores: se reducen diferencias innecesarias entre elementos.
Ahorrar tiempo: no es necesario definir nuevas medidas para cada selector.
Mejorar la escalabilidad: el diseño es más fácil de adaptar y ampliar.


(3) De qué manera la centralización en :root previene colisiones visuales a medida que la hoja
de estilos crece.

La centralización de variables CSS en :root ayuda a prevenir colisiones visuales porque permite definir y administrar los valores de diseño desde un único lugar, evitando que diferentes partes de la hoja de estilos utilicen medidas, colores o estilos contradictorios.

Hallazgos: Pseudoclases y Pseudoelementos
1. Diferencia entre pseudoclases y pseudoelementos

Las pseudoclases y los pseudoelementos permiten mejorar la apariencia y la interactividad de una página web mediante CSS.

Las pseudoclases permiten cambiar los estilos de un elemento dependiendo de la interacción del usuario. En esta actividad se utilizaron :hover, para cambiar el color de las categorías y los botones al pasar el cursor; :focus, para resaltar los enlaces cuando se navega con el teclado; y :active, para generar un efecto de presión al hacer clic en los botones de compra.

Los pseudoelementos permiten agregar contenido decorativo sin necesidad de modificar la estructura