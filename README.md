# Slider-imag CSS (webkit - reset.css - good practice writing code)

Este proyecto se utilizará en la exploración de diversas interpretaciones de estilos css que realizan los navegadores, permitiendo hacer uso de prefijos css para la comprensión especifica de estilos soportados por el navegador, reinicio en blanco de los estilos predominantes de cada navegador con un reset.css y buenas prácticas de escritura en código que facilitaran la interpretación de los estilos aplicados.

<p align='center'>
<a>
<img width='350' src="https://i.imgur.com/hVldPCq.png">
</a>
<br>
<a>
<img width='750' src="https://i.imgur.com/YDRgfHb.gif">
</a>

</p>


## Prefijos y reset.css

La gran variedad de servidores para la navegación web ha requerido de estandarizar constantemente en busca de una armonía en la representación de código en diferentes navegadores web permitiendo interpreta rel código de una forma muy similar en diferentes navegadores.

Dentro de esta interpretación unificada podremos implementar buenas practicas de escritura de código para facilitar esta interpretación, prefijos CSS que permitan ser comprendidos exclusivamente por un navegador en concreto y un archivo reset.css que restaurará los estilos preestablecidos en cada navegador diferente permitiendo partir de una estructura en blanco sin estilos predefinidos.

## Buenas Practicas

1. Organizar la estructura del código de estilos de manera descendiente para facilitar la ubicación de los mismos.

~~~CSS
/****** generic classes*******/
styles goes here…

/****** header *******/
styles goes here…

/****** nav menu *******/
styles goes here…

/****** main content *******/
styles goes here…

/****** footer *******/
styles goes here…
~~~

2. Nombrar correctamente los selectores. No comenzar el nombre de un selector con mayúsculas, números ni caracteres especiales.

~~~sh
Evitar: #1div, .=div, DivContent 

Mejor utilizar: #div1, .div, divContent
~~~

3. Uso de **guiones**. Es recomendable evitar el uso de guiones bajos **"_"** para la construcción de nombres ya que algunos navegadores no lo soportan.

~~~CSS
/* Opción 1: Palabras separadas por mayúsculas */
navMenu { padding: 2em; border: 2px solid green; }

/* Opción 2: Palabras separadas por guiones */
nav-menu { padding: 2em; border: 2px solid green; }
~~~

4. Combinar elementos al declarar estilos. si dos o más elementos compartirán los mismos estilos de **.class** e **#** identificadores.

~~~CSS
div p {  color: red; }
~~~

5. Abreviar los propiedades dentro de una sola declaración.

~~~CSS
/* Propiedades margin-left, margin-right y margin-top */
.nav-menu {margin-left: 5px; margin-right: 5px; margin-top: 5px;}
/* Propiedad abreviada margin */
.ṇav-menu {margin: 5px 5px 0px 5px;}
~~~

6. Probar diseño en diferentes navegadores. Este testeo de implementación arrojara diferentes características a alinear si se requiere una interpretación de estilos similar en todos los navegadores.

7. También se puede hacer uso de la aplicación browserling que te permite ver tu desarrollo en varias versiones diferentes de cada navegador. 

    https://www.browserling.com/

8. Validar estilos mediante herramientas como: 

	*W2C-CSS**

    https://jigsaw.w3.org/css-validator/

9. Y por ultimo agregar prefijos CSS para propiedades de estilos que todavía no son estables.

Existen herramientas como **caniuse.com** que nos indicas el soporte de ciertas etiquetas y estructuras par aque el código sea interpretado como los estilos determinen y no como el navegador permita.

    https://caniuse.com/?search=img

    https://es.stackoverflow.com/questions/372610/los-siguientes-prefijos-siguen-siendo-necesarios-en-css3



## Prefijos CSS

Los prefijos para navegadores se anteponen al estilo CSS destinado a que dicho estilo sea leído y aplicado exclusivamente por un navegador en concreto. 

| Prefijo | Navegador |
| -- | -- |
| -webkit- | Chrome, Safari, Android y iOs |
| -moz- | Firefox  |
| -o- | Opera |
| -ms- | Microsoft Internet Explorer |


###  reset file

Algunos archivos ejemplos de resect.css files son los siguientes:

~~~CSS

/* 
* Reducir fonst-size en 
* este porcentaje en 
* espesifico (62.5%) 
* permitira hacer 
* uso de unidades de 
* tamaños como rem para 
* aproximarlo a un px y que 
* su interpretación sea 
* similar en diferentes 
* tamaños de pantalla
*/
html{
    font-size: 62.5%; 

*{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    list-style: none;
    text-decoration: none;
    border: none;
    outline: none;
}
~~~


~~~CSS

/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}

~~~
