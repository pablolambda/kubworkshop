## Ejercicio 7

Respuestas:

- Se están ejecutando dos contenedores

- Basados en las imágenes `nicopaez/jobvacancy-ruby:1.3.0` y `postgres`

- Línea por línea del archivo .yml:

`version: '2'` versión del desarrollo

`services:` servicios que utiliza y/o brinda (contenedores)

... `web:`

....... `image: nicopaez/jobvacancy-ruby:1.3.0` imagen del contenedor principal

....... `links:`

........... `- db` contenedor conectado al principal

....... `ports:`

........... `- "3000:3000"` puerto en el que "escucha" la aplicación

....... `environment:` entorno específico del contenedor principal

........... `PORT: "3000"`

........... `RACK_ENV: "production"`

........... `DATABASE_URL: "postgres://postgres:Passw0rd!@db:5432/postgres"`

....... `depends_on:` establece un contenedor como obligatorio

........... `- db`

... `db:` detalles del contenedor coenctado al principal

....... `image: postgres` nombre de la imagen

....... `environment:` entorno específico del contenedor

........... `POSTGRES_PASSWORD: Passw0rd!`

- Los contenedores se "ven" entre sí por que la db está declarada en `links`
