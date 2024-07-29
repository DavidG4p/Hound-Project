# 🚀 EN DESARROLLO 🚀 
<p align="center">
<img src="https://github.com/DavidG4p/Hound-Project/assets/169712177/907fcb07-ea56-42a6-b2c1-e18c70f6c2b5">
</p>

# THE HOUND PROJECT 🐶🔎
_**The Hound Project**_ es un proyecto orientado a la realización de una investigación aplicando Inteligencia en Fuentes Abiertas (OSINT).

El objetivo de este proyecto son proporcionar al analista un entorno en el cual se garantice el mayor anonimato y la mayor seguridad posible de cara a la realización de una investigación y por otro lado proporcionar una distribución customizada con dis herramientas y aplicaciones para desempeñar las labores de investigación pertinentes por el analista.

Este proyecto consta de dos máquinas virtuales las cuales han sido implementadas y adecuadas para su virtualización en el hipervisor **VirtualBox**.

*  _**Hound Gateway**_ como bien indica el nombre haría de Gateway, es una máquina virtual la cual tiene una implementación de Pfsense con distintas configuraciones preestablecidas y se ha implementado un Sistema de Detección de Intrusos (IDS) con Suricata para así disponer de un gateway intermediario con una monitorización del tráfico para en caso de ser necesario poder hacer un análisis del tráfico.
  
    Esta máquina permite ser la "frontera" entre Internet y la máquina virtual _**Hound Desktop**_, haciendo así que la máquina _**Hound Desktop**_ nunca tenga acceso directo a Internet siendo necesario que pase el tráfico a través de la máquina  _**Hound Gateway**_.

    Para llevar a cabo este escenario ha sido necesario implementar dos tarjetas de red en la máquina Gateway:
    * Tarjeta Externa que se conecta a una Red NAT teniendo así esa salida al exterior.
    * Tarjeta Interna que se conecta a una Red Interna que solo tiene acceso la máquina _**Hound Gateway**_ y _**Hound Desktop**_.   


*  _**Hound Desktop**_ es la máquina escritorio que usará el analista para proceder a realizar su propia investigación, esta máquina virtual consta de la distribución _**Hound OS**_, una distribución basada en Ubuntu 22.04 LongTermSupport (LTS) y dispone de una gran colección de herramientas, aplicaciones y marcadores que facilitaran la investigación del analista.

A continuación, se proporciona una imagen de la topología de la distribución de ambas máquinas.

<p align="center">
<img src="https://github.com/DavidG4p/Hound-Project/assets/169712177/d2f63c86-1644-4e68-a110-7123604a31c4">
</p>

> [!Note]
> Ambas máquinas están pensadas para su virtualización en VirtualBox dado que se ha implementado el entorno en dicho software hipervisor y se ha realizado la instalación del agente  "GuestAdditions" para su optimo funcionamiento en VirtualBox.

# HOUND OS v0.1 💻
Hound OS como bien se ha indicado en el punto anterior, es una distribución personalizada de Ubuntu 22.04 LTSR, esta distribución la encontraremos implementada en la máquina _**Hound Desktop**_. Esta distribución dispone de una gran colección de herramienta, aplicaciones y marcadores enfocados a la investigación OSINT que se detallaran a continuación.

## Navegadores 🧭

Nos encontramos distintas aplicaciones de navegadores Web, se ha procedido a optar a implementar los dos navegadores más usados que sin Firefox en su versión ESR (Extended Support Release) y Google Chromium. 
Para estos navegadores se ha implementado una configuración de seguridad como, por ejemplo, la eliminación del historial o la caché en el cierre de los navegadores.  

  Por otro lado, se ha optado por la instalación de TOR Browser para en caso de ser necesaria la navegación por la Red TOR poder hacerlo con su correspondiente navegador.

* Firefox ESR
* Google Chromium
* Tor Browser

### Marcadores 🔖

Tras hacer varias investigaciones, se ha optado a hacer uso de los marcadores de la organización _**OSINT Combine**_ dado que ofrecen un completo abanico de marcadores pudiendo así ser til para cualquier investigación que se lleve a cabo. 

> [!IMPORTANT]
> Adjunto en el siguiente [LINK](https://www.osintcombine.com/free-osint-tools/osint-bookmark-stack) un acceso directo a la página de descarga de los marcadores OSINT.
>
>  Adjunto en el siguiente [LINK](https://www.osintcombine.com/free-osint-tools/darkweb-bookmark-stack) un acceso directo a la página de descarga de los marcadores OSINT de la DarkWeb usados del navegador TOR.

### Extensiones 🧩
Tomando de referencia el objetivo de realizar una investigación OSINT, se ha procedido a agregar una colección extensiones en los navegadores Firefox y Chrome. 

En el caso de Firefox 🦊 se ha implementado las siguientes extensiones:
- Firefox Multi-Account Containers:  Las cookies se separan por contenedor, lo que te permite usar la web con varias cuentas.
- uBlock Origin: Bloqueador de publicidad.
- DownThemAll!: Descargador masivo para tu navegador.
- SingleFile: Guarda una página web completa en un archivo HTML.
- Exif Viewer: Muestra los datos Exif de imágenes locales o remotas.
- Dark Reader: Modo oscuro para todos los sitios web.
- OneTab: Convierta las pestañas de tu navegador en una lista.
- FoxyProxy: Herramienta de gestión de proxy.


En el caso de Google Chrome 🇬 se ha implementado las siguientes extensiones:
- InVID WeVerify: Verificación de hechos y desacreditación en las redes sociales, especialmente a la hora de verificar vídeos e imágenes. 
- Ublock: Bloqueador de publicidad.
- downthemall: Descargador masivo para tu navegador.
- singleFile: Guarda una página web completa en un archivo HTML.
- OneTab: Convierta las pestañas de tu navegador en una lista.
- Wayback Machine: Reabre la pestaña actual en la Wayback Machine.

## Herramientas ⚙️

En este apartado se detallarán las distintas herramientas enfocadas las cuales han sido instaladas en la distribución Hound OS.
No obstante, nos encontraremos herramientas con distintos objetivos por ello, se ha procedido a separar más adelante en distintas categorías dependiendo de su función.

### Análisis de datos 🔎
- DumpsterDiver

### Dominios 🛡️
-    Amass
-    Checkdmark
-    Sublist3r

### Email ✉️
-    Buster
-    H8mail
-    TheHarvester

### Herramientas de descarga ⬇️
-    Browse Mirrored Websites
-    Metagoofil
-    Spiderpig
-    WebHTTrack Website Copier
-    Yt-dlp

### Geolocalización 📍
-    Creepy

### Web 🌐
-    Carbon14

### Esteganografía 🖼️
-    Exiftool
-    Exif
-    Photon
-    Stegosuite Terminal
-    Steghide

### Metadatos 🔬
-    Metagoofil

### Infraestructura 🏰
-    FinalRecon
-    Little Brother
-    Recon-ng
-    Sn0int
-    Spiderfoot
-    WikiLeaker

###  Números de Teléfono ☎️
-    PhoneInfoga
-    Th3Inspector

### Redes Sociales 📱
-    Instaloader
-    Osi.ig
-    OSINTGRAM
-    TWOSINT
-    X-Osint

### Usuarios 👥
-    Blackbird
-    Sherlock


###  Editor de Texto e IDE 👨‍💻
-    Notepad ++
-    Pycharm
-    Visual Studio Code

### 🪛Otras Herramientas🪛    
- Shodan-python 
- Maltego 
- Keepassxc  
- Cherrytree 
- Google Earth Pro 
- Terminator
- ProtonMail

# Descarga e iniciación del entorno 

El entorno se debe de descargar desde el siguiente [LINK](https://########.###).

La contraseña del comprimido es " TheHoundProject " 
