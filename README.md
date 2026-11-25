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


## Hallazgos: Arquitectura BEM y Modularidad

### 1. ¿Qué significa BEM y cómo se escribe visualmente?

BEM significa *Block, Element, Modifier* (Bloque, Elemento y Modificador). Es una metodología que permite organizar las clases de HTML y CSS de manera clara, facilitando la identificación de cada componente y sus partes.

Su estructura se representa de la siguiente manera:

- **Bloque:** es un componente independiente, como una tarjeta de producto. Se escribe `.card`.
- **Elemento:** es una parte que pertenece al bloque y se identifica con dos guiones bajos. Por ejemplo, `.card__title` representa el título de una tarjeta.
- **Modificador:** permite crear una variación visual o funcional de un bloque o elemento. Se escribe con dos guiones medios, como `.card--destacada`.

Esta nomenclatura permite identificar fácilmente la función de cada clase y evita utilizar nombres genéricos que puedan generar conflictos entre componentes.

### 2. ¿Por qué dividir el CSS en varios archivos facilita el trabajo colaborativo?

La modularidad consiste en dividir una hoja de estilos principal en archivos más pequeños, donde cada uno se encarga de un componente específico de la página.

Durante la práctica, se utilizaron archivos independientes como `tarjeta.css` y `botones.css`, que posteriormente se conectaron al archivo principal `style.css` mediante la regla `@import`.

Esta organización facilita el trabajo colaborativo porque permite que cada integrante del equipo trabaje en un componente diferente sin tener que modificar constantemente un mismo archivo. También ayuda a encontrar errores, realizar modificaciones y mantener el código organizado.

Además, cuando se necesita actualizar un componente, es posible modificar únicamente su archivo correspondiente sin afectar directamente los estilos de los demás.

### 3. ¿Cómo BEM evita la guerra de especificidad y mantiene un peso plano?

La guerra de especificidad ocurre cuando varias reglas CSS intentan aplicar estilos diferentes al mismo elemento, generando conflictos sobre cuál debe prevalecer.

BEM ayuda a evitar este problema mediante el uso de clases independientes y selectores planos, sin necesidad de crear reglas anidadas o cada vez más complejas.

Por ejemplo, en lugar de utilizar un selector como `.producto h2`, se utiliza la clase `.card__title`. Ambas reglas tienen una especificidad de 10 puntos, pero la segunda permite identificar directamente el elemento que se desea modificar.

Al mantener una especificidad uniforme, las reglas CSS son más fáciles de controlar y se reducen los conflictos entre componentes. Los estilos se aplican de manera más predecible, teniendo en cuenta el orden de la cascada y las demás reglas de prioridad de CSS.

Es importante aclarar que BEM no elimina completamente la cascada, sino que ayuda a mantenerla organizada y evita que los estilos dependan de selectores demasiado específicos.

### Conclusión

La combinación de BEM y la modularidad permite desarrollar interfaces más organizadas, fáciles de mantener y preparadas para crecer. La separación de archivos facilita el trabajo en equipo, mientras que la nomenclatura BEM permite identificar cada componente y mantener una especificidad plana.

Gracias a esta metodología, es posible realizar cambios en el diseño de una página sin generar conflictos innecesarios entre los estilos, conservando una estructura clara y reutilizable.