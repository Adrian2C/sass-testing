//para empezar a trabajar con Sass se debe instalar el servicio de sass
//npm i sass

//se crea el archivo sass ( o carpeta con archivo dentro)
//se hace el watch de sass, y luego se vincula el style.css al html


esto se divide en :
-el archivo principal que recibe todos los estilos, partials, etc
-carpeta Components --> van los colores, partials pequeños
-carpeta pages --> paginas internas
-vars --> variables de colores, tipografia, etc


//los partial son bloques que se pueden añadir a tu sitio como un card, nav, header, un boton, etc
//estos se crean con "_nombre" y se utilizan en el lugar que desees agregarlo como "@use _nombre"


//use y forward

//forward --> no tiene variables ni mixins  (va para el main y rejunte de archivos)
//use --> tiene variables o mixins (va para editar bloques, o partes de la pagina) y se debe insertar al inicio del archivo .scss, y luego se usa como variable
    ej: @use ../color.scss as c
    y antes de cada variable se pone la c  --> c.$color

// --------------------------
//primeramente se importo fuentes
//se declaran las variables


//se resetea los estilos

//y se añade los estilos globales

//luego se va a los mas especializados y se hace el nesting de las clases y subclases

CREARLAS VARIABLES ROOT N UNA CARPETA
//$COLOR, ETC

// ----------------------- 
para hacer use o forward, se hace en el archivo que se quiere recibir.

-para traer archivos de una carpeta al main.scss, se hace con forward si no tiene variables o mixins, como pedazos de codigo
-para traer variables, hacia otro archivo scss, se usa @use 
//-------------------------

-mixins, son codigos creados exclusivamente para reutilizar a lo largo del codigo

se escriben 
--> @mixin nombreMixin{
    codigo
}

y para usarlo, se pone dentro del codigo que queremos con @include 
-->
.nombreClase{
    @include nombreMixin;
    colro:red;
    etc
}

//--------------

@extend--> nos permite reusar una configuracion css en otra propiedad. esta es util si las propiedades son casi identicas, salvo alguna q otra modificacion

.btn{
    color:red;
    padding:20px;
}
.btn2{
    @extend .btn;
}

//-----------------


