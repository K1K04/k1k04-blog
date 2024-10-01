---
layout: default
title: Introduccion a lxc
permalink: /lxc/
---
# Introducción de contenedores LXC

[![url-pledin](https://www.josedomingo.org/pledin/assets/wp-content/uploads/2021/12/lxc.png)](https://www.josedomingo.org/pledin/2021/12/introduccion-lxc/)

**LXC (Linux Containers)** es una tecnología de virtualización ligera que permite ejecutar múltiples sistemas Linux de manera aislada en un solo host, compartiendo el mismo kernel del sistema operativo. A diferencia de las máquinas virtuales tradicionales, **LXC no requiere un hipervisor**, lo que lo hace más eficiente en términos de recursos. Los **contenedores** proporcionan un entorno similar al de una máquina virtual, pero con menos sobrecarga, lo que los hace ideales para tareas como la creación de entornos de desarrollo, la implementación de aplicaciones, y la gestión de servicios en entornos de nube.

> LXC representa un punto de inflexión en la evolución de la virtualización, proporcionando una forma eficiente y ligera de ejecutar múltiples entornos Linux en un solo kernel, lo que lo hace adecuado para infraestructuras modernas como microservicios y DevOps.

## Instalacion LXC

| Distribución     | Método de Instalación                                     | Comando                                    |
|------------------|----------------------------------------------------------|---------------------------------------------|
| *Ubuntu*      | Instalación desde los repositorios oficiales             | `sudo apt update && sudo apt install lxc`  |
| *Debian*      | Instalación desde los repositorios oficiales             | `sudo apt update && sudo apt install lxc`  |
| *Fedora*       | Instalación desde los repositorios oficiales             | `sudo dnf install lxc`    |                  
| *CentOS/RHEL*  | Activar el repositorio EPEL y luego instalar             | `sudo yum install epel-release && sudo yum install lxc` |
| *Arch Linux*   | Instalación desde los repositorios oficiales             | `sudo pacman -S lxc`   |                     
| *OpenSUSE*    | Instalación desde los repositorios oficiales             | `sudo zypper install lxc` |                  

## Creacion de contenedores LXC

Al crear un contenedor se bajará el sistema de archivos que formará parte de él. La primera vez que bajamos con   ~~debootstrap~~ una versión de un sistema operativo se descargará un sistema de archivo mínimo del sistema (que llamamos plantilla) que servirá para crear todos los contenedores que creemos de la misma versión del sistema.

`sudo lxc-create -n contenedor1 -t debian -- -r bullseye`

- -n: Nombre del contenedor
- -t: Nombre de la plantilla.
- -r: Es una opción de la plantilla. Es el nombre de la versión del sistema operativo. Para ver más opciones de una plantilla ejecutamos: `lxc-create -t debian -h`.

Comprobar que se ha creado un contenedor;
`sudo lxc-ls -f`


## Ventajas y Desventajas de LXC

### Ventajas
- **Ligereza**: LXC utiliza menos recursos que las máquinas virtuales, ya que comparte el mismo kernel.
- **Rápido inicio**: Los contenedores LXC se inician y detienen más rápidamente que las máquinas virtuales.
- **Aislamiento**: Proporciona un alto nivel de aislamiento entre contenedores, similar al de las máquinas virtuales.
- **Facilidad de uso**: La gestión de contenedores es sencilla y se puede hacer a través de herramientas de línea de comandos.
- **Portabilidad**: Los contenedores pueden ser fácilmente movidos entre diferentes hosts que soporten LXC.
- **Escalabilidad**: Permite la creación rápida de múltiples entornos de prueba o producción.

### Desventajas
- **Compatibilidad limitada**: Solo puede ejecutar sistemas operativos compatibles con el kernel del host.
- **Configuración compleja**: La configuración inicial y la gestión de contenedores pueden ser complicadas para principiantes.
- **Menor seguridad en comparación con VM**: Aunque proporciona aislamiento, no es tan seguro como las máquinas virtuales, ya que comparten el mismo kernel.
- **Dependencia del kernel**: Los problemas en el kernel pueden afectar a todos los contenedores en ejecución.
- **Falta de soporte de algunas herramientas**: Algunas herramientas y software pueden no ser totalmente compatibles con entornos LXC.
