**El rol de CSS**
CSS se va a encargar de dar colores, tamaños, espacios, animaciones todo a la pagina web. Es para darle un buen diseño a las paginas web.

**¿Que es CSS?**
Son hojas de estilo en cascada, que permitiran darle a tu codigo HTML un diseño unico y especial en pocas lineas.
CSS se va a encargar de:
* Tamaños y tipos de fuente
* Colores
* Espacios
* Margenes
* Adaptar diseños a distintos dispositivos.
* Animaciones

**ANATOMIA DE CSS**
Tendremos un selector que debe concordar con nuestro codigo HTML. Las llaves, donde meteremos todo el codigo o propiedades, y un set de valores (propiedad y su valor).
p {
    todo lo que este aqui sera los estilos o codigos css  que se le atribuiran a los parrafos p. Por ejemplo:

    color: blue;  --> se utiliza para darle color al texto, en este caso seria azul. 
}

Para cargar una hoja de estilos y conectarla a nuestro HTML tenemos que crear una etiqueta que se llama <link> el cual va a recibir como atributo un href

<link href = 'css/style.css'> dentro de las comillas va la ruta a la hoja de estilos. Ademas esta etiqueta tambien viene con un atributo que se llama rel que viene por defecto con un valor 'stylesheet' . rel significa la relacion que tiene el link con lo que apunta, en este caso es stylesheet es decir una hoja de estilos..

Para que nuestro sitio web sea mas rapido podemos usar preload

<link rel ='preload' href = 'css/style.css' as ='style'>

**SELECTORES**

* Selector de clase:  una clase se puede crear multiples veces (es reutilizable) e inicia con un punto. Por ejemplo: 

.cliente {
    color: blue;
}


* Selector de ID: puedes tener multiples ID por pagina pero sus nombres no pueden repetirse. Por ejemplo:

#cliente {
    color: blue;
}

* Selector de atributo:  selecciona elementos basado en algun atributo que tengan. Por ejemplo:

[src = 'logo.jpg'] {
    color: blue;
}

* Combinacion de descendentes: selecciona los elementos hijos cuyo padre sea una clase o ID en especifico. Por ejemplo: 

.cliente .nombre {
    color: blue;
}

* Todos los hijos: aplica la siguiente regla a todos los parrafos hijos. Por ejemplo:

.cliente > p {
    color: blue;
}

**ESPECIFICIDAD:**
Si nosotros queremos ser muy especificos con el selector al cual queremos aplicarle un estilo, podemos indicar hasta su clase.. por ejemplo:

Si tenemos un h1 que tiene una cierta clase y ademas tiene un span, podemos ser especificos e indicarla de la siguiente manera:

h1.titulo span {
    Aqui iran todos los estilos que querramos aplicarle al h1 que tenga como clase 'titulo' y ademas tenga un span.
}

La especificidad es como el navegador va a mostrar el CSS de acuerdo a que tan especifico es el selector que hemos creado

CSS es en cascada, eso no significa que si un selector aparece despues sera tomado en cuenta sino mas bien su especificidad. Lo mas importante es su especificidad. Si un elemento tiene un selector mas especifico no importa mucho donde haya sido declarado, CSS decidira por su especificidad. Si queremos pasar por encima de cualquier especificidad le podemos agregar a la propiedad un important al final, asi:

p {
    color: blue!important;
}

**COLORES EN CSS**
En CSS puedes utilizar los colores de muchas formas, podemos indicarlos por nombres, por codigo hexadecimal, por rgb() o hsl(), rgba() y hsla().

Para agregar selectores en la hoja de estilos que no estan en el html los podemos agregar con unos dos puntos al inicio. Asi:

:root {
    root es una forma de almacenar variables de CSS que se las conoce como custom propertys. 
}

**Display Block o Inline:**
Algunos elementos se muestran de una forma y otros de otra..
Todos los elementos en el HTML ya tienen un display por default. 

* display: block; esto significa que el elemento se colocara uno debajo del otro sin importar su tamaño o contenido. Los divs son un ejemplo de esto.

* display: inline; significa que el elemento se posicionara a la derecha una vez que haya tomado el espacio que requiere.. la barra nav es un ejemplo bueno de esto. 

Ningun elemento tiene un display flex o grid por default. No es necesario ademas especificar un display para cada elemento, salvo que desees modificar el que viene por default. 

**Padding**
El padding sirve para engordar el elemento. Todo entero, a diferencia del margin que lo que hace es alejarlo de otro elemento pero sin modificarlo. 

**FLEXBOX:**
Flexbox fue diseñado como un modelo unidimensional para crear layouts. Flexbox tiene dos ejes, solo puede colocar y distribuir tus elementos en una direccion (fila o columna). 

fila --> row. Es aplicado por default al definir un display: flex;
Los otros valores son row-reverse, column y column-reverse.

Si elegimos row o row-reverse los elementos hijos se colocaran de izquierda a derecha uno junto a otro. 

Al elegir column o column-reverse los elementos se colocaran de arriba hacia abajo. 

Flexbox es especialmente diseñada para alinear elementos en tus diseños. No añade efectos de animaciones, ni textos. Es una tecnologia utilizada unicamente para los layouts y sustituye a los floats o table-cell.

**¿COMO ESCRIBIR CODIGO CSS?**
Existen diferentes formas de escribir codigo CSS: BEM, Utility First o Modulo. Si el proyecto tiende a ser grande es buena idea utilizar cualquiera de los 3. 

* BEM: bloques, elementos, modificadores. Basicamente el codigo css tendria un bloque que lo definiria con una clase principal y luego vas describiendo cada uno de los elementos que vas teniendo. Por ejemplo: 

   .card {}  El card seria el bloque
   .card__titulo {} 
   .card__imagen {} 
   .card__boton {} Estos tres serian elementos.
   .card__boton--activo {} Esto es modificador. 

* Utility First: basicamente creas clases con una sola propiedad que describe que es lo que haria. Por ejemplo, si queres centrar el texto harias lo siguiente: 

.text-center { aqui dentro el codigo para centrar el texto }

Si queres tener tu paleta de colores:

.color-red-100{}

O si queres poner un color de fondo: 

.bg-blue-200 {}

Esto termina siendo mucho codigo, pero se usa mucho..

* Modulos: defines el contenido principal, y despues vas seleccionando cada uno de los elementos html. Defines como una clase padre y luego vas seleccionando cada una de las etiquetas html.

.card {}
.card h2 {}
.card img {}
.card a {}

Es posible utilizar mas de 1 enfoque en un mismo proyecto.

**Responsive Web Design**

Esto es basicamente hacer que tu sitio web adaptable a diferentes dispositivos. Todos los usuarios navegan desde diferentes dispositivos. 

Google penaliza a los sitios webs que no se adaptan a diferentes dispositivos. La solucion para evitar crear multiples sitios web y que sean adaptables a una gran cantidad de dispositivos es: Resposive Web Design con Media Queries. 

* ¿que es Responsive Web Design? 

    Es un enfoque que nos dice que nuestros diseños deberan adaptarse a las interacciones del usuario y la resolucion que utilizan. Los sitios deberan adaptarse a celulares, tablets, laptops, computadoras de escritorio, y televisores. 

* ¿Como logro que mi sitio web sea responsive?

    Con Media Queries. Con la sig sintaxis:

    @media (min-width:768px) {

    }
    @media (min-width: 992px) {

    }


480px --> este va a cambiar cuando el dispositivo que use el usuario sea un telefono celular. 

768px --> este es el de una tablet. 

1140px ---> este sirve bien para una notebook o una computadora de escritorio..

1440px --> para cosas mas grandes. Tambien se usa

**CSS Box Model**

Todo en CSS es una caja, pero como sea esa caja depende de 4 cosas

* ¿Que es CSS Box Model? El tamaño de lo que se muestra en pantalla esta delimitado por 4 cosas: tamaño de contenido, tamaño de relleno (padding), tamaño del borde y el margen.  

Si tienes el siguiente selector: 

.cliente {
    padding: 20px;
    width: 200px;
    border: 10px solid red;
}

Tu elemento medira 260px: 200 del width, 40 del padding y 20 del border. 

**CSS Grid**

CSS Grid te permite definir la ubicacion y tamaño de los elementos de tu sitio web. Mientras que en flexbox el contenido crece automaticamente, en CSS Grid el contenido se agrupa dentro de un area definida. En cierta forma es como una tabla de HTML, con la ventaja de mayor flexibilidad y control sobre tu diseño. Porque en flexbox solo tiene acceso o control de una sola dimension (row o column), en cambio en CSS Grid tienes acceso a dos dimensiones.

* ¿CSS Grid es mejor?

    Algunos diseños son mas faciles en CSS Grid que en flexbox, y otros son mas sencillos en flexbox que en CSS Grid. Los puedes utilizar juntos en un mismo diseño. 

* ¿Como decidir si utilizar CSS Grid o Flexbox?

    Utiliza Flexbox para la alineacion o distribucion de los elementos que estaran dentro de contenedores.
    Por ejemplo una barra de navegacion con algunos enlaces.

    Utiliza CSS Grid para definir el layout de tu sitio web, como pueden ser las columnas o contenedores de elementos. Cuando tenga un diseño que tenga que distribuir diferentes areas es mejor utilizar CSS Grid. 

    Utiliza Floats cuando pudas mover tus orejas sin tocarlas, osea nunca, o cuando debas crear un sitio web que se vea bien en internet explorer 6.. osea nunca.



