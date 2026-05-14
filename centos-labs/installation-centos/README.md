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

## Creación de la VMware para CentOS Stream 10
Vamos a crear una nueva máquina virtual para poder instalar nuestro sistema operativo linux y llevar acabo pruebas

### 1. Selección del disco de instalación
- Tener seleccionada la opción DVD ISO, ya que no se cuenta con un disco físico de instalación
- Tener definida una ruta en la que se encuentre nuestro archivo y facilitar la instalación
- Aceptar el proceso para continuar con la ruta de instalación

### 2. Nombramiento del nuevo sistema virtual
- Nombrar el sistema operativo basado en su versión o número de versiones
- Requerimiento: No tener dos máquinas con el mismo nombre

### 3. Especificación de disco duro
- El sistema por defecto recomienda 20.00 GB,asignaremos 30.00 GB para más espacio

### 4. Especificación de memoria RAM
- El instalador recomienda 1 GB,el sistema será usado como servidor para mejores recursos 2 GB es lo ideal.

### 5. Asignación del núcleo para el sistema
- 2 núcleos sera el número para el sistema para mejores respuestas de nuestra máquina

### 6. Adaptadores de red
- Adaptador NAT para estabilidad dentro de nuestra VMware ,es lo que necesitamos para iniciar
- Para pruebas futuras de servicios de servidor bridged será nuestro nuevo adaptador

### 7. Controladores para periféricos
- Con la instalación y actulización de VMware del sistema operativo invitado los periféricos se detectan en automático

### 8. Finalizar y arrancar la VMware
- Realizar las configuraciones pasadas para tener éxito en el arranque de la máquina

## Proceso de Instalación de Centos Stream 10
- Para inicar el proceso de instalación existen dos modos el normal es:
> Install CentOS stream 10
- si seleccionamos la opción Troubleshooting el modo es el siguiente:
> Install CentOS 10 Stream in basic graphics mode
Seleccionar la primera opción ya que en la segunda necesitamos el controlador VGA, en caso de equivocación la muestra de pantalla es un bug.Para continuar regresar a la pantalla anterior y seleccionar la ópcion de instalación normal.

### 1. Selección del idioma para su instalación
- Apartado para seleccionar el idioma de instalación y comodidad
- Puede cambiarse más adelante para mejor experiencia o por requerimientos

### 2. Instalación de Teclado
- En la ruta de instalación seleccionar el teclado para agregar una distribución correspondiente
- En este caso es Latinoamericano e inglés (EE.UU.)

> [ !IMPORTANT ]
> 

