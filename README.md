# Comandos Utiles

![license](https://img.shields.io/github/license/miguepollo/Comandos-Utiles?style=for-the-badge)
![Last commit](https://img.shields.io/github/last-commit/miguepollo/Comandos-Utiles?style=for-the-badge)
![activity](https://img.shields.io/github/commit-activity/m/miguepollo/Comandos-Utiles?style=for-the-badge)
![github stars](https://img.shields.io/github/stars/miguepollo/Comandos-Utiles?style=for-the-badge)

Para extraer un fichero .tar

`tar zxvf {nombre_del_fichero_a_extraer}  `

Para activar el servidor de SSH

`Sudo apt install ssh` 

Aunque SSH ya esté descargado se descargará utilidades requeridas para poder ejecutar el servidor ssh.



## Navegación y Exploración de Archivos

### Comandos básicos de navegación
- `pwd` - Muestra el directorio actual
- `ls` - Lista archivos y directorios
- `ls -la` - Lista detallada incluyendo archivos ocultos
- `cd [directorio]` - Cambia de directorio
- `cd ..` - Sube un nivel en la jerarquía
- `cd ~` - Va al directorio home del usuario
- `cd -` - Va al directorio anterior

### Exploración de contenido
- `tree` - Muestra estructura de directorios en árbol
- `find [ruta] -name "*.txt"` - Busca archivos por nombre/patrón
- `locate [archivo]` - Busca archivos en base de datos indexada
- `which [comando]` - Muestra la ubicación de un comando
- `whereis [programa]` - Localiza archivos binarios, código fuente y manual

## Manipulación de Archivos y Directorios

### Crear y eliminar
- `touch [archivo]` - Crea archivo vacío o actualiza fecha
- `mkdir [directorio]` - Crea directorio
- `mkdir -p ruta/completa/nueva` - Crea directorios padre si no existen
- `rm [archivo]` - Elimina archivo
- `rm -r [directorio]` - Elimina directorio recursivamente
- `rm -rf [directorio]` - Elimina forzadamente sin confirmación
- `rmdir [directorio]` - Elimina directorio vacío

### Copiar y mover
- `cp [origen] [destino]` - Copia archivo
- `cp -r [origen] [destino]` - Copia directorio recursivamente
- `mv [origen] [destino]` - Mueve/renombra archivo o directorio
- `rsync -av [origen] [destino]` - Sincronización avanzada de archivos

### Enlaces
- `ln [archivo] [enlace]` - Crea enlace duro
- `ln -s [archivo] [enlace]` - Crea enlace simbólico

## Visualización y Edición de Archivos

### Visualizar contenido
- `cat [archivo]` - Muestra contenido completo
- `less [archivo]` - Visualiza archivo por páginas
- `more [archivo]` - Visualiza archivo por páginas (básico)
- `head [archivo]` - Muestra primeras 10 líneas
- `head -n 20 [archivo]` - Muestra primeras 20 líneas
- `tail [archivo]` - Muestra últimas 10 líneas
- `tail -f [archivo]` - Sigue archivo en tiempo real

### Editores de texto
- `nano [archivo]` - Editor simple y fácil
- `vim [archivo]` - Editor avanzado Vi mejorado
- `emacs [archivo]` - Editor Emacs

## Búsqueda y Filtrado

### Búsqueda en archivos
- `grep "patrón" [archivo]` - Busca patrón en archivo
- `grep -r "patrón" [directorio]` - Búsqueda recursiva en directorio
- `grep -i "patrón" [archivo]` - Búsqueda sin distinguir mayúsculas
- `grep -n "patrón" [archivo]` - Muestra números de línea
- `grep -v "patrón" [archivo]` - Muestra líneas que NO contienen el patrón

### Filtrado y procesamiento
- `sort [archivo]` - Ordena líneas alfabéticamente
- `uniq [archivo]` - Elimina líneas duplicadas consecutivas
- `wc [archivo]` - Cuenta líneas, palabras y caracteres
- `wc -l [archivo]` - Cuenta solo líneas
- `cut -d',' -f1 [archivo]` - Extrae primera columna (delimitador coma)
- `awk '{print $1}' [archivo]` - Imprime primera columna

## Permisos y Propiedades

### Permisos de archivos
- `chmod 755 [archivo]` - Cambia permisos (rwx r-x r-x)
- `chmod +x [archivo]` - Añade permisos de ejecución
- `chmod -w [archivo]` - Quita permisos de escritura
- `chmod u+rw [archivo]` - Añade lectura/escritura al propietario

### Propietarios
- `chown usuario:grupo [archivo]` - Cambia propietario y grupo
- `chgrp [grupo] [archivo]` - Cambia solo el grupo
- `ls -l` - Muestra permisos y propietarios

## Procesos y Sistema

### Gestión de procesos
- `ps aux` - Lista todos los procesos
- `ps -ef` - Lista procesos con formato completo
- `top` - Monitor de procesos en tiempo real
- `htop` - Monitor mejorado de procesos (si está instalado)
- `kill [PID]` - Termina proceso por ID
- `kill -9 [PID]` - Fuerza terminación de proceso
- `killall [nombre]` - Mata todos los procesos con ese nombre
- `jobs` - Muestra trabajos en background
- `bg` - Envía trabajo al background
- `fg` - Trae trabajo al foreground
- `nohup [comando] &` - Ejecuta comando inmune a hangups

### Información del sistema
- `uname -a` - Información del sistema
- `uptime` - Tiempo de actividad del sistema
- `whoami` - Usuario actual
- `id` - ID y grupos del usuario actual
- `w` - Usuarios conectados y su actividad
- `df -h` - Espacio en disco (formato legible)
- `du -sh [directorio]` - Tamaño de directorio
- `free -h` - Memoria RAM disponible
- `lscpu` - Información del procesador
- `lsblk` - Lista dispositivos de bloque

## Redes y Conectividad

### Comandos de red
- `ping [host]` - Prueba conectividad
- `wget [URL]` - Descarga archivo desde web
- `curl [URL]` - Transfiere datos desde/hacia servidor
- `ssh usuario@servidor` - Conexión SSH remota
- `scp archivo usuario@servidor:/ruta` - Copia segura por SSH
- `netstat -tuln` - Muestra puertos abiertos
- `ss -tuln` - Versión moderna de netstat

## Compresión y Archivos

### Tar (archivado)
- `tar -czf archivo.tar.gz directorio/` - Crea archivo comprimido
- `tar -xzf archivo.tar.gz` - Extrae archivo comprimido
- `tar -tzf archivo.tar.gz` - Lista contenido sin extraer

### Otros formatos
- `zip -r archivo.zip directorio/` - Crea ZIP
- `unzip archivo.zip` - Extrae ZIP
- `gzip [archivo]` - Comprime archivo
- `gunzip [archivo.gz]` - Descomprime archivo

## Historial y Shortcuts

### Historial de comandos
- `history` - Muestra historial de comandos
- `!!` - Ejecuta último comando
- `!n` - Ejecuta comando número n del historial
- `!texto` - Ejecuta último comando que empiece con "texto"
- `Ctrl+R` - Búsqueda reversa en historial

### Atajos de teclado útiles
- `Ctrl+C` - Cancela comando actual
- `Ctrl+Z` - Suspende proceso actual
- `Ctrl+D` - EOF (fin de archivo) o logout
- `Ctrl+L` - Limpia pantalla
- `Ctrl+A` - Ir al inicio de línea
- `Ctrl+E` - Ir al final de línea
- `Ctrl+U` - Borra desde cursor hasta inicio de línea
- `Ctrl+K` - Borra desde cursor hasta final de línea

## Variables de Entorno y Configuración

### Variables de entorno
- `env` - Muestra todas las variables de entorno
- `echo $HOME` - Muestra directorio home
- `echo $PATH` - Muestra PATH del sistema
- `export VARIABLE=valor` - Define variable de entorno
- `source ~/.bashrc` - Recarga configuración de bash

### Alias
- `alias ll='ls -la'` - Crea alias temporal
- `alias` - Muestra todos los alias
- `unalias ll` - Elimina alias

## Comandos de Texto y Pipes

### Pipes y redirecciones
- `comando1 | comando2` - Pipe: salida de cmd1 → entrada de cmd2
- `comando > archivo` - Redirige salida a archivo (sobrescribe)
- `comando >> archivo` - Redirige salida a archivo (añade)
- `comando < archivo` - Redirige archivo como entrada
- `comando 2> error.log` - Redirige errores a archivo
- `comando &> todo.log` - Redirige salida y errores

### Ejemplos útiles de pipes
- `ls -la | grep "^d"` - Solo directorios
- `ps aux | grep firefox` - Procesos de firefox
- `history | grep ssh` - Comandos ssh del historial
- `cat archivo.txt | sort | uniq` - Ordena y elimina duplicados

## Gestión de Paquetes (según distribución)

### Ubuntu/Debian (apt)
- `sudo apt update` - Actualiza lista de paquetes
- `sudo apt upgrade` - Actualiza paquetes instalados
- `sudo apt install [paquete]` - Instala paquete
- `sudo apt remove [paquete]` - Elimina paquete
- `apt search [término]` - Busca paquetes

### CentOS/RHEL/Fedora (yum/dnf)
- `sudo yum update` - Actualiza sistema
- `sudo yum install [paquete]` - Instala paquete
- `sudo dnf install [paquete]` - Instala paquete (Fedora)

## Comandos Útiles Adicionales

### Monitoreo y diagnóstico
- `watch [comando]` - Ejecuta comando repetidamente
- `strace [comando]` - Rastrea llamadas del sistema
- `lsof` - Lista archivos abiertos
- `iostat` - Estadísticas de I/O
- `vmstat` - Estadísticas de memoria virtual

### Fechas y tiempo
- `date` - Fecha y hora actual
- `cal` - Calendario del mes actual
- `uptime` - Tiempo desde último reinicio

### Misceláneos
- `man [comando]` - Manual del comando
- `info [comando]` - Información detallada del comando
- `apropos [palabra]` - Busca comandos relacionados
- `clear` - Limpia la terminal
- `exit` - Sale de la terminal
- `sleep [segundos]` - Pausa por tiempo especificado
