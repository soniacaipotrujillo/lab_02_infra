# Laboratorio 02
en el siguiente laboratorio consiste en el despliegue de una infraestructura en la cual utilizamos Docker-compose.

1. comandos de operacion :

 - docker compose build : construye la imagen local de la API

 - docker compose up -d :inicia todos los contenedores 

 - para comprobar el funcionamiento , se realizan peticiones a los puertos (3000,3001 y 3002) utilizando el siguiente comando :

    curl -i http://localhost:3000
    curl -i http://localhost:3001
    curl -i http://localhost:3002


2. Tipo de redes en docker :

en el codigo solo se utiliza un tipo de red en docker y es bridge pero hay muchos mas y son los siguientes 

 - bridge : Docker Compose crea normalmente una red bridge para conectar los servicios del mismo proyecto, como las APIs y PostgreSQL.

 - host :Sirve para el contenedor y se usa directamente la red del equipo anfitrion.

 - none : Sirve para ejecutar un contenedor sin conexion de red .

 - overlay : se utiliza para comunica contenedores distribuidos en diferentes equipos de Docker.

 - macvlan: Sirve para asignar al contenedor su propia direccion MAC y hacerlo visible en la red fisica como otro dispositivo.

 - ipvlan : se utiliza para asignar direcciones IP a los contenedores usando la interfaz de red.

3. TIpo de Volumenes de Docker 

 - Volumen nombrado : administrado por Docker y reutilizable. en nuestro proyecto es POSTGRES_DATA usado por PostgreSQL.

 - Volumen anonimos:creado por el mismo Docker  sin un nombre explicitamente 

 - Bind mount: conecta una carpeta o archivo del equipo anfrition con un contenedor.

 - tmpfs: almacena datos temporalmente en la memoria RAM

Capturas de su proyecto desplegado en README.md

![Resultados en la terminal](mensaje_consola.png)

![API01 resultado en localhost](resultado_api01.png)

![API02 resultado en localhost](api02_localhost.png)

![API03 resultado en localhost](api03_localhost.png)
