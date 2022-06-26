## Ejercicio 10

Instrucciones para desplegar un bot de Telegram con kubernetes

- Abrir ventana de chat @BotFather:

    `@BotFather> /newbot`

- Elegir un nombre:

    `@BotFather> KubWorkshopBot`

- Elegir un nombre de usuario (para el bot):

    `@BotFather> KubWorkshop_bot`

- Tomar nota del token (token:tokenHash)

- Crear una variable de ambiente

    `$ export TELEGRAM_TOKEN=<token:tokenHash>`

- Correr la imagen de prueba en docker (por consola se mostrará el tráfico del bot)

    `$ docker run -e TELEGRAM_TOKEN nicopaez/telegrambot:0.0.7`

- Probar en el chat de Telegram

    `@KubWorkshopBot> /version`

- Correr en kubernetes

    `$ minikube start`

    `$ alias kubectl="minikube kubectl --"`

    `$ kubectl apply -f deployment.yml`

- Probar en el chat de Telegram

    `@KubWorkshopBot> /version`





