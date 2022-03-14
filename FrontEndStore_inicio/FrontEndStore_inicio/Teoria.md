**BEM**  Block Element Modifier

BEM es una metodologia para crear codigo reutilizable y ordenado en tus proyectos con CSS. Para utilizarlo hay que seguir las convenciones de BEM, gracias a ellas se evita la colision de nombres.

* Reglas de BEM:

    * Bloques: son un contenedor, si una seccion por si sola es significativa y no requiere de otras secciones para su apariencia (CSS) debera ir en un bloque.

        <div class="cliente"> ... </div>

    * Elementos: son parte de un bloque, dependen de bloque y no es por si solo significativo; tienen la caracteristica de que utilizan el nombre del bloque y despues doble guion bajo __ . Por ej. 

        <p class="cliente__nombre"> ... </p>

    En el CSS tendriamos algo asi: .cliente__nombre { ... }

    *  Modificadores: es una bandera que avisa que cierto elemento tendra un diseño diferente. Por ejemplo:

        <p class="cliente__nombre--ceo"> ... </p>

        .cliente__nombre--ceo {...}






