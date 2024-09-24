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

<!-- Actualizar el repositorio con lo visto en la 2da parte
  1) Explicar los conceptos con ejemplos
  2) (Agregar una nueva tipografia de google fonts, usando font-face)
-->