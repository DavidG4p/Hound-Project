# Introducción Pfsense 🇵 🇫

Como se ha reflejado en el documento [README.md](https://github.com/DavidG4p/Hound-Project/blob/main/README.md?plain=1#the-hound-project-), se dispone de dos máquinas: un escritorio y un gateway con una 
implementación de Pfsense. En este apartado, se va a realizar una breve introducción tanto al acceso a la consola de Pfsense, como a la implementación y la revisión de los logs de reporte del Sistema de 
Detección de Intrusiones (IDS).

Un Sistema de Detección de Intrusiones (IDS) es una herramienta de seguridad de red que monitoriza el tráfico y los dispositivos de la red en busca de actividades maliciosas conocidas, actividades sospechosas 
o infracciones de las políticas de seguridad y genera alertas al detectarlas. Según estas alertas, se podría investigar el problema y tomar las medidas adecuadas para corregir la amenaza.

# Acceso 🚪

Como se ha indicado en puntos anteriores, para comodidad del usuario, se recomienda el inicio de la máquina "Hound Gateway" en modo inicio sin ventana, por ello, para el acceso a la administración de Pfsense 
se accederá desde el portal web que se encontrará en la máquina "Hound Desktop".

Accediendo a la máquina "Hound Desktop", en los navegadores Firefox o Chrome, se encontrará un marcador llamado "Pfsense" (o accediendo a la dirección "https://192.5.1.1"), se mostrará una ventana
indicando que se está accediendo a un sitio potencialmente peligroso, por lo que para continuar se debe pulsar la opción de "Advanced..." y posteriormente en "Accept the Risk and Continue".

<p align="center">
<img src="https://github.com/user-attachments/assets/2eb84ae6-6cbf-4241-87e0-4bb1a7983558"
</p>

Posterior a la acción anterior, se mostrará la pantalla de login donde se solicitarán las credenciales de acceso al portal de administración de Pfsense.

<p align="center">
<img src="https://github.com/user-attachments/assets/ab18ef11-1276-459a-818d-1d65b00b40d2"
</p>
  
> [!IMPORTANT]
> Como se ha indicado anteriormente, las credenciales son las siguientes:
> - Usuario: "admin"
> - Contraseña: "Hound_Pa$$"

Tras introducir las credenciales se accederá al dashboard principal.

<p align="center">
<img src="https://github.com/user-attachments/assets/445381ed-ccd1-4867-bc0f-20e26ef721f7"
</p>

# Configuración IDS 📜

Esta implementación del IDS, se ha procedido a realizar con Suricata, el cual es un motor de detección de amenazas haciendo las funciones de IDS. Esta implementación no viene de forma nativa en Pfsense, por 
lo que ha sido necesario realizar su correspondiente implementación en el entorno.

Para acceder a la administración y configuración del servicio Suricata, se debe acceder a "Services > Suricata". 

<p align="center">
<img src="https://github.com/user-attachments/assets/f6565a23-bd19-4f80-b971-f74d63482ce2"
</p>

Se encontrará que lo primero que se muestra al usuario es el panel "Interfaces", en el se muestran todas las interfaces que se están monitorizando, en este caso, es la interfaz WAN del Pfsense. Como se puede apreciar en la 
columna de "Suricata Status", se muestra el estado actual del servicio que en este caso, se encuentra corriendo con el icono del check en verde. 

<p align="center">
<img src="https://github.com/user-attachments/assets/c05c176c-6162-4649-a37e-93709f6aa525"
</p>

> [!NOTE]
> Para evitar una experiencia de usuario dificultosa debido a los bloqueos, se ha decidido deshabilitar el modo de bloqueo automático, dado que al probar el sistema operativo, se han experimentado numerosos bloqueos
> de red al hacer uso de distintas herramientas de OSINT como búsquedas masivas o automatizadas.

En el apartado de "Global Settings" se podrá ver las distintas configuraciones que se han aplicado.

<p align="center">
<img src="https://github.com/user-attachments/assets/817c9809-2287-495e-a541-7c805c9c6d1d"
</p>

Respecto al tipo de reglas que se han implementado, se han procedido a implementar las siguientes normas;
- ETOpen Emerging Threats Rules
- Snort GPLv2 Community 
- Feodo Tracker Botnet C2 IP
- ABUSE.ch SSL Blacklist

# Revisión de logs IDS 📖
Para hacer una revisión de los logs y alertas que ha monitorizado el IDS, dentro de "Services > Suricata" se debe de acceder a "Alerts".

<p align="center">
<img src="https://github.com/user-attachments/assets/30bd5ed6-9a74-44b7-be77-f4313d967637"
</p>

Indicando la estancia que se quiere revisar la alertas (en este caso al tener solo una, se muestra la interfaz WAN por defecto), se pueden ver las distintas entradas que se han generado a lo largo de la 
conectividad de la máquina y de su correspondiente uso. Desde aquí se puede monitorizar el origen y el destino, el puerto o protocolo usado.

> [!TIP]
> En la columna de "Pri", se puede apreciar la severidad del nivel de alerta, siendo 1 el más alto y 4 el más bajo.

<p align="center">
<img src="https://github.com/user-attachments/assets/608e3785-6d7d-4942-964f-3b9bb009b9f0"
</p>
