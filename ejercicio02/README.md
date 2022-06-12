## Ejercicio 1

- Ejecutar en línea de comandos:

    `docker login -u <dockerid> -p <password>`

    `docker login -u pablolambda -p <password>` (en mi caso)

    `docker image pull nicopaez/pingapp:3.0.0`

    `docker image tag nicopaez/pingapp:3.0.0 pablolambda/pingapp:3.0.0`

    `docker image push pablolambda/pingapp:3.0.0`

- Para descargar la imagen:

    `docker pull pablolambda/pingapp:3.0.0`


- Respuesta bonus a la pregunta de la clase ¿Cuál es la madre de todas las imágenes?

    De la documentación de docker:

    *A* **base image** *has no parent image specified in its Dockerfile. It is created using a Dockerfile with the* `FROM scratch` *directive.*

