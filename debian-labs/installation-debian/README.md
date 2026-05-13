# Debian 13.4.0 Installation Lab (Trixie) 

## Objetivo
Realizar la instalación del sistema operativo linux Debian para realizar prácticas de administración de sistema y obtener la certificación ofcial de compTIA Linux+.

## Entorno utilizado
- Máquina Virtual: VMware Workstation 16 Player
- Sistema operativo: Debian 13.4.0 (Trixie)
- CPU: 2 cores
- RAM: 4 GB
- Disco: 30 GB
- Red: NAT

## Proceso de instalación del sistema

### 1.Create a New Virtual Machine
Al entrar al entorno gráfico de nuestra VMware Workstation seleccionamos crear una nueva máquina virtual 

### 2.Montaje de ISO
La petición es seleccionar nuestra imágen ISO oficial de Debian 13.4.0,buscando en nuestro documentos para llevar acabo la instalación

### 3.Instalación del Sistema Operativo
- Selección del tipo de sistema: Linux
- Asignación del nombre del sistema operativo: Debian
- Capacidad de disco duro: 30 GB
- Capacidad de memoria RAM: 4 GB
- Drivers: Auto detect
- Selección del adaptador de red: NAT

### 4.Instalación Virtual
- Tipo de instalación: sin entorno gráfico
- Idioma: Spanish México
- Keyboard: Latinoamericano
- Nombre de la máquina: Debian
- Nombre de dominio: sin asignar
- Clave privada: ********
- Nombre completo para el nuevo usuario: ********
- Zona Horaria:********

#### 5.Particionado de Discos
- Método de particionado: Guiado para utilizar todo el disco asignado
- Elegir disco a particionar: default asigando a la máquina virtual para el sistema operativo Debian 13.4.0 Trixie
- Esquema del particionado: Todos los ficheros en una partición (recomendado para novatos)
- Resumen del particionado de discos: Finalizar el particionado y escribir los cambios en el disco
- Confirmación: sí
- Instalar paquetes adicionales: No

### 6.-Selección de paquetes
- Tenemos que participar en la encuesta sobre el uso de los paquetes del sistema
- Tipo de entorno de escritorio: Xfce para no utilizar demasiados recursos del sistema
- SSH server: será instalado de manera práctica para hacer pruebas de laboratorio
- Instalación de arranque GRUB para unidad principal: Sí
- Dispositvo de arranaque: Partición creada /dev/sda
- Finalizamos para arrancar con el sistema operativo linux


