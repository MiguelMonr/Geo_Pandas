# Geo_Pandas
Trabajo final para la materia Fuentes de Datos otoño 2023

Comandos para hacer su imagen y cargar su contenedor satisfactoriamente:

1. Hacer fork a este repo para poder mandar su tarea
2. Clonar el repo en su local
3. Con su terminal, entrar en el directorio Geo_Pandas
4. Crear su imagen de Docker, comandos:
    # Esto crea la imagen con el nombre imagen_geopandas
    docker build -t imagen_geopandas ./ejecutables
    # Esto crea el contenedor
    docker run --name geopandas -p 8888:8888 imagen_geopandas
    


