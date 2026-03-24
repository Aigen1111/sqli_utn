FROM python:3.11-slim

WORKDIR /app

# Copiar requirements e instalar dependencias
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copiar el código de la aplicación
COPY . .

# Crear el directorio de base de datos
RUN mkdir -p db

#  V-04 CORREGIDA: Usar variable de entorno para SECRET_KEY
#  V-05 CORREGIDA: debug=False por defecto (controlado por FLASK_ENV)

EXPOSE 5000

CMD ["python", "app.py"]