## Ejercicio 1

- Ejecutar en línea de comandos:

    `docker container run -p 80:80 --volume <abs path>/ejercicio01:/usr/share/nginx/html nginx`

    `docker container run -p 80:80 --volume /home/tt/kub/ejercicio01:/usr/share/nginx/html nginx` (en mi caso)

- Navegar a `localhost` con un browser para verificar que creamos un contenedor con nginx

- Navegar a `localhost/pablo.html` para ver la página estática
