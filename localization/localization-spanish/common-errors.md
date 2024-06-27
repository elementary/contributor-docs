# Errores comunes y comportamientos a evitar cuando traduzca al español en elementary

Aquí exponemos algunas prácticas no recomendadas que pueden causar problemas al hacer traducciones correctas para elementary.

## Evite expresiones locales o coloquiales del español

El fundamento de esta recomendación es que la traducción de elementary se pretende ser para un español internacional. Significa que se deben evitar palabras, jergas y expresiones locales que no sean universales en la región hispanoamericana.

Esto es más difícil de lo que parece, ya que cada región tiene expresiones que, aunque pueden sonar bien en una zona, sonarán mal o fuera de tono en otra. La recomendación aquí es utilizar fuentes como el [diccionario de la lengua española RAE](https://dle.rae.es/) para obtener información sobre una palabra o expresión y observar si es algo específico de una región o no.

Por esta misma razón, se debe ser lo más neutral posible al expresarse al usuario. Se debe evitar tanto el voseo y el tuteo, como formas coloquiales de referencia al usuario, por la misma razón expuesta anteriormente.

## Ejemplo

Este texto:

> Type to test your settings
>
> You’re connected!

Se traduciría a:

> Escriba para probar su configuración
>
> ¡Está conectado!

No se permiten formas como:

> Escribe para probar tu configuración
>
> ¡Estás conectado!


> Escribí y probá tu configuración
>
> ¡Vos estáis conectado!


## ¡Tenga cuidado con el presente progresivo en inglés!

El presente progresivo no siempre se debe traducir literalmente al español. Muchas veces en inglés, aunque se use esta conjugación, se está indicando algo en tiempo presente, futuro, o el verbo en infinitivo. 

En resumen, la terminación _-ing_ no necesariamente representa un verbo terminado en «-ando» o «-iendo».

### Ejemplo

El siguiente texto:

> After restarting you can set up a new user, or you can shut down now and set up a new user later.

Se traduciría a:	

> Después de reiniciar, puede configurar una cuenta de usuario nueva, o puede apagar ahora y configurarla más tarde.

Nótese que utilizar el verbo _restarting_ como «reiniciando» no tendría sentido en esta frase, es necesario usar el verbo en infinitivo para que funcione.

## Evite el uso de comillas inglesas o sencillas

En español, las comillas inglesas (“, ” o ") o comillas sencillas (` o ') no se utilizan a menos que sea absolutamente necesario. De manera predeterminada, siempre usaremos comillas españolas o angulares (« y ») para textos comunes para el usuario.

Excepciones para utilizar las comillas inglesas o de hacker son:

* Secciones de código de ejemplo de lenguajes de programación como Vala, donde la sintaxis exige el uso de comillas inglesas o comillas simples.
* Etiquetas de navegador internas del lenguaje HTML, Markdown que exigen el uso de comillas simples y no se pueden cambiar. De lo contrario, el formato de estos lenguajes se rompería.

En Linux, estos caracteres se pueden escribir con la combinación de teclas Alt Gr + Z y Alt Gr + X, respectivamente, con las distribuciones de teclado hispanoamericanas con teclas muertas. En Windows esto se realiza con la combinación Alt + 174 y Alt + 175, respectivamente.

El sitio web de Weblate también ofrece botones que pueden ser presionados con el ratón para colocar estos caracteres.

### Ejemplos

### Ejemplo uno

El texto:

> The program "io.elementary.calendar" may not be installed

Se traduce a:

> Es posible que el programa «io.elementary.calendar» no esté instalado

### Ejemplo dos

> Take this time to read the \<a href="/docs/learning-the-basics">getting started\</a> guide to learn about your new operating system.

Se traduce a:

> Dedique un momento a leer la \<a href="/docs/learning-the-basics">guía de primeros pasos\</a> para aprender a utilizar su nuevo sistema operativo.
 
Nótese que no se traducen las comillas de la etiqueta HTML, ya que es una exigencia para que funcione correctamente y la dejamos como está.

## Evite reemplazar las etiquetas de programación o HTML de un texto

Las etiquetas HTML y otros aspectos de código HTML (o de lenguajes de programación como Vala) tienen una exigencia de sintaxis que no debe ser alterada, ya que rompería el formato HTML y puede causar problemas. Estas partes del texto nunca deben ser traducidas.

### Ejemplo

> You can also secondary-click a window's header bar and choose \<strong\>Resize\</strong\> or press \<kbd\>Alt\</kbd\>\<kbd\>F8\</kbd\> to enter resize mode.

Se traduce a:

> También puede hacer clic con el botón secundario en la barra de encabezado de una ventana y elegir \<strong\>Redimensionar\</strong\> o presionar \<kbd\>Alt\</kbd\>\<kbd\>F8\</kbd\> para ingresar al modo redimensionar.

Nótese que las etiquetas _\<strong\>_ y _\<kbd\>_ no se traducen. Se conserva su estructura para que el formato HTML dibuje correctamente el resultado final.

## Evite el uso excesivo de los adverbios (es decir, de palabras con «...mente» al final)

Ejemplos de palabras pueden ser _actualmente, automáticamente, momentáneamente, especialmente, nuevamente, accidentalmente, permanentemente, etc_.

Estas palabras no tienen nada malo _per se_. Lo que ocurre es que es muy común abusar de ellas, resultando en una traducción llena de este tipo de palabras.

El uso de estas palabras es más tolerable en secciones de documentación o notas de versión. Pero es preferible intentar encontrar alternativas cuando se trata de elementos de interfaz de usuario.

Sin embargo, esta no es una regla inmutable. Es posible que en algunos casos no se pueda evitar usar el adverbio, e incluso puede ser la mejor palabra dado el contexto. Pero se recomienda al menos tratar de encontrar alternativas si se siente que la traducción no se beneficia de la palabra actual.

### Ejemplo

Por ejemplo este texto del complemento de sonido de la Configuración del Sistema:

>No applications currently emitting sounds. Applications emitting sounds will automatically appear here.

Si lo traducimos con las palabras terminadas en «...mente» obtendríamos algo como esto:

> No hay aplicaciones emitiendo sonidos _actualmente_. Las aplicaciones que emitan sonidos aparecerán aquí _automáticamente_.

Nótese que hay mucha redundancia y aliteración con el uso excesivo del adverbio. Una traducción un poco mejor sería algo como esto:

> No hay aplicaciones emitiendo sonidos _en este momento_. Las aplicaciones que emitan sonidos aparecerán aquí _de forma automática_.

## Evite el exceso de cortesía en el español

El español en herramientas técnicas, como aplicaciones y sistemas operativos, no se usan tantas palabras de cortesía, a diferencia del inglés. Muchas veces se considera superfluo e innecesario agregar estos detalles en español, resultando molesto (precisamente, la intención contraria de lo que desea).

En particular, el uso de _please_ en inglés es muy común, pero que en español se suele omitir. Por lo general, el imperativo en español suena mejor a la hora de pedir aclaraciones o solicitar acciones.

Una excepción a esta regla es cuando se hacen preguntas al usuario para realizar o confirmar una acción. En esta situación es recomendable utilizar la cortesía, en particular el uso del verbo «desear» y preguntar confirmaciones con «está seguro que...». Estamos prefiriendo el verbo «desear» sobre otros como «querer» y «está seguro que...» sobre «confirma que...».

Otra excepción también surge cuando es claro que es un error o dificultad que está fuera del control del usuario o del sistema.

Finalmente, es recomendado también enviar la cortesía al referirse a elementos del usuario y evitar la segunda persona. Por ejemplo, _your message_ es preferible traducirlo a «el mensaje» en vez de «su mensaje».

### Ejemplos

#### Ejemplo uno

Este texto:

> Please restart your system to finalize updates

Se traduce así:

> Reinicie el sistema para terminar de instalar las actualizaciones

En este caso, evitamos traducir _please_ para evitar el exceso de cortesía y simplemente se usa la forma imperativa en la oración.

#### Ejemplo dos

Este texto a continuación:

> An error occurred while processing the card. Please try again later. We apologize for any inconvenience caused.

Se traduce de esta manera:

> Se ha producido un error al procesar la tarjeta. Inténtelo de nuevo más tarde. Sentimos cualquier inconveniente causado.

Nótese que la última parte sí se traduce, porque en este contexto (un error de procesamiento de pago de tarjeta) puede provocar un «pago fantasma» creando un inconveniente serio al usuario, pero fuera del control del sistema y del usuario. Por lo tanto en este caso, pedimos disculpas.

#### Ejemplo tres

Y finalmente este texto:
 	
>Are you sure you want to Log Out?
	
Se traduce así:

>¿Está seguro que desea cerrar la sesión?

Aquí se usa la forma cortés de «desear» y solicitamos la confirmación con «está seguro», puesto que es una pregunta para una posible acción «irreversible» por decirlo de una forma.

## En español, el uso de verbos modales y pronombres reflexivos es más común de lo que se cree

Los pronombres reflexivos (_me, te, se, nos_) y los verbos modales (_deber, poder, tener, haber que_) son mucho más usados de lo que se cree en español. Por lo general, se utilizan para:

* Referirse a eventos pasados o presentes cuando se producen errores o algún proceso falla.
    * Lo común aquí es el uso de «se pudo», «no se pudo», «se ha producido» etc.
* Traducir palabras en inglés como _may_ a su respectivo verbo modal, dependiendo del contexto.
* Al hablar de actualizaciones y notas de versión, el pronombre reflexivo «se» es común de usar para hablar de cambios y demás.

Una excepción de los verbos modales es con «haber que», «hubo», etc. Usualmente, se prefiere el uso del pronombre reflexivo «se» para este tipo de expresiones.

### Ejemplos

#### Ejemplo uno

Este texto:

> This may have been caused by sideloaded or manually compiled software, a third-party software source, or a package manager error. Manually refreshing updates may resolve the issue.

Se traduce a:

> Esto puede deberse a instalaciones externas o aplicaciones compiladas manualmente, una fuente de aplicaciones de terceros, o un error en el gestor de paquetes. Refrescar las actualizaciones podría solucionar el problema.

Nótese el uso diferente de los verbos modales en ambas acepciones de _may_. Existe una intención ligeramente diferente en cada oración.

#### Ejemplo dos

Este texto, en relación a una nota de actualización de versión

> Improve brightness in the dark style

Se traduce a:	

> Se mejoró el brillo en el estilo oscuro

### Ejemplo tres

El texto:

> There was an unexpected error while sending your message.

Se podría traducir a:

> Hubo un error inesperado mientras se enviaba su mensaje.

Pero la semantica resulta un poco extraña. El pronombre reflexivos nos ayuda a mencionar que este fue un evento que ya ocurrió, fue registrado

en cuyo caso preferimos traducilor a:

> Se ha producido un error inesperado al enviar el mensaje.

### Ejemplo cuatro

Los siguientes textos: 

> Could not save configuration
>
> Firewall rules can't be changed without the required system permission.

Se traducen a:

> No se pudo guardar la configuración	
>
> Las reglas del cortafuegos no se pueden cambiar sin los permisos necesarios.

## Tenga en cuenta las distinciones entre nombres simples y las aplicaciones con nombre propio

A la hora de traducir, es importante  poder distinguir entre los nombres propios de las aplicaciones versus el uso común de las palabras que representan. 

En particular, una aplicación, servicio o _plug_, al ser un nombre propio, debe ir siempre en su formato correcto, especificado en el glosario de términos y, si es posible, evitar referirse a la aplicación antecedida de un artículo (por ejemplo, es «Correo», no «el Correo»).

Puede consultar un glosario de términos de todos los nombres propios de las aplicaciones básicas de elementary OS en el [glosario de términos](glossary.md).

## Evite hacer traducciones absolutamente literales

Las traducciones literales nunca son recomendadas. Es muy común querer traducir palabra por palabra la forma verbal del inglés para simular el flujo del idioma original. El español tiene una estructura diferente y utiliza modismos y estructuras verbales de manera distinta que el inglés.

La sugerencia de esta guía es siempre leer la frase completa primero y entender el contexto detrás de ella para luego traducir. Trate de ver el todo de la frase y no sus palabras individuales para enviar el mismo mensaje, así no resulte necesariamente en una traducción literal.

Es recomendable evitar _transliterar_ o _traducir palabra a palabra_, es decir, leer la primera palabra, traducirla, ir a la siguiente, traducirla, etcétera. Esto suele crear frases extrañas con una composición que no se siente natural al idioma español.

### Ejemplo

Consideremos esta frase:

> This site uses cookies for incremental improvements. You may find the services function without them but at a reduced usability.

La traducción literal tanto en palabras como gramatical resultaria en:

> Este sitio usa _cookies_ para mejoras incrementales. Usted puede encontrar que los servicios funcionen sin ellas pero a una reducida usabilidad.

Pero esto no se siente natural, tanto en vocablos como en gramática. Una traducción centrada más en la comprensión general de la frase sería algo como lo siguiente:

> Este sitio utiliza _cookies_ para realizar mejoras continuas. Puede utilizar los servicios sin ellas pero con una usabilidad reducida.

## Evite traducciones automáticas con traductores

Es bastante común caer en la tentación de utilizar servicios de traducción como [el traductor de Google](https://translate.google.com) para obtener una traducción rápida. 

_No se recomienda el uso de estos servicios y, de hecho, se prefiere evitarlos completamente._

Existen múltiples razones para ello:

* Estos servicios gratuitos muchas veces son _exclusivamente para uso personal_ y los términos legales de estos servicios suelen ser complicados de usar para una organización como elementary, Inc., exigiendo el pago de licencias comerciales para un proyecto como elementary OS.

* Muchas veces estos traductores hacen _traducciones literales_. Esto significa que deciden traducir términos de manera literal, sin conocer el contexto del texto o su nivel técnico. <br>
Por ejemplo, muchas veces se traducen palabras de nombres en inglés sin posibles traducciones propias al término técnico como _cookies_ (en el contexto web, que traducen a «galletas») o _plugs_ (en el contexto de los complementos de elementary, que traducen a «enchufe»), que no tendrían cabida o sentido en la traducción final.

* A veces los traductores ofrecen traducciones de palabras que no tienen un perfecto significado a lo que se refiere. Por ejemplo, _sideload_ puede llegar a traducirse como «transferencia local» o «carga lateral» que, aunque técnicamente correctos, en el contexto de elementary no serían los términos precisos y puede llegar a confundir (en elementary estamos usando «instalación externa» para esta palabra).

* Los traductores tienden a _transliterar_ las frases. Esto resulta muchas veces en una traducción que, como se ha expuesto anteriormente, causa un español extraño y con poco sentido.

Por todas estas razones se concluye que no se pueden usar estos servicios de manera satisfactoria y desafortunadamente no podemos recomendar su uso.


# Tabla con errores simples al traducir

A continuación se expone una tabla con posibles errores comunes que se suelen escribir a la hora de hacer traducciones al idioma español, con su corrección y notas del razonamiento.

| Frase original | Correcto | Incorrecto | Notas o justificación |
| --- | --- | --- | --- |
| Click with the secondary mouse button | Haga clic con el botón secundario del ratón | _Haga clic con el botón derecho del ratón._ | Existen usuarios que usan el ratón con la mano izquierda, así que el botón derecho se refiere al botón secundario (la excepción es cuando explícitamente se refiera al botón físico del ratón). Las acciones de un botón son primario, secundario y central. |
| Whoops! That link has expired! | ¡Vaya! ¡Este enlace ha caducado! | _Vaya! Este enlace ha caducado!_ | Las frases de interrogación y exclamación siempre llevan signos tanto al comienzo como al final de la frase expresada. |
| We Have Shipped Your Order | Hemos enviado su pedido | _Hemos Enviado Su Pedido_ | Las mayúsculas compuestas no se permiten en español (esto es, una mayúscula al inicio en cada palabra). Sin embargo, se debe tener cuidado de no descapitalizar un nombre propio. Las siglas tampoco de descaptilizan |
| Spring, Fall, March, November, Tuesday, Friday | Primavera, otoño, marzo, noviembre, martes, viernes | _Primavera, Otoño, Marzo, Noviembre, Martes, Viernes_ | Los días, meses y las estaciones no utilizan mayúsculas en español, a menos que comiencen una frase |
| "elementary OS is different… a beautiful and powerful operating system." | «elementary OS es diferente… un sistema operativo hermoso y potente». | _«elementary OS es diferente… un sistema operativo hermoso y potente.»_ | Los puntos siempre van por fuera de las comillas y los paréntesis en español. |
| System Settings offers several advantages to OEMs shipping elementary OS. | La Configuración del Sistema posee varía ventajas para fabricantes OEM que ofrezcan elementary OS. | _La Configuración del Sistema posee varía ventajas a las OEMs que ofrezcan elementary OS._ | Las siglas no tienen plural en español, si ver siglas plurales, se debe buscar una alternativa o, como mínimo, utilizar los  determinantes plurales (los, las). |
