# Cheat Sheet 📋
En este apartado se explicará de una forma agil como comenzar a usar las herramientas de consola que han sido instaladas en la máquina. A continuación veremos una lista separada por categorias de las distintas herramientas que se disponen en la distribución, 
en función de la necesidad del analista se ha procedido a realizar una separación por alcance u objetivo.

Para comenzar a usar las herramientas, simplemente el analista debe de introducir el comando que se desee usar que se muestra en el listado en una terminal y complementarlo con las opciones o atributos necesarios.  

> [!IMPORTANT]
> El comando a introducir debe de coincidir tanto en mayusculas como minúsculas debido a que Linux es case sensitive (distingue entre mayusculas y minúsculas) a diferencia de por ejemplo Windows.


> [!TIP]
> En caso de desconocer como poder trabajar con la herramienta se recomienda usar la opción '-h' o '--help' para que el propio comando muestre el manual con las distintas opciones de consulta que pueden usarse. 

## Ejemplo de uso 👾

Supongamos que estamos en el hipotético caso de que queremos aplicar OSINT a nuestra investigacion de la página web "https://aula.campusciberseguridad.com".

En este caso como objetivo la página web buscamos en este repositorio si hay algun categoría que se asemeja. Nos vamos que la categoría de "Web 🌐" es idonea para nuestra investigación y nos decantamos por la herramienta "carbon14".

Desconocemos como usar la herramienta por lo que siguiendo las recomendaciones del punto anterior, introducimos el comando "carbon14" seguido del parametro "-h". 
<p align="center">
<img src="https://github.com/user-attachments/assets/bddbe541-67a2-4d60-8044-685b49614346"
</p>

Tras analizar el comando vemos que introduciendo el comando seguido de la url que queremos investigar ya empieza a analizar.

Tras lanzar el comando vemos qwue nos información de las cabeceras HTTP y las imagenes interas y externas.

<p align="center">
<img src="https://github.com/user-attachments/assets/2a12095f-c8ff-42bf-a73a-27414913decb"
</p>

# Análisis de datos 🔎
-    dumpsterDiver
-    photon
-    Th3inspector
-    foremost

# Dominios 🛡️
-    amass
-    checkdmark
-    sublist3r
-    masscan
  
> [!IMPORTANT]
> En el caso de __amass__, debe de ejecutarse con permisos de administrador. (sudo amass ....)

# Email ✉️
-    buster
-    h8mail
-    theHarvester

# Esteganografía 🖼️
-    photon
-    stegosuite
-    steghide
  
# Herramientas de descarga ⬇️
-    metagoofil
-    spiderpig
-    httrack
-    yt-dlp

# Infraestructura 🏰
-    finalRecon
-    littlebrother
-    recon-ng
-    sn0int
-    spiderfoot
-    wikileaker

# Metadatos 🔬
-    exif
-    exiftool

# Números de Teléfono ☎️
-    phoneInfoga

# Redes Sociales 📱
-    instaloader
-    osintgram
-    twosint
-    xosint

# Web 🌐
-    carbon14

# Usuarios 👥
-    blackbird
-    sherlock
