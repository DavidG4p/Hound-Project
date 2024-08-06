# Guía de Iniciación 📖
Esta guía esta pensada para los analistas que cuentan bajo conocimiento de informática o en entornos virtualizados, la idea es permitir con esta pequeña guía proporcionar al analista una fácil accesibilidad para su utilización.


## Descarga del entorno ⬇️
Para comenzar con esta guía, primero de todo debemos de proceder con la descarga del fichero ".zip" desde el siguiente [LINK](https://########.###).

> [!IMPORTANT]
> Para verificar la integridad y legitimidad del archivo .zip indicamos el hash SHA256 del comprimido (_**SHA256**_)  

Dado  que el comprimido tiene establecida una contraseña de encriptado, indicar que se recomienda hacer uso de un software de archivador de ficheros como "7zip".

La contraseña del comprimido es " TheHoundProject " 

## Importación del entorno ⬆️

Una vez tengamos el archivo .zip descomprimido, procederemos a importar las máquinas virtuales en nuestro software VirtualBox.

> [!NOTE]
> Este procedimiento se explicará una vez, pero indicar que hay que hacer este procedimiento dos veces, una para importar la máquina "Hound Gateway" y otra para importar la máquina "Hound Desktop".

1. Abrir la aplicación VirtualBox y en el panel superior pulsar "Archivo" > "Importar servicio virtualizado..."
<p align="center">
<img src="https://github.com/user-attachments/assets/91c36644-aef1-40cc-8529-cb646bd81015"
</p>

2. Seleccionando el icono de la carpeta se puede indicar el recurso del archivo OVA de la máquina que queremos importar, en este caso se va a proceder a importar la máquina "Hound Desktop" y pulsamos "Siguiente".
> [!WARNING]
>   Recordar nuevamente que hay que realizar la importación de ambas máquinas.
<p align="center">
<img src="https://github.com/user-attachments/assets/7dbc2916-8995-4daf-913e-ee992cc1964e"
</p>


3. Finalmente nos mostrará un resumen de la máquina que vamos a exportar donde dejaremos todo por defecto, esto es aplicable a ambas máquinas.

   En caso de querer guardar la máquina virtual en otra ubicación del equipo en este paso se puede modificar. 
<p align="center">
<img src="https://github.com/user-attachments/assets/b27324bf-8cf5-4b69-a0ad-9a191f1cfb55"
</p>

## Ejecución del entorno 💻🕵🏻‍♂️
Una vez tengamos todas las máquinas importadas, en el panel de VirtualBox nos encontraremos con las dos máquinas virtuales.

1. En primer lugar, procederemos con el encendido de la máquina "Hound Gateway".
   Dado que esta máquina no la vamos a necesitar ya que podemos acceder a ella desde la máquina "Hound Desktop", procederemos a realizar un "Inicio sin pantalla" como se muestra en la siguiente imagen haciendo click derecho sobre la máquina.
<p align="center">
<img src="https://github.com/user-attachments/assets/7cb9f181-2adc-4006-a2e0-5e06efc3612b"
</p>

2. Una vez esté encendida la máquina "Hound Gateway", procederemos con la ejecución de la máquina "Hound Desktop". En este caso el tipo de inicio de la máquina será "Inicio normal".
<p align="center">
<img src="https://github.com/user-attachments/assets/9dcfb84b-2b35-48f2-bfe3-a37726e2a110"
</p>

> [!NOTE]
> Es normal si al encender la máquina "Hound Desktop" la encontramos sin red, esto puede deberse a que todavía no ha terminado de arrancar la máquina de "Hound Gateway", una vez termine de arrancar ya tendremos red en la máquina escritorio.
