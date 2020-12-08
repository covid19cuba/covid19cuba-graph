# Microservicio GRAPH

Micro servicio encargado de generar los gráficos que muestra el bot.

## ¿Como fuciona?

Este microservicio es utilizado por el microservicio de API REST, el microservicio de API se encarga de enviarle los datos necesarios para que genere los gráficos. Este microservicio no puede ser utilizado directamente, solo actua como un servicio auxiliar de la API.

## Variables de entorno que deben ser configuradas

`SERVER_URI`: Aquí debe ir la dirección del servidor y el puerto en el que se encuentra corriendo el microservicio, esto solo es utilizado para la marca de agua que se coloca en los gráficos.

`PORT`: Puerto donde va a correr el servicio, se puede especificar directamente al utilizar `gunicorn` en modo producción.

## Instalación y ejecución
1. Clonar este repo.
2. Instalar dependencias de python: `pip install -r requirements.txt`
4. Ejecutar servicio: `gunicorn app:app` o `python app.py`, el puerto debe ser especificado al utilizar `gunicorn` o se debe modificar el script `app.py` para que corra en modo producción y especificar el puerto.
