# 📓 Mis Apuntes de Git & GitHub

Este repositorio es mi guía personal para el manejo de versiones. Aquí guardo los comandos esenciales aprendidos en la **PRIMERA CLASE**.

---

## 🧹 Cómo "Resetear" este Repo (Limpieza Manual)
Si clonaste un repo con archivos (HTML, CSS, JS) y quieres dejarlos fuera para que solo queden tus apuntes, sigue estos pasos:

1. **Borrar físicamente:** - En Windows (PowerShell): `Remove-Item * -Recurse -Force`
   - En Mac/Linux/Git Bash: `rm -rf *`
   *(Esto limpia tu carpeta local pero mantiene la configuración de Git).*

2. **Anotar los cambios en Git:**
   - `git add -A`: Este comando le dice a Git: "Oye, borré todo lo viejo y quizás agregué cosas nuevas, marca todo para la siguiente foto (commit)".

3. **Confirmar la limpieza:**
   - `git commit -m "Elimino archivos viejos para dejar solo mis apuntes"`: Guarda el estado "vacio" en tu historial local.

4. **Subir a la nube:**
   - `git push origin main`: Actualiza GitHub para que el repo se vea limpio.

---

## 🔄 ¿Para qué sirve `git checkout`?
Es el comando para **"viajar en el tiempo"** o moverte entre versiones y ramas.
Imaginalo como un selector de canales de televisión: tú decides qué canal (rama) quieres ver en tu carpeta.

Cambiar entre ramas existentes
Si quieres saltar de lo que estás haciendo en la rama principal a lo que hiciste en una clase específica:

* **Para volver a una versión anterior de un archivo:**
    Si arruinaste un archivo y quieres que vuelva a estar como en el último commit:
    `git checkout nombre_archivo.html`
* **Para cambiar de rama:**
    Si tienes una rama llamada "clase-2":
    `git checkout clase-2`
* **Crear y cambiar a una rama nueva (Atajo):**
    `git checkout -b nueva-rama`
* **Recuperar un archivo arruinado**
    Si borraste algo por error en tu archivo de notas y quieres que vuelva a estar como en el último guardado (commit):

    `git checkout README.md`
    (Esto "restaura" el archivo a su estado original del último commit).

---

## 🚀 Guía de Comandos Rápidos

### CONFIGURACIÓN DE GIT
* `git config --global user.name "Tu Nombre"`: Define tu nombre.
* `git config --global user.email "tuemail@gmail.com"`: Define tu email.
* `git config --list`: Muestra la configuración.

### INICIAR Y PREPARAR <----------------
* `git init`: Inicia un repo local.
* `git status`: Mira qué archivos cambiaron.
* `git add .`: Prepara **todos** los archivos para guardar.

### GUARDAR Y SUBIR
* `git commit -m "mensaje"`: Guarda cambios en el historial local.
* `git remote add origin URL`: Conecta tu PC con GitHub.
* `git push -u origin main`: Sube tus cambios por primera vez.
* `git push`: Sube cambios nuevos (cuando ya está vinculado).

### TRABAJO EN OTRA PC
* `cd ~/Desktop`: Ve al escritorio.
* `git clone URL`: Descarga tu repositorio.
* `git pull`: Trae los cambios más nuevos de GitHub a tu PC.

---

### SUBIR CAMBIOS A GIT (cuando agregaste algo a un archivo)

git status
Verifica qué archivos cambiaron.

git add .
Prepara los cambios.

git commit -m "actualizo archivo"
Guarda los cambios en Git.

git push
Sube los cambios a GitHub.

---
### ☁️ GitHub vs. 🏠 Tu PC
1. git push (Subir)
Se usa cuando tú hiciste cambios en tu computadora y quieres enviarlos a GitHub para que se guarden en internet.

Dirección: De tu PC ➔ a GitHub.

Uso: "Ya terminé mis apuntes, los voy a subir para no perderlos".

Comando: git push origin main

2. git pull (Bajar)
Se usa cuando el repositorio en GitHub tiene cambios que tú no tienes en tu computadora y quieres descargarlos para estar actualizado.

Dirección: De GitHub ➔ a tu PC.

Uso: "Ayer edité el README desde la oficina y ahora en mi casa quiero bajar esos cambios para seguir escribiendo".

Comando: git pull origin main

Comando,Acción,¿Qué hace?
git push    ,Enviar,Sube tus fotos (commits) a la nube.
git pull    ,Traer,Descarga las fotos nuevas que alguien más (o tú mismo) subió.

---
## 💻 PowerShell - Comandos de Carpeta
     IR AL ESCRITORIO
* `cd Desktop` Cambia a la carpeta Escritorio.
* `cd ~/Desktop` También cambia al Escritorio (ruta directa del usuario).
* `cd nombre_carpeta` Entra en la carpeta.
* `pwd`: ¿Dónde estoy parado?
* `ls` o `dir`: Ver qué hay en esta carpeta.
* `mkdir nombre`: Crear carpeta nueva.
* `cd ..`: Volver una carpeta hacia atrás.