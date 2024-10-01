# CSS 

- Es un lenguaje para dar estilos a la web

## SINTAXIS

- Como se puede establecer codigo CSS

```css
h1{
    color: red;
}
```
- h1 : Selector
- color : Propiedad
- red : Valor

## CONCEPTOS IMPORTANTES CSS

- 4 Conceptos importantes de CSS

### SELECTORES

- Indica a que elemento o elementos, se aplicara estilos

```css
/* SELECTOR DE ETIQUETA  */
h1{
    color: red;
}

/* SELECTOR DE DESCENDENCIA */
nav ul li a {
    color: red;
}
```

### HERENCIA

- Elementos ancestros heredan algunas propiedades a sus descendientes.

```html 
<p>Hola mundo <a href="">Esto es un enlace</a></p>
```

```css
p{
    color: green;
}

a{
    color: inherit;
}
```

### CASCADA

- Significa que los estilos que llegan en ultimo lugar, sobreescriben a los de antes.
- La especificidad vence a la cascada

```css
h1{
    color: red;
}

h1{
    color: green;
}
```

### ESPECIFICIDAD

- Es un valor numerico que adquieren los selectores y se aplica cuando hay conflictos

```html
<!-- Selector de Etiqueta (1)-->

<!-- Selector de Clase (10)-->

<!-- Selector de ID (100)-->

<!-- Inline  (1000)-->

<!-- IMPORTANT (infinito)-->
```

## ESTILOS DE TEXTO

### PROPIEDADES

- color
- font-size (em,rem,px)
- font-family (google fonts - fontface)
- font-weight (peso de tipografia)
- estilo entre navegadores (normalize.css)
- text-transform: uppercase | lowercase | capitalize
- text-align : left | center | right
- text-decoration : none | underline

### SELECTORES
- Selector de Etiqueta(1)
- Selector de Clase(10)
- Selector de ID(100)
- Selector Universal (uso box model)

```html

<!-- Actualizar el repositorio con lo visto en la 2da parte
  1) Explicar los conceptos con ejemplos
  2) (Agregar una nueva tipografia de google fonts, usando font-face)
-->
```

## SELECTORES

- La manera de agarrar elemento o elementos del HTML para aplicar estilos
 
## SELECTORES SIMPLES
 
1. Selector de Etiqueta
 
- Se aplica a elementos HTML especificos
- Se le conoce como estilos base(general)
 
```css
h1 {
  color: red;
}
 
span {
  display: block;
}
```
 
2. Selector de Clase
 
- Es un atributo HTML que se indica con "class"
- Es lo mas utilizado en CSS para aplicar estilos (recomendado)
- Para el nombramiento de clases se utiliza nomenclatura( arquitectura )
 
```html
<h1 class="message">Selector de Clase</h1>
```
 
```css
.message {
  color: blue;
}
```
 
3. Selector de ID
 
- Es un atributo HTML que se indica con "id"
- No se recomienda utilizarlo para CSS
- No puede existir dos elementos html con el mismo "id"
 
```html
<main id="mainContent">Contenido principal</main>
```
 
```css
#mainContent {
  display: block;
}
```
 
4. Selector Universal
 
- No se recomienda utilizar mucho
- Tiene un caso especifico
 
```css
* {
  color: red;
}
```
 
## SELECTORES COMPUESTOS
 
1. Selector de Descendencia (Descendente)
 
- Se aplica a un elemento que esta incluido en otro
- No necesita ser hijo directo, puede estar niveles mas abajo
 
```html
<div class="padre">
  <p>Hijo 1</p>
  <p>Hijo 2</p>
  <p>Hijo 3</p>
</div>
```
 
2. Selector Hijo Directo
 
- Selecciona al elemento o elementos que estan dentro y seguido de otro elemento
 
```html
<div class="padre">
  <p>Hijo 1</p>
  <p>Hijo 2</p>
  <p>Hijo 3</p>
</div>
```
 
```css
.padre > .hijo {
  color: red;
}
```
 
3. Selector Anidado
 
- Juntar selectores mediante comas
- Se aplica a todos los selectores
 
## BOX MODEL
 
 
- Algoritmo que usa el navegador para dibujar elementos
- Estos elementos tienen propiedades
- Todos los elementos en la web son rectangulares
- Propiedades importantes ( width - height )( ancho - alto )
- Elementos bloque ( width - height )
- Elementos inline ( width relativo - no tiene height)
- Propiedad display
- El box model se aplica solo a elementos de bloque
 
```html
<div>Soy un elemento</div>
```
 
### PARTES
 
1. Content Box (AZUL)
2. Padding Box (VERDE)
3. Border Box (AMARILLO)
4. Margin Box (NARANJA)
 
## POSICIONAMIENTO
 
- Con posicionamiento vamos a poder poner un elemento en cualquier lado que deseemos
- Position va romper el flujo basico del DOM
- Para que un elemento este posicionado (initial | relative | absolute | fixed | sticky)
- Cuando un elemento esta posicionado , aprende nuevas propiedades
<!--
  top
  right
  bottom
  left
  z-index
-->
 
### RELATIVE
 
- Un element posicionado de manera relative, mantiene sus dimensiones
- La relacion de relative es para dar contexto a un posicionamiento absolute
 
### ABSOLUTE
 
- Un element posicionado de manera absolute,no mantiene sus dimensiones (salvo que las tenga definidas)
- Su contexto es su ancestro posicionado mas cercano
 
### FIXED
 
- Pierde su espacio en el flujo

## FLEXBOX

- Un modelo de layout que fue introducido por W3C
- Incorpora el concepto de cajas flexibles
- Todo flexbox tiene dos ejes (eje principal y eje secundario)
- Eje principal (Main Axis) y Eje secundario (Cross Axis)
- Por default el eje principal es Horizontal, el eje secundario es vertical
- Los flex items son (hijos directos, contenido y pseudoelementos)

## TERMINOLOGIA FLEXBOX

- Flex Container
- Flex Items
- Main Axis
- Cross Axis
- Main Start
- Main End

## EJE PRINCIPAL (MAIN AXIS)

- Justify-content: Propiedad que aplica al eje principal (MAIN AXIS)
- Valores: space-betwen || space-around || space-evenly || flex-start || flex-end || center
- space-between(X)
- space-around(X)
- space-evenly(X)
- flex-start(X)
- flex-end(X)
- center(X)

## EJE SECUNDARIO (CROSS AXIS)

- Align-items: Propiedad que aplica al eje secundario (CROSS AXIS)
- Valores: flex-start || flex-end || center

## CAMBIO EJE
 
- flex-direction