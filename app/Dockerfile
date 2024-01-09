# Define la imagen base
FROM python:3.11-alpine

# Establece el directorio de trabajo
WORKDIR /code

# Establece variables de entorno
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

# Instala dependencias necesarias
RUN apk add --no-cache gcc musl-dev linux-headers

# Copia el archivo requirements.txt y app.py al directorio de trabajo
COPY requirements.txt /code/
COPY app.py /code/

# Instala las dependencias de Python
RUN pip install -r requirements.txt

# Establece el comando de arranque
CMD ["flask", "run"]
