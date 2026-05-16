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

> [!IMPORTANT]
> Fecha y hora son detectados automáticamente sin configurar

### 3. Distribución del Teclado
- Agregar la distribucón de nuestro teclado preferido para trabajar con el sistema instalado
- Revisar características del teclado físco para elegir la distribución adecuada

### 4. Selección del software de instalación
- Seleccionar instalación mínima para obtener un sistema más puro y mejorar rendimiento
- Optar por las herramientas de seguridad son algo vital para un servidor

### 5. Destino de instalación de CentOS Stream 10
- Configuración de almacenamiento personalizado
- Creación de un nuevo particionado de forma manual
- Capacidad deseada: 500 MB
- Punto de montaje: /boot
- Tipo de dispositivo: Partición estándar
- Sistema de archivos: ext4
- Nuevo punto de montaje: /
Las características de configuración son similares a /boot,con la diferencia de no asignar capacidad ya que el sistema automáticamente le proporciona lo restante.Dar click en hecho para aceptar cambios y finalizar el destino de instalación del sistema

> [!NOTE]
> La configuración personalizada es una práctica usada en Enterprise para administración avanzada en sistemas linux,por ello la separación /boot del sistema operativo nos da un entorno diferente para administrar correctamente nuestro servidor.Algunos puntos importantes de esta configuración son:
> * Estabilidad y seguridad
> * compatibilidad con GRUB/BIOS/UEFI
> * Facilidad en administración avanzada
> * Entorno Enterprise como Red Hat Enterprise Linux (RHEL)
Cifrar /boot obtendremos problemas con el arranque del sistema o simplemente no lo ejecutará,así que es recomendable no hacerlo en el punto de montaje

### 6. Configuración de red
- Ir al apartado de red para encender el switch

> [!NOTE]
> Se encontró un error de configuración de red dentro de VMware Workstattion,la nueva configuración del adaptador ethernet fue activar la opción `connect at power on`

### 7. Creación de usuario
- Dentro del apartado asignar nombre completo y usuario
- Crear una contraseña y confirmar

> [!NOTE]
> Las contraseñas siempre deben ser súper fuertes y no débiles que se encuentren en diccionarios de fuerza bruta.Se ejecutarán distintos laboratorios para pruebas por ello asignamos contraseñas de fácil memorización ya que no exponemos datos sensibles.
> Las buenas prácticas siempre deben ser prioridad en entornos enterprise y de uso cotidiano para evitar ataques cibernéticos

### 8. Cuenta root
- Crear cuenta root y confirmar
- No permitir el acceso SSH de root con contraseña

> [!WARNING]
> El usuario root es el principal blanco en ataques de hackers y conectarlo con SSH es entregarles las llaves de total acceso

### 9. Finalizar instalación
- Comenzar la instalación del sistema operativo una vez terminada la configuraión completa
- Esperar y reiniciar la máquina para poder iniciar con las prácticas

# Errores y soluciones de la instalación de CentOS Stream 10
El sistema operativo linux usado por el temario de la certificación es CentOS 7,los puntos de montaje fueron `/boot` y `/`.Para la instalación de CentOS Stream 10 el sistema de instalación necesita de 2 puntos de instalación nuevos
## Solución aplicada

Se realizó nuevamente la configuración manual de particiones agregando correctamente:

- `/boot`
- `/`
- `/biosboot`
- `swap`

Después de corregir la estructura de particionado, la instalación del sistema se completó correctamente

| Punto de montaje / Tipo | Tamaño | Filesystem / Tipo |
|---|---|---|
| biosboot | 1024 KiB | biosboot |
| /boot | 1024 MiB (1 GiB) | ext4 |
| swap | 2 GiB | swap |
| / | 23.15 GiB | ext4 |

## Evidencias del Proceso de instalación
Adjunto evidencias del proceso de instalación de CentOS Stream 10,se encuentra en la carpeta siguiente:
```
assets/screenshots/centos-installation

```
## Incluye
- Descarga del DVD ISO en la página oficial de CentOS
- Creación de la VMware para montar el sistema operativo
- Proceso de instalación por sección
- Errores y soluciones de la instalación

## Aprendizaje de la Práctica
- Particionado manual
- Puntos de montaje en sistemas linux
- Troubleshooting
- Estructura del sistema

## Estado del laboratorio
- El laboratorio se encuentra listo para continuar con las prácticas
- CentOS Stream 10 en su estado más crudo y puro para un mayor rendimiento


