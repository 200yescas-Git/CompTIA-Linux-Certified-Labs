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
- Idioma: Spanish
- ubicación geográfica: México
- keyboard: Latinoamericano
- Nombre de la máquina: Debian
- Nombre de dominio: sin asignar
- Configuración de usuario root: ********
- Nombre completo para el nuevo usuario no root : ********
- Configuración del usuario no root: ********
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

## Configuración Post-Instalación debian 13.4.0 (Trixie)
Se realizaron configuraciones básicas del sistema 
- Busqueda de servidores remotos para descarga y gestión de paquetes
- Para configuraciones del sistema debe ser en estado root
- Verificación de paquetes y actualizaciones

```
sudo
nano /etc/apt/sources.list
```
```
apt-get update
```
## Errores y soluciones del sistema Debian 13.4.0 (Trixie)
- Erorr en la busqueda de paquetes del servidor remoto,APT-intenta leer paquetes de CD-ROM pero ya esta montado y no lo necesitamos más
- Solución:Comentar la linea del servidor Y guardar cambios
```
#deb cdrom:[Debian GBU/Linux 13.4.0 _Trixie_ - Official amd64 DVD Binary-1 with firmware 20260314-11:54]/ trixie contrib main
```
```
CTRL+O
ENTER
CTRL+X
```

## Evidencias del Proceso de instalación de Debian 13.4.0 (Trixie)
Las capturas del proceso de encuentran en la carpeta:
```
assets/screenshots/debian-installation
```
Incluyen:
- Creación de la VM
- Proceso de instalación
- Uso de la línea de comandos
- Comandos para la consulta y actualización de paquetes
- Erorres encontrados y soluciones

## Aprendizaje obtenido del proceso
- Instalación completa de Debian 13.4.0 Trixie
- configuración básica de un sistema linux
- Uso de la terminal de linux
- Estructura de una orden dentro del sistema linux
- Detección de error en servidores remotos de actualización de paquetes
- Corrección de errores
- Usuarios y permisos

## Estado del Laboratorio
- Instalación completa
- Sistema funcional para pruebas futuras
- Arranque para administración del sistema linux y obtención de la certificación CompTIA Linux+

## Notas
Este laboratorio forma parte de mis prácticas de administración en sistemas linux y preparación para roles SysAdmin/DevOps

