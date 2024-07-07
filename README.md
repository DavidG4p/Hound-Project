# 🚀 EN DESARROLLO 🚀 
<p align="center">
<img src="https://github.com/DavidG4p/Hound-Project/assets/169712177/907fcb07-ea56-42a6-b2c1-e18c70f6c2b5">
</p>



# THE HOUND PROJECT 🐶🔎
_**The Hound Project**_ es un proyecto orientado a la realización de una investigación aplicando Inteligencia en Fuentes Abiertas (OSINT).

El objetivo de este proyecto es proporcionar al analista un entorno en el cual se garantice el mayor anonimato y la mayor seguridad posible de cara a la realización de una investigación.

Este proyecto consta de dos máquinas virtuales las cuales han sido implementadas y adecuadas para su virtualización en el hipervisor **VirtualBox**.

*  _**Hound Gateway**_ como bien indica el nombre haría de Gateway, es una máquina virtual en la cual se ha procedido a instalar Pfsense y se ha implementado un Sistema de detección de intrusos (IDS) y un Sistema de Prevención de Intrusión (IPS) para así en caso de ser detectada una amenaza a la seguridad se pueda actuar de manera autonoma para eludir dicha amenaza.
La adecuación de esta máquina es que hace de intermediario entre el exterior y la máquina virtual _**Hound Desktop**_ haciendo así que esta nunca tenga acceso directo como tal al exterior, esto se ha realizado implementando dos tarjetas de red.
  
    * Una tarjeta de red configurada con Red Nat que tiene conectividad con el exterior.
    * Una tarjeta de red interna que únicamente tiene conectividad con la máquina Hound Desktop.

*  _**Hound Desktop**_ sería la máquina que usaría el analista para proceder a realizar su propia investigación, esta máquina virtual consta de un sistema operativo Ubuntu 22.04 LongTermSupport (LTS) y dispone de una gran colección de herramientas, aplicaciones y marcadores que facilitaran la investigación del analista.
A continuación, se proporciona una imagen de la topología de como sería el fl

<p align="center">
<img src="https://github.com/DavidG4p/Hound-Project/assets/169712177/d2f63c86-1644-4e68-a110-7123604a31c4">
</p>
