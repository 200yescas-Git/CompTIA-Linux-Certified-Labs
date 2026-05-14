# CentOS Stream 10 Installation Lab

## Objetivo
La creación de este centro de pruebas para la administración de sistemas linux es de suma importancia ya que es un sistema para servidor en el cual ya estaremos trabajando para entornos de servicios web e infraestructura.Red Hat Enterprise Linux (RHEL) es el creador de esta gran distribución pero con la diferencia de ser libre,open source,sin ningún pago de licencia;sin embargo,lo genial es que viene con la integración por default de SElinux que es muy importante para la seguridad de nuestro servidor.

## Entorno utilizado
- Máquina virtual: VMware Workstation 16 Player
- Sistema Operativo: CentOS Stream 10
- Arquitectura: ARM64 (aarch64)
- File: Centos Stream 10 DVD ISO
- Disco duro VM: 30 GB
- Memoria RAM: 2 GB
- Red: NAT
- Driver Auto Detect

## Proceso de instalación del sistema CentOS Stream 10

### 1. Creación de la máquina virtual
Vamos a crear una nueva máquina virtual para poder instalar nuestro sistema operativo linux y llevar acabo pruebas

### 2. Selección del disco de instalación
- Tener seleccionada la opción DVD ISO, ya que no se cuenta con un disco físico de instalación
- Tener definida una ruta en la que se encuentre nuestro archivo y facilitar la instalación
- Aceptar el proceso para continuar con la ruta de instalación

### 3. Nombramiento del nuevo sistema virtual
- Nombrar el sistema operativo basado en su versión o número de versiones
- Requerimiento: No tener dos máquinas con el mismo nombre

### 4. Especificación de disco duro
- El sistema por defecto recomienda 20.00 GB,asignaremos 30.00 GB para más espacio

### 5. Especificación de memoria RAM
- El instalador recomienda 1 GB,el sistema será usado como servidor para mejores recursos 2 GB es lo ideal.

### 6. Asignación del núcleo para el sistema
- 2 núcleos sera el número para el sistema para mejores respuestas de nuestra máquina

### 7. 
