# Cheat Sheet 📋
En este apartado, se explicará de una forma ágil como comenzar a usar las herramientas de consola que han sido instaladas en la máquina. A continuación se verá una lista separada por categorias de las distintas herramientas que se disponen en la distribución, en función de la necesidad del analista se ha procedido a realizar una separación por alcance u objetivo.

Para comenzar a usar las herramientas, simplemente el analista debe de introducir el comando que desee utilizar en una terminal y complementarlo con las opciones o atributos necesarios. 

> [!IMPORTANT]
> El comando a introducir debe de coincidir tanto en mayusculas como minúsculas con el que se muestra en el listado, esto es debido a que Linux es *case sensitive* (distingue entre mayusculas y minúsculas) a diferencia de por ejemplo Sistemas Operativos como Windows.


> [!TIP]
> En caso de desconocer como poder trabajar con la herramienta se recomienda usar la opción '-h' o '--help' posterior al comando que se desee utilizar, esto desplegará un manual de ayuda con las distintas opciones de consulta que pueden usarse. 

## Ejemplo de uso 👾

En este ejmplo de uso se supondrá que se desea aplicar OSINT a una investigacion de la página web "https://aula.campusciberseguridad.com".

En este caso como el objetivo es una página web se procederá a realizar una busqueda en este repositorio en el apartado de  [Herramientas 🔧](link) si hay algun categoría que se asemeja. En este caso se muestra la categoría "Web 🌐" es idonea para esta investigación, por lo qu el analista se decanta por la herramienta "*carbon14*".

En este caso, se desconoce como usar la herramienta por lo que siguiendo las recomendaciones del punto anterior, se procede a introducir el comando "*carbon14*" seguido del parametro "-h". 
<p align="center">
<img src="https://github.com/user-attachments/assets/bddbe541-67a2-4d60-8044-685b49614346"
</p>

Tras analizar el comando se comprueba que introduciendo el comando seguido de la url que sequiere investigar ya empieza a realizar un analisis.

Tras lanzar el comando se comprueba que ofrece información como las cabeceras HTTP y las imagenes interas y externas.

<p align="center">
<img src="https://github.com/user-attachments/assets/2a12095f-c8ff-42bf-a73a-27414913decb"
</p>

# Herramientas 🔧
En este apartado, se detallarán las distintas herramientas enfocadas las cuales han sido instaladas en la distribución Hound OS. No obstante, se ecnontrarán herramientas con distintos objetivos por ello, se ha procedido a separar más adelante en distintas categorías dependiendo de su función.

> [!NOTE]
> Se ha procedido a generar un hipervinculo en cada harramienta que lleva al repositorio github o manual correspondiente de cada una de las herramientas.

## Análisis de datos 🔎
-    [dumpsterDiver](https://github.com/securing/DumpsterDiver)  -> Herramienta que puede analizar grandes volúmenes de datos en busca de secretos codificados como claves o contraseñas.
-    [photon](https://github.com/s0md3v/Photon) -> Extractor de datos, puede extraer datos como: URL, Subdominios y datos relacionados con DNS, ficheros, claves secretas, etc. 
-    [Th3inspector](https://github.com/Moham3dRiahi/Th3inspector) -> Herramienta usada para recopilación de información y reconocimiento.
-    [foremost](https://github.com/korczis/foremost) -> Herramienta para recuperar archivos basándose en sus cabeceras, pies de página y estructuras de datos internas.

## Dominios 🛡️
-    [amass](https://github.com/owasp-amass/amass) -> Herramienta que realiza el mapeo de redes de superficies de ataque y el descubrimiento de activos externos.
-    [checkdmark](https://github.com/domainaware/checkdmarc) -> Herramienta para validar registros DNS SPF y DMARC.
-    [sublist3r](https://github.com/aboul3la/Sublist3r) -> Herramienta para enumerar subdominios de páginas web.
-    [masscan](https://github.com/robertdavidgraham/masscan) -> Herramienta que puede escanear rápidamente grandes rangos de direcciones IP y puertos en poco tiempo.
  
> [!IMPORTANT]
> En el caso de __amass__, debe de ejecutarse con permisos de administrador. (sudo amass ....)

## Email ✉️
-    [buster](https://github.com/sham00n/buster) -> Herramienta que recopila la información que está vinculada a una dirección de correo electrónico. 
-    [h8mail](https://github.com/khast3x/h8mail) ->  Herramienta de caza de brechas y OSINT de correo electrónico que utiliza diferentes servicios de brechas y reconocimiento, o brechas locales como "Collection1" de Troy Hunt y el infame torrent "Breach Compilation".
-    [theHarvester](https://github.com/laramies/theHarvester) -> Herramienta que recopila nombres, correos electrónicos, IPs, subdominios y URLs.

## Esteganografía 🖼️
-    [stegosuite](https://manpages.debian.org/unstable/stegosuite/stegosuite.1.en.html) -> Herramienta de esteganografía.
-    [steghide](https://manpages.ubuntu.com/manpages/trusty/man1/steghide.1.html) -> Herramienta de esteganografía que puede ocultar información en archivos de imagen.
  
## Herramientas de descarga ⬇️
-    [httrack](https://manpages.ubuntu.com/manpages/jammy/man1/httrack.1.html) -> Herramienta de descarga de sitios web. 
-    [yt-dlp](https://github.com/yt-dlp/yt-dlp) -> Herramienta de descarga de YouTube.

## Infraestructura 🏰
-    [finalRecon](https://github.com/thewhiteh4t/FinalRecon) -> Herramienta automática de reconocimiento web.
-    [recon-ng](https://github.com/lanmaster53/recon-ng) -> Framework de reconocimiento , interfaz similar a Metasploit.
-    [sn0int](https://github.com/kpcyrd/sn0int) -> Herramienta de enumeración de superficie de ataque mediante el procesamiento de información pública.
-    [spiderfoot](https://github.com/smicallef/spiderfoot) -> Servidor web integrado para proporcionar una interfaz web limpia e intuitiva, pero también se puede utilizar completamente a través de la línea de comandos. Está escrito en Python 3 y tiene licencia MIT.
-    [wikileaker](https://github.com/jocephus/WikiLeaker) -> Herramienta para buscar en WikiLeaks la existencia de un dominio o cualquier dirección de correo electrónico. 

> [!TIP]
> En caso de querer usar la versión web de **spiderfoot** se recomienda usar el siguiente comando "*spiderfoot -l 127.0.0.1:5001*" y posteriormente acceder en el navegador a la url "*127.0.0.1:5001*".

## Metadatos 🔬
-    [exif](https://manpages.ubuntu.com/manpages/trusty/man1/exif.1.html) -> Herramienta para mostrar información EXIF oculta en archivos JPEG.
-    [exiftool](https://github.com/exiftool/exiftool) -> Herramienta para leer, escribir y manipular metadatos de imágenes, audio, vídeo y PDF.
-    [metagoofil](https://github.com/opsdisk/metagoofil) -> Herramienta de extracción de metadatos de documentos públicos.
-    [spiderpig](https://github.com/hatlord/Spiderpig) -> Herramienta de recolección de metadatos de documentos

## Números de Teléfono ☎️
-    [phoneInfoga](https://github.com/sundowndev/phoneinfoga) -> Herramientas más avanzadas para escanear números de teléfono internacionales.
-    [xosint](https://github.com/TermuxHackz/X-osint) ->  Herramienta que recoge información sobre un número de teléfono, dirección de correo electrónico del usuario y la dirección IP. 


## Redes Sociales 📱
-    [instaloader](https://instaloader.github.io/) -> Herramienta para descargar imágenes (o vídeos) junto con sus pies de foto y otros metadatos de Instagram.
-    [osintgram](https://github.com/Datalux/Osintgram) -> Herramienta OSINT en Instagram para recopilar, analizar y ejecutar reconocimientos.
-    [twosint](https://github.com/falkensmz/tw1tter0s1nt) -> Herramienta OSINT para investigaciones de Twitter o actualmente X.

## Web 🌐
-    [carbon14](https://github.com/Lazza/Carbon14) -> Herramienta OSINT para estimar cuándo se escribió una página web.

## Usuarios 👥
-    [blackbird](https://github.com/p1ngul1n0/blackbird) -> Herramienta OSINT que realiza busquedas de cuentas de usuario por nombre de usuario o correo electrónico.
-    [littlebrother](https://github.com/lulz3xploit/LittleBrother) -> Herramienta de recopilación de información diseñada para realizar búsquedas sobre una persona francesa, suiza, luxemburguesa o belga.
-    [sherlock](https://github.com/sherlock-project/sherlock) ->  Herramienta de busqueda de redes sociales por nombre de usuario. 
