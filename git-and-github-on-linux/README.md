# Git and GitHub On Linux

## Objectivo
Instalar Git y GitHub en sistemas operativos linux principalmente en Debian y CentOS Stream 10 donde se llevarán acabo nuestras prácticas para la certificación CompTIA Linux+.

## Introducción
Git nos permite llevar un control de versiones sobre archivos y proyectos.Facilitando el siguimiento de cambios en proyectos,recuperación de versiones anteriores y sobre todo trabajar de forma ordenada junto con colaboraciones de equipos en tecnología.

GitHub es el alojamiento y colaboración,permitiendo hacer repositorios como el actual trabajamos que hemos creado,compartiendo documentación técnica pública para replicar trabajos y proyectos.

## Uso de Git y GitHub en ambientes Linux y SysAdmin

En el área de SysAdmin, DevOps e infraestructura, Git y GitHub no solo se utilizan para desarrollo de software, sino también para:

- Documentar laboratorios y configuraciones
- Administrar scripts Bash
- Respaldar archivos de configuración
- Controlar cambios en automatizaciones
- Colaborar en equipos de infraestructura

## Diferencia entre gestión de paquetes en Debian y CentOS Stream 10

Los sistemas basados en Debian utilizan el gestor de paquetes `apt` para instalar, actualizar y administrar software.

CentOS Stream 10 utiliza el gestor de paquetes `dnf`, el cual cumple la misma función de administración de paquetes en sistemas basados en Red Hat Enterprise Linux.

Ambos gestores permiten:
- instalar paquetes
- actualizar el sistema
- eliminar software
- administrar dependencias


## Permisos administrativos para instalar software

En Linux, para instalar software es necesario contar con privilegios administrativos.

Esto se debe a que la instalación de paquetes modifica directorios y archivos importantes del sistema operativo.

Por seguridad, normalmente no se recomienda trabajar directamente como `root`. En su lugar, se utiliza el comando `sudo` para ejecutar tareas administrativas de manera temporal.

Ejemplo en Debian:

```bash
sudo apt install git -y
```

## Instalación de Git en Debian
- Arrancar máquina virtual de Debian para iniciar proceso
- Actualizar el sistema con el siguiente comando:

```bash
sudo apt update
```
## Errores y solución durante la instalación de Git en Debian
Durante la actualización de los paquetes del sistema el usuario debianlabs no contaba con permisos sudo por ende se optó ingresar con usuario root y agrgear al grupo de sudo con los siguientes comandos.

```bash
sudo -
```

```bash
groups debianlabs
```

Agregar al grupo si no contiene sudo

```bash
usermod -aG sudo debianlabs
```

Reiniciar el sistema ya que inicando de nuevo cargan correctamente los sistemas de administración

```bash
reboot
```

