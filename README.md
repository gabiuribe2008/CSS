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