HTML es facil
Tiene una sintaxis clara y facil

<p> = parrafos
<nav> = Navegaciones
<header> = encabezado del sitio web o el elemento
<main> = contenido principal de la app
<footer> = pie de pagina o elemento

**ESTRUCTURA DE HTML**

<html>
    <head>
        Aqui colocas informacion que el navegador puede entender, como interpretar esta pagina. Por ej:

        <title> Mi pagina Web </title>
    </head>


    <body>
        Aqui va lo que es importante para el usuario, lo que el usuario tiene que ver. 

        <p> Contenido de mi pagina </p>
    </body>
</html>

HTML es un lenguaje, pero no de programacion. Es un lenguaje para darle estructura a los sitios web.

Cuando inicias un nuevo archivo .html si tocas ! y enter visual studio code te entrega todo un formato de html ya armado, con un head y un body. 

<h1> va a definir una importancia mayor en el contenido. No deberia haber dos h1. 
<h2> es de menor importancia que el h1 y de menor tamaño. A partir del h2 al h6 va bajando la importancia y el tamaño de la letra. Pueden repetirse ademas. Lo recomendable es usar hasta h3.

**¿Que significa estructurar el codigo HTML?**

Significa separar las diferentes secciones de una pagina en especifico. Por ejemplo, el header, la navegacion, etc. 
Estructurar es muy similar a agrupar. 

**ETIQUETAS PARA AGRUPAR**
<footer> parte inferior, pie de pag.      <section> para secciones, se puede usar multiples.
<header> parte superior, encabezado       <article> Si tenemos entradas de blogs o noticias
<nav> barra o menu de navegacion           <aside> barras laterales
<main> para definir el contenido principal. <div> se usa cuando no podes usar los otros.

Dentro de la etiqueta de apertura <a> podemos poner un href='' que va a hacer referencia a donde queremos que se dirija nuestra app cuando clickeemos en nuestro boton. href es un atributo de html. Cuando tenemos mas de un enlace es necesrio que metamos todas esas etiquetas html en una etiqueta de barra de navegacion. Si solo tenemos un enlace eso no es necesario..

class es otro atributo que le podemos dar a cualquier etiqueta de html. 

**¿Como crear formularios HTML?**

Siempre que tengamos un formulario con diferentes campos tenemos que usar una etiqueta que se conoce como form. Eso va a indicar que todo lo que este adentro pertenece a ese formulario, y esos datos si los configuramos de cierta forma podemos enviarlos a un servidor para insertarlo en una base de datos. O compararlo con la base de los registros para verificar ciertos datos..

Lo primero que hay que hacer es definir un fieldset, dentro del cual tendremos un legend (donde indicaremos al usuario que tiene que hacer) el cual va a tener un cierto diseño

Para definir uno de los campos como por ejemplo el nombre podemos usar label
Luego input para que nos defina un espacio donde el usuario pueda ingresar el nombre
la etiqueta input tiene varios tipos de campos:

Por ejemplo:
<input type = 'text' > este es el default, en el podemos escribir cualquier cosa.
<input type = 'checkbox' > ese es para habilitar o deshabilitar. O si queremos marcar varias opciones de una misma lista. 
<input type = 'radio' > Este es para seleccionar una opcion o otra. Pero solo una.
<input type = 'tel' > Es similar al de text, con la diferencia que si se usa en un celular la app, cuando seleccionas para escribir en el cuadro de texto en ves de abrirte el teclado alfabetico te abre el de numeros, para que coloques numeros, en ves del teclado completo.
<input type = 'email' > Este sirve para lo mismo que text pero agrega al teclado una arroba para que sea mas facil escribir el mail. 
<input type = 'number' > Solo podes escribir numeros, y verifica que lo que coloques tenga formato de numero. 

A parte de eso:

<input type = 'text' placeholder = '' > Al agregarle el placeholder, eso hara que en el cuadro de texto en el que el usuario vaya a escribir cosas, figure como ya escrito o un poco visible lo que nosotros le pasemos en las comillas. Eso puede ser un indicador de lo que el usuario deberia ingresar en dicho campo como Tu nombre o cosas asi..

Para agregar un campo donde el usuario puede escribir una mayor cantidad de texto, hay que usar textarea.

Para enviar el mensaje se puede usar un input o un button. 

