---
layout: default
title: Git
permalink: /git/
---

# Git y GitHub
   
   ![alt text](https://live.staticflickr.com/65535/40666021673_fb324524ec_b.jpg)
   
   ## Comandos basicos
   
   | Comando                               | Descripción                                                     |
|---------------------------------------|-----------------------------------------------------------------|
| `git init`                            | Inicializa un nuevo repositorio Git.                           |
| `git clone <URL>`                    | Clona un repositorio remoto a tu máquina local.               |
| `git status`                          | Muestra el estado actual del repositorio (archivos modificados, etc.). |
| `git add <archivo>`                  | Añade un archivo específico al área de preparación.            |
| `git add .`                           | Añade todos los archivos modificados al área de preparación.   |
| `git commit -m "<mensaje>"`          | Realiza un commit con un mensaje descriptivo.                  |
| `git log`                             | Muestra el historial de commits.                               |
| `git diff`                           | Muestra las diferencias entre los archivos modificados y el último commit. |
| `git branch`                          | Muestra las ramas en el repositorio.                           |
| `git branch <nombre_rama>`           | Crea una nueva rama con el nombre especificado.                |
| `git checkout <nombre_rama>`         | Cambia a la rama especificada.                                 |
| `git merge <nombre_rama>`            | Fusiona la rama especificada en la rama actual.               |
| `git remote add origin <URL>`        | Vincula tu repositorio local a un repositorio remoto.          |
| `git push`                            | Envía tus commits al repositorio remoto.                       |
| `git pull`                            | Obtiene y fusiona cambios del repositorio remoto a tu rama actual. |
| `git fetch`                           | Obtiene cambios del repositorio remoto sin fusionar.           |
| `git reset <archivo>`                | Elimina un archivo del área de preparación, pero no de los cambios locales. |
| `git stash`                           | Guarda temporalmente cambios no confirmados.                   |
| `git stash pop`                       | Recupera los cambios guardados por el último `git stash`.      |
| `git revert <commit>`                 | Crea un nuevo commit que deshace los cambios de un commit anterior. |

   
   Utilizaremos git para realizar el control de versiones de los proyectos que realicemos en la asignatura. Deberás ir realizando los proyectos de forma incremental, y registrar los cambios (commits) realizados.
   
   ## Empezemos
   Primero instalaremos el git.
   
   `sudo apt install git`
   
   Configurar git.
   ```
   git config --global user.name "John Doe"
   git config --global user.email johndoe@example.com`
   ```
   Iremos a nuestro directorio y lo inicializamos.
   `git init`
   
   ## Ventajas de Utilizar Git

1. **Control de Versiones**
   - Permite rastrear los cambios en el código a lo largo del tiempo, facilitando la gestión de versiones.

2. **Colaboración**
   - Facilita el trabajo en equipo al permitir que múltiples desarrolladores trabajen en el mismo proyecto simultáneamente.

3. **Ramas y Fusiones**
   - Soporta la creación de ramas para trabajar en características o correcciones de manera aislada, que luego pueden fusionarse con la rama principal.

4. **Deshacer Cambios**
   - Proporciona herramientas para deshacer cambios o revertir a versiones anteriores en caso de errores.

5. **Almacenamiento Eficiente**
   - Git almacena datos de manera eficiente, lo que permite manejar proyectos grandes sin un gran consumo de espacio.

6. **Rápido y Ligero**
   - Las operaciones como commit, branch, y merge son rápidas debido a la naturaleza local de Git.

7. **Trabajo Offline**
   - Permite trabajar sin conexión a Internet; puedes realizar commits y otras operaciones localmente y sincronizarlos más tarde.

8. **Integración Continua**
   - Facilita la integración continua con herramientas de automatización para pruebas y despliegue.

9. **Historial Completo**
   - Mantiene un historial completo de cambios, lo que ayuda a comprender el desarrollo del proyecto y la toma de decisiones.

10. **Amplio Soporte**
    - Es ampliamente utilizado en la industria, lo que facilita la colaboración con otros desarrolladores y la integración con diversas herramientas.

[MAS SOBRE GIT](https://https://fp.josedomingo.org/iaw2122/u01/github.html)
