# Usa una imagen base de Python, pero especifica una versión de Python para evitar futuras incompatibilidades.
FROM python:3.9-slim

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia el archivo de requerimientos al contenedor
COPY requirements.txt requirements.txt

# Instala las dependencias de Python (usa --no-cache-dir para evitar que pip guarde archivos temporales)
RUN pip install -r requirements.txt
               
# Copia el resto de los archivos de la aplicación al contenedor
COPY . .

# Expone el puerto en el que correrá la aplicación (4200 parece ser para una aplicación Angular; para Python, generalmente sería 5000 u 8000)
EXPOSE 4200

# Comando para ejecutar la aplicación
CMD ["python", "app.py"]
