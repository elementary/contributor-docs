# Tabla de contenidos

* [Guía de estilo (este documento)](README.md)
* [Glosario de términos](glossary.md)
* [Prácticas recomendadas](best-practices.md)
* [Errores comunes de traducción](common-errors.md)

# Guía de estilo de elementary OS en español

Bienvenidas y bienvenidos a la wiki del equipo de traducción de elementary OS al español. Esta guía habla de detalles específicos de elementary para la localización al español. Este documento pretende unificar las traducciones de todas las variantes del español y nos ayuda a tener una traducción coherente y unificada para elementary en nuestro idioma.

# Sobre esta guía

_Esta guía no es una biblia inmutable e indiscutible._

Es un conjunto de referencias y acuerdos entre las personas que han traducido elmentary al español que nos resultan convenientes a la hora de traducir el sistema operativo y sus aplicaciones. Y debido a que el español está en continua evolución, las recomendaciones que consignemos aquí hoy pueden cambiar.

Si tiene una petición, queja, reclamo o sugerencia constructiva, es más que bienvenida. Recomendamos iniciar la discusión en:

* [El canal de Matrix de traducciones de elementary (en inglés)](https://matrix.to/#/%23elementary-l10n%3Amatrix.org) 

* [La comunidad de Discord de elementary (en inglés)](https://discord.gg/vZZCBwZ6).

# Aspectos específicos de elementary OS

A continuación discutiremos sobre aspectos específicos de la traducción de elementary OS al idioma español.

## El objetivo de _elementary OS_ como distribución

La distribución de elementary OS pretende ser una distribución concisa y simple, pero potente. 

Esto hace que las interfaces hacia el usuario deban ser simples, concisas y fáciles de entender para usuarios que no son ávidos consumidores de tecnología, o expertos en manejar sistemas. Pero, a su vez, un usuario con conocimientos puede darle un gran uso a su equipo en tareas del día a día y mucho más.

Esto, como filosofía, debe representarse en toda traducción que se haga. En la práctica, lo que se evita es ser excesivamente técnico o abstracto y tratar siempre de virar hacia lo sencillo, conciso y claro.

## Acerca de la localización regional

En este instante no se tiene como objetivo tener localizaciones regionales. Estamos asumiendo la traducción al español como un español neutro, posible de entender para toda la región hispanoamericana.

Esto significa que en Weblate, a pesar de que pueden existir otras regiones, en particular «Español (México)», o *es_MX*, no vamos a realizar traducciones en esa área, ya que no se piensan utilizar en elementary a futuro. Solamente tendremos actualizada la región principal, que en Weblate es *Español* a secas.

## Sobre el nombre _elementary_ y sus variaciones

El nombre elementary consiste de tres elementos:

* elementary: Usualmente, se refiere al equipo de desarrollo.
* elementary OS: El sistema operativo como tal.
* elementary, Inc.: La empresa y razón social detrás de elementary y elementary OS.

Este conjunto de nombres tienen las siguientes reglas:
* Nunca deben ser traducidos. Es decir, nunca debe referirse como «elemental» o traducir el acrónimo _OS_ a _SO_
* Nunca debe escribirse en mayúsculas, con la excepción del acrónimo si aparece. Al inicio de una frase debe mantenerse la minúscula. Si es posible, es recomendable modificar el texto para que _elementary_ o _elementary OS_ no sea la primera palabra de la frase.
    * Se permite reemplazar OS (en caso de que aparezca) por «sistema operativo» si esto corrige la necesidad de tener elementary como la primera palabra de una frase.
    * Si no hay manera de tener una traducción adecuada sin tener «elementary» al inicio de la frase, se permite como último recurso dejarlo tal como está.
* Si elementary aparece sin el acrónimo _OS_, no es necesario añadírselo, ya que usualmente se refiere al equipo de trabajo. Si se mencionan las palabras _operative system_ se traducirá normalmente a «sistema operativo».
* En la traducción de _elementary, Inc._ no se debe traducir la parte _Inc._, ya que no existe un equivalente hispanoamericano universal a la razón social de la empresa.

### Ejemplos

#### Ejemplo uno

> elementary OS automatically checks your Internet connection when you connect to a new Wi-Fi network.

Se traduce a:

> El sistema operativo elementary comprueba automáticamente su conexión a Internet cuando se conecta con una red wifi nueva.

#### Ejemplo dos

> The elementary brand belongs to elementary, Inc., the company that guides and supports development of elementary products.

Se traduce a:

>La marca elementary pertenece a elementary, Inc., la compañía que guía y apoya el desarrollo de los productos elementary.

#### Ejemplo tres

> Get help installing elementary OS with our step-by-step guide.

Se traduce a:

> Aprenda a instalar elementary OS con nuestra guía paso a paso.

## Nombres propios de aplicaciones

En elementary estamos traduciendo algunos nombres de aplicaciones, pero otras no. Existen diferentes razones para traducir o no traducir ciertos nombres.

En todo caso, el nombre de la aplicación debe tener siempre mayúsculas al inicio de cada palabra, excepto por artículos y conjunciones (por ej. «Centro de Aplicaciones», nótese la C y la A mayúsculas). 

Esto rompe con la convención normal del español de no hacer capitalizaciones en cada palabra, pero para nombres propios se hace una excepción.

También, al ser nombres propios, no es necesario distinguirlos de nombre extranjeros con el tipo letra itálica.

### Razones para traducir nombres propios:

* El nombre es un nombre de una aplicación de uso común, fácil de traducir (por ejemplo, _Calculator_ se traduce a «Calculadora»)
* El nombre tiene un equivalente claro en español que no distraería de su uso diario (por ejemplo, _AppCenter_ se traduce a «Centro de Aplicaciones»)

### Razones para **no** traducir nombres propios:

* No existe una traducción clara en español que podría producir más confusión. Por ejemplo, _Sideload_ no tiene una palabra clara, existe «transferencia local», pero en el contexto de elementary, no se está usando exactamente como una transferencia local, sino más bien como una aplicación externa. De hecho, cuando se refiere a _sideload_ en las traducciones, es más apropiado hablar de una «instalación externa».
* Cuando el nombre como tal no aporta nada a la interfaz del usuario o cuando es un nombre código que se usa más por los programadores y sería confuso traducirlo (por ej. _Granite_, siendo un conjunto de bibliotecas sobre GTK4 para programadores, causaría más confusión traducirlo porque nunca se refiere así internamente y no representa nada para un usuario común. Por lo tanto, lo dejamos sin cambios).

## Nombres propios de los «plugs»

Los plugs son los complementos externos que se utilizan en la aplicación de _Switchboard_ o Configuración del Sistema. En varios puntos de la traducción es común referirse a estos plugs. 

Las reglas de nombre para estos plugs son similares a las aplicaciones, con la excepción de que solamente se conserva en mayúscula la primera palabra después del prefijo «configuración», pero las demás palabras permanecen en minúscula. 

## Sobre las notas de las versiones

Las notas de las versiones usualmente se pueden encontrar en las secciones _(extra)_ de Weblate.

Estas secciones se refieren a notas de nuevas versiones respecto a correcciones, mejoras y nuevas funcionalidades.

Se recomienda, al referirse a estas secciones, al ser notas de versiones, como elementos que __han cambiado, corregido o agregado,__ por lo que se recomienda utilizar verbos en pasado con pronombres reflexivos, particularmente el uso de _se_ si resulta posible.

No es una obligación siempre usar esta forma gramatical, pero es altamente recomendado siempre que se pueda hacer.

### Ejemplo

El siguiente texto, referido a una nueva característica en la aplicación Code:

> New custom dark and light elementary styles for the source view

Se traducirá a:

> Se agregó un nuevo estilo claro y oscuro de elementary para la vista de código

## Guías de base

Es importante mencionar que una gran parte de esta información se ha tomado de los equipos de traducción al español de Ubuntu y de Fedora, así como el diccionario de términos técnicos e informáticos de Microsoft y el Diccionario panhispánico de dudas de la RAE.

Se recomienda leer y revisar frecuentemente estas guías para tener claro todos los aspectos de traducción al español para elementary OS.

* Guía de estilo de Ubuntu al español: [Ubuntu Spanish Translators](https://wiki.ubuntu.com/UbuntuSpanishTranslators)
* Guía de estilo de Fedora al español: [Fedora L10N Spanish Team](https://fedoraproject.org/wiki/L10N/Teams/Spanish/Diccionario)
* Diccionario de términos técnicos e informáticos de Microsoft: [Microsoft Terminology](https://learn.microsoft.com/en-us/globalization/reference/microsoft-terminology) y [Microsoft Terminology Search](https://msit.powerbi.com/view?r=eyJrIjoiODJmYjU4Y2YtM2M0ZC00YzYxLWE1YTktNzFjYmYxNTAxNjQ0IiwidCI6IjcyZjk4OGJmLTg2ZjEtNDFhZi05MWFiLTJkN2NkMDExZGI0NyIsImMiOjV9)
* Manual de la RAE con diversos temas [Diccionario panhispánico de dudas](https://www.rae.es/dpd/)

Si hay alguna contradicción entre estas guías y lo explicado aquí, este documento y el glosario de términos tienen precedencia sobre las guías base.


