# Guia de instalacion de SonarQube para una distibucion Linux deribada de Debian

## Introducción
SonarQube es una herramienta de código abierto para el análisis de la calidad del código. Puede escanear el código fuente en busca de posibles errores y vulnerabilidades y genera un informe que le permite identificar problemas. Escanea hasta 30 lenguajes de programación.
SonarQube tiene dos partes: una aplicación de escáner en la máquina local para escanear el código y una aplicación de servidor para mantener registros.

## Requisitos previos
- Contar con un servidor Linux basado en Debian con al menos 2 GB de RAM.
- Cree un usuario no root con privilegios sudo.

## 1. Instalar OpenJDK
Instalar la ultima version de OpenJDK.
~~~
sudo apt-get install default-jdk
~~~

## 2. Instalar PostgreSQL
Importar la clave del repositorio de PostgreSQL.
~~~
curl https://www.postgresql.org/media/keys/ACCC4CF8.asc | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/apt.postgresql.org.gpg >/dev/null
~~~
Agregar el repositorio de PostgreSQL.
~~~
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
~~~
Actualizar la lista de repositorios del sistema.
~~~
sudo apt update
~~~
Instalar PostgreSQL 14.
~~~
sudo apt install postgresql postgresql-contrib
~~~
Verificar el estado del servicio de PostgreSQL.
~~~
sudo systemctl status postgresql
~~~






~~~
curl https://www.postgresql.org/media/keys/ACCC4CF8.asc | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/apt.postgresql.org.gpg >/dev/null
~~~



___
Este es otro ejemplo de caja en Markdown.
___
