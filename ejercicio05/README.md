## Ejercicio 5

Todos estos comandos se utilizan en el Dockerfile

- HEALTHCHECK

    Se utiliza para verificar si un recurso está funcionando correctamente.
    
    Por ejemplo, con el comando curl se puede verificar si la aplicación
    está corriendo o no. Si
    retorna 200, el *exit code* será 0; si la aplicación se rompe, retornará 1

    `HEALTHCHECK CMD curl --fail http://localhost:3000 || exit 1`

- ONBUILD

    Agrega una instrucción disparada que será ejecutada a posteriori, cuando la imagen
    sea usada como base para otra *build*. Cualquier instrucción para la construcción de una nueva imagen
    puede ser registrada como disparada.

    Por ejemplo, si la imagen generará aplicaciones Python puede requerir que el código fuente se agregue
    en un directorio en particular

    ```
    [...]
    ONBUILD ADD . /app/src
    ONBUILD RUN /usr/local/bin/python-build --dir /app/src
    [...]
    ```

- VOLUME

    Permite que el desarrollador disponga de datos persistentes en uso dentro de los contenedores

    `VOLUME /some/dir` en el archivo Dockerfile al construir una imagen y `docker run -v /some/dir`
    al ejecutar una imagen por línea de comandos tendrán comportamientos similares.