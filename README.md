Apuntes HTML

HTML

HTML es el lenguaje que se utiliza para crear la estructura de una página web.
Sirve para organizar el contenido, no para darle estilo.
Con HTML se colocan textos, imágenes, enlaces, listas, tablas y formularios.

Un archivo HTML suele tener la extensión .html.

Estructura básica de un documento HTML:

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Título de la página</title>
</head>
<body>
</body>
</html>

La etiqueta html es la principal.
Dentro de head se pone información que no se ve.
Dentro de body se pone todo lo visible.


ETIQUETAS DE TEXTO
Las etiquetas h1 a h6 sirven para títulos.
h1 es el título principal.
h2 y h3 se usan para subtítulos.

La etiqueta p se usa para párrafos.
Cada p hace un salto de línea automático.

La etiqueta br hace un salto de línea manual.
No es recomendable abusar de ella.

LISTAS
Las listas no ordenadas usan ul y li.
Las listas ordenadas usan ol y li.

ENLACES
La etiqueta a sirve para crear enlaces.
Se usa el atributo href para indicar el destino.


IMÁGENES
Las imágenes se insertan con la etiqueta img, es obligatorio usar el atributo alt.

FIGURE Y FIGCAPTION

Figure sirve para agrupar una imagen.
Figcaption sirve para poner un pie de foto.


(figcaption lo he usado para hacer mi web de turismo en Paris para poner los pie de foto en laas noticias).

CSS
CSS significa Cascading Style Sheets.
Sirve para dar estilo a las páginas HTML.
Con CSS se cambian colores, tamaños, márgenes y posiciones.
CSS se puede usar de tres formas:
CSS en línea.
CSS interno.
CSS externo (el recomendado).

SINTAXIS DE CSS

selector {
    propiedad: valor;
}

SELECTORES

Selector por etiqueta.
Selector por clase.
Selector por id.

BOX MODEL
Todos los elementos tienen:
content
padding
border
margin

DISPLAY
display block
display inline
display none

FLEXBOX
Flexbox se usa para colocar elementos en fila o columna.
display flex activa flexbox.


GRID
Grid se usa para crear layouts por columnas.
display grid activa grid.


RESPONSIVE

Media queries se usan para adaptar la web a móviles.

CSS DE EJEMPLO USADO EN EL PROYECTO

{
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
}

.layout {
    display: grid;
    grid-template-columns: 1fr 3fr 1fr;
}

.menu {
    background-color: #2c3e50;
    color: white;
}

HISTORIA DE CSS 
CSS apareció para solucionar el problema de mezclar el contenido con el estilo en las páginas web. Al principio todo se hacía dentro del HTML y era difícil de modificar y mantener.

El W3C recibió varias propuestas para crear hojas de estilo y finalmente se eligieron dos ideas principales. Una de ellas fue Cascading HTML Style Sheets, propuesta por Håkon Wium Lie en 1994, y otra fue Stream-based Style Sheet Proposal. A partir de estas propuestas nació lo que hoy conocemos como CSS.
La primera versión fue CSS Level 1, que se propuso como estándar a finales de 1996. Esta versión permitía cambiar colores, tipos de letra, márgenes y tamaños básicos.
En mayo de 1998 se publicó CSS Level 2, que añadió mejoras importantes como un mejor posicionamiento de los elementos y soporte para diferentes dispositivos. Más adelante, en el año 2008, se revisó esta versión y se publicó CSS 2.1, que es una versión más estable y corregida.
Actualmente se trabaja con CSS3 no es una versión única, sino que está dividida en módulos. Cada módulo se encarga de una parte del diseño, como los colores, los selectores, las animaciones o el diseño adaptable.
Gracias a CSS3 se pueden crear diseños más modernos y visuales, con animaciones, transiciones y páginas que se adaptan a móviles y tablets sin necesidad de usar otros lenguajes.


CSS Ventajas e inconvenientes
CSS tiene varias ventajas cuando se usa para dar estilo a una página web.
Una de las principales es que el código se puede mantener mejor y es más fácil de modificar.
A nivel de diseño, CSS es mucho más potente que usar solo etiquetas de HTML.
Además, es un lenguaje bastante sencillo de aprender.
Con CSS se pueden crear diferentes hojas de estilo para un mismo documento HTML.
Por ejemplo, una hoja para ver la web en el ordenador y otra distinta para imprimirla.
También permite reutilizar los estilos en diferentes páginas web.
El principal inconveniente de CSS es que no todos los navegadores interpretan las hojas de estilo de la misma manera.
Esto obliga muchas veces al programador a adaptar el CSS o crear varias versiones para que se vea bien en todos los navegadores.

CSS Ubicación
Los estilos CSS se pueden aplicar a los elementos HTML de diferentes formas, dependiendo de dónde se escriba el código CSS.

El estilo inline se escribe directamente en la etiqueta HTML usando el atributo style.
Las propiedades CSS se aplican solo a ese elemento.
Ejemplo de un párrafo centrado y de color rojo usando estilo inline:
<p style="text-align:center; color:red">Paràgraf centrat vermell</p>

El estilo interno se escribe dentro de la etiqueta style que va en la cabecera head del documento HTML.
Las reglas CSS se aplican a todos los elementos que coincidan con el selector.
<style>
    p {
        text-align: center;
        color: red;
    }
</style>

El estilo externo consiste en escribir las propiedades CSS en un archivo aparte con extensión .css.
Luego, ese archivo se enlaza desde el documento HTML usando la etiqueta link dentro de head.
<link rel="stylesheet" href="estils.css" type="text/css">
p {
    text-align: center;
    color: red;
}

CSS Prioridad
Puede pasar que varias reglas CSS afecten al mismo elemento HTML.
Cuando ocurre esto, CSS sigue un orden de prioridad para decidir qué estilo se aplica.

Estilo externo
Primero se mira si hay una hoja de estilos externa asociada al documento HTML.

Estilo interno
Si hay estilos definidos dentro del head del documento HTML, estos tienen prioridad sobre el estilo externo si hay contradicción.

Estilo inline
Por último, si el estilo está escrito directamente en la etiqueta HTML usando style="", este tiene la mayor prioridad y sobrescribe a los anteriores.

Selector universal * → no suma casi nada
Selectores de etiqueta (p, h1, div)
Selectores de clase, atributos y pseudoclases (.clase, [type="text"]:hover)
Selectores de id (#id)
Estilo inline (style="") es el que más prioridad tiene.

Sintaxis básic CSS
Una hoja de estilos CSS es un conjunto de reglas que sirven para definir el aspecto final de los documentos HTML.
Cada regla CSS está formada por:
Un selector
Un conjunto de declaraciones
Una declaración está formada por:
Una propiedad
Un valor
El selector indica a qué elemento o elementos HTML se les va a aplicar el estilo.
Las declaraciones definen cómo se verá ese elemento.

p {
    font-size: 10pt;
    background-color: gray;
}

Los comentarios en CSS:
Empiezan con /*
Terminan con */
Pueden ocupar una o varias líneas
En CSS solo existen comentarios de bloque, no hay comentarios de una sola línea como en otros lenguajes.
/* CSS */

En CSS se pueden agrupar selectores para no repetir el mismo código varias veces.
Si queremos aplicar el mismo estilo a varios elementos, como por ejemplo h1 y p, podríamos hacerlo así:

h1 { color: red; }
p { color: red; }

En CSS existen distintos tipos de selectores.
Cada selector sirve para aplicar estilos a una parte concreta del HTML.

Los selectores básicos son:
Selector de elementos (o selector de tipo)
Se usa para aplicar estilos directamente a una etiqueta HTML, como p, h1, div, etc.

Selector de id
Se usa para aplicar estilos a un elemento concreto que tenga un id.

Selector de clase
Se usa para aplicar estilos a uno o varios elementos que compartan la misma clase.

También existen selectores avanzados;
Selector universal
Selectores de atributos
Selectores de hijos
Selectores de descendientes
Selectores de hermanos adyacentes
Pseudoclases
Pseudoelementos

El selector de elementos se aplica a todos los elementos de ese tipo que haya en la página.

a {
    color: red;
}

Selector de id:
El selector de id se utiliza para aplicar estilos a un elemento concreto que tenga un atributo id con un valor específico.
En CSS, los selectores de id se escriben usando el símbolo #.
#example {
    property: value;
    property2: value2;
}
Este selector afectará al elemento HTML que tenga el atributo:
<p id="example">Texto de ejemplo</p>

Selector de clase
El selector de clase se utiliza para aplicar estilos a todos los elementos que tengan el atributo class con un valor determinado.
En CSS, los selectores de clase se escriben usando un punto ( . ) delante del nombre de la clase.

.example {
    property: value;
    property2: value2;
}

una clase se puede repetir en varios elementos

<p class="example"></p>
<li class="example"></li>
<div class="example"></div>

Selector universal
El selector universal sirve para seleccionar todos los elementos de la página web.
Se representa con el símbolo *.
En el ejemplo, se indica que todos los elementos del documento HTML tendrán un borde negro sólido de 1 píxel.

*{
    border: 1px solid #000000;
}

Selectores de atributos
Los selectores de atributos permiten seleccionar elementos HTML según los atributos que tienen.
En el primer ejemplo, se seleccionan todas las imágenes:
img[alt] {
    border: 1px solid #000000;
}

También se puede seleccionar según el valor concreto del atributo.
img[src="alert.gif"] {
    border: 1px solid #000000;
}

Selectores de hijos
Los selectores de hijos sirven para seleccionar elementos que son hijos directos de otros elementos.
Por ejemplo, esta regla aplica color azul a los elementos strong que sean hijos directos de un h3:
h3 > strong {
    color: blue;
}

Selectores de descendientes
El selector de descendientes es parecido al selector de hijos, pero con una diferencia importante:
El selector de hijos solo selecciona hijos directos.
El selector de descendientes selecciona elementos que estén en cualquier nivel dentro del elemento, no solo los directos.

<div>
    <em>hello</em>
    <p>In this paragraph I will say <em>goodbye</em></p>
</div>


El div tiene dos hijos:
Un em
Un p

div > em {
    /* estilo */
}

En cambio, si usamos un selector de descendientes, se seleccionan todos los elementos em que estén dentro del div, estén donde estén:
div em {
    /* estilo */
}

Selectores de hijos
El selector de hijos solo afecta a los elementos que son hijos directos de otro elemento.
Se escribe usando el símbolo >.

div > em {
}

Selectores de descendientes
El selector de descendientes afecta a todos los elementos que estén dentro de otro, sin importar el nivel.
Se escribe sin el símbolo >, solo con un espacio.

div > em {
}

Selectores de hermanos adyacentes
Los selectores de hermanos adyacentes permiten seleccionar un elemento que aparece justo después de otro elemento y que está al mismo nivel en el HTML.
Se utiliza el símbolo +.

<h1>Encabezado 1</h1>
<h2>Encabezado 2 (hermano adyacente)</h2>
<h2>Encabezado 2 (hermano no adyacente)</h2>

Definimos la regla siguiente:

h1 + h2 {
    margin-top: -5mm;
}

Pseudoclases
Las pseudoclases se usan para aplicar estilos según el estado de un elemento, no al elemento en sí.
Las pseudoclases:
:link
Es el estado normal del enlace, cuando todavía no se ha visitado.
:visited
Enlaces que ya han sido visitados por el usuario.
:focus
Enlaces o campos de formulario que tienen el cursor activo en ese momento.
:hover
Cuando el puntero del ratón está encima del enlace.

Pseudoelementos
Los pseudoelementos, igual que las pseudoclases, no afectan a todo el elemento, sino que permiten aplicar estilos a una parte concreta del mismo.

p::first-line {
    color: red;
}

COMPOSICIÓN. Márgenes, bordes y relleno en CSS
Muchos elementos de HTML, como los elementos div y los encabezados, se representan por defecto ocupando todo el ancho del lienzo del navegador y fuerzan un salto de línea al final, de manera que una serie de estos elementos se mostraría como una pila, uno sobre otro, en el lienzo del documento.
El control del espacio en blanco en las hojas de estilo predeterminadas de los navegadores no es adecuado en la mayoría de los casos, por lo que los especialistas en estilos acostumbran a usar a menudo los márgenes (margin), bordes (border) y relleno (padding), junto con otras propiedades CSS, que ayudan a componer el documento de forma adecuada.

Margin (margin)
El margin representa el área transparente que rodea la caja, es decir, el espacio que la separa de los elementos contiguos.
La propiedad margin se puede usar como propiedad global o desglosarse en cuatro propiedades:
margin-top → margen superior
margin-right → margen derecho
margin-bottom → margen inferior
margin-left → margen izquierdo

píxeles, por ejemplo: 2px
referencia al valor del font-size del elemento actual: 1em
referencia al valor del font-size del elemento <html>: 1rem
porcentaje: 5%
automático: auto

Los bordes representan el estilo que tendrán los bordes del elemento.
border: border-width || border-style || border-color || inherit;
os bordes superior e inferior de un elemento en línea pueden solaparse dependiendo del valor de la propiedad line-height.
La propiedad border se puede dividir en cuatro propiedades:
border-top
border-right
border-bottom
border-left
El estilo del borde (border-style) puede tener los siguientes valores:
none
hidden
dotted (punteado)
dashed (discontinuo)
solid (sólido)
double
groove
ridge
inset
outset
inherit

Relleno (padding)
El padding es el espacio entre el borde del elemento y su contenido.
De la propiedad padding, al igual que las otras propiedades anteriores, se derivan cuatro propiedades específicas para cada lado:
padding-top
padding-right
padding-bottom
padding-left
Aspectos importantes del padding:
El valor del padding nunca puede ser negativo.
El estilo del padding es transparente.

Margin: es el espacio exterior que rodea al elemento y lo separa de otros elementos.
Border: es el borde que envuelve al elemento.
Padding: es el espacio interior entre el borde y el contenido.
Content: es el contenido real del elemento.

Acortar los valores de padding:
Un solo valor:
padding: 5%;
padding: 10px;

Dos valores:
padding: 10px 20px;

Tres valores:
padding: 10px 3% 20px;

Cuatro valores:
padding: 1px 3px 30px 5px;

Reglas de posicionamiento
En CSS hay varias reglas que sirven para controlar cómo se colocan y se comportan los elementos dentro de la página.
Algunas de las más importantes son:
display: block
Dimensionamiento de bloques: width, height, padding y border
box-sizing: content-box y border-box
Desbordamiento de contenidos: overflow y text-overflow
position: static, relative, absolute, fixed y sticky
display: flex

Un elemento puede mostrarse como:
block
inline
flex
grid
o puede estar oculto
Por defecto, muchos elementos HTML usan display: block.
Los elementos de tipo bloque ocupan todo el ancho disponible y hacen un salto de línea antes y después.
Cuando un elemento tiene display: block, su tamaño final se calcula teniendo en cuenta:
width
height
padding
border
display: block
box-sizing: content-box
box-sizing: border-box;

<body>
  <section class="container">Esto es un botón</section>
</body>

.container {
  width: 100px;
  height: 100px;
  background: #FFFFFF;
  padding: 10px;
  border: 10px solid #FF0000;
}

section {
  display: block;
  box-sizing: content-box;
}

{
  box-sizing: border-box;
}

body {
  margin: 0;
}

Desbordamiento (overflow)
overflow: hidden
Oculta el contenido que se desborda del contenedor, no se ve en ningún caso.
overflow: scroll
Recorta el contenido y el navegador muestra barras de desplazamiento siempre, aunque no hagan falta.
overflow: auto
El navegador decide si mostrar o no las barras de desplazamiento.
Si el contenido no se sale, no aparecen.
En dispositivos móviles suele comportarse de forma diferente según el navegador.

overflow: hidden
Oculta el contenido que se desborda del contenedor, no se ve en ningún caso.
overflow: scroll
Recorta el contenido y el navegador muestra barras de desplazamiento siempre, aunque no hagan falta.
overflow: auto
El navegador decide si mostrar o no las barras de desplazamiento.
Si el contenido no se sale, no aparecen.
En dispositivos móviles suele comportarse de forma diferente según el navegador.

.container {
  width: 150px;
  height: 150px;
  background: #FFFFFF;
  padding: 10px;
  box-sizing: border-box;
  font-size: 48px;
}

text-overflow: clip
Valor por defecto. El texto se corta sin mostrar nada más.
text-overflow: ellipsis
Si el texto no cabe, se corta y se añaden tres puntos … indicando que continúa.

.container {
  width: 150px;
  height: 150px;
  background: #FFFFFF;
  padding: 10px;
  box-sizing: border-box;
  overflow: hidden;
  text-overflow: ellipsis;
}

display: flex

Estos métodos funcionaban, pero no se adaptaban bien a los diseños actuales, donde hay distintos tamaños de pantalla, móviles, tablets y diferentes resoluciones.
Flex (o flexbox) es un sistema de elementos flexibles que permite que los elementos HTML
se adapten y se coloquen automáticamente, haciendo que sea más fácil personalizar el diseño de una página web.

Contenedor
Es el elemento padre. Dentro de él se colocan los elementos flexibles.
Item
Son los elementos hijos que están dentro del contenedor flex.
Eje principal
Es la dirección principal en la que se colocan los items.
Por defecto, el eje principal es horizontal (en fila).
Eje secundario
Es el eje perpendicular al eje principal.
Si el eje principal es horizontal, el secundario será vertical, y al revés.

display: flex
Activa el modo flex y convierte a los hijos en elementos flexibles.

flex-direction
Indica la dirección del eje principal.
Puede ser:
row (por defecto, en fila)
column (en columna)
row-reverse
column-reverse
flex-wrap
Indica si los elementos pueden bajar a otra línea.
nowrap 
wra
wrap-reverse
justify-content
Alinea los elementos en el eje principal.
flex-start
center
flex-end
space-between
space-around
space-evenly
align-items
Alinea los elementos en el eje secundario.
stretch (por defecto)
flex-start
center
flex-end
baseline
align-content
Alinea las filas cuando hay varias líneas de elementos.


Propiedades de children
order
Cambia el orden de los elementos sin modificar el HTML.
flex-grow
Indica cuánto puede crecer un elemento respecto a los demás.
flex-shrin
Indica cuánto puede reducirse un elemento si no hay espacio.
flex-basis
Define el tamaño inicial del elemento antes de repartir el espacio.
align-self
Permite alinear un solo elemento de forma diferente al resto.

diseño responsive
El diseño responsive es una técnica de diseño web que permite que un sitio web se adapte automáticamente a diferentes tamaños de pantalla y dispositivos, como ordenadores, tablets y teléfonos móviles.
El contenido y la estructura cambian según el tamaño de la pantalla para que la web se vea bien en todos los dispositivos.

Flexible y adaptable
El diseño y los elementos (como texto, imágenes y menús) se ajustan al tamaño del dispositivo.
Media queries
Se usan para aplicar estilos específicos según el ancho, alto u otras características de la pantalla.
Rejillas fluidas
Los tamaños de los contenedores se basan en porcentajes en lugar de valores fijos.
Imágenes y fuentes escalables
Se ajustan para mantener la proporción y la legibilidad en diferentes dispositivos.

Media queries
En pantallas grandes (escritorio):
El fondo es azul.
En pantallas medianas (tablets):
El fondo es verde.
En pantallas pequeñas (teléfonos):
El fondo es amarillo.





















