# Proyecto EcoMarket - Tienda Online de Productos Ecológicos

## Integrantes

- Juan Jose Prada Contreras
- Breyner Fernando Pinto

## Descripción del Sistema

EcoMarket es una aplicación web para comprar productos ecológicos, locales y sostenibles. Los usuarios pueden registrarse, buscar productos, dejar reseñas, seguir marcas y recibir recomendaciones.

## Como crear la base de datos desde MongoDB

### Mediante Mongosh

1. Crear Base de datos.

Usar el comando:

`use (nombre_base_de_datos)`

2. Crear Colecciones.

Usar el comando:

`db.createCollection(nombre_de_la_colección)`

se repite hasta crear las colecciones: Marcas, Pedidos, Productos, Reseñas y Usuarios.

3. Importar los .JSON en cada colección

Usar el siguiente comando:

`mongoimport --db <database_name> --collection <collection_name> --file <path_to_json_file> --type json --jsonArray`

*Explicacion del comando*

- mongoimport: Comando para importar datos a MongoDB desde un archivo externo.
- --db <database_name>: Nombre de la base de datos a la que quieres importar los datos.
- --collection <collection_name>: Nombre de la colección en la que se guardarán los documentos importados.
- --file <path_to_json_file>: Ruta al archivo .json que contiene los datos a importar.
- --type json: Indica que el archivo es de tipo JSON (opcional si la extensión es .json).
- --jsonArray: Le dice a mongoimport que el archivo contiene un array de documentos JSON.

### Mediante MongoDB Compass

1. Crear Base de Datos.

- Ya sea mediante conexión local o remota, utilizar el boton Create data base.

![Paso 1](/Imagenes/Paso_1.png)

- Luego de eso se nos desplegara una ventana en la cual le daremos nombre a nuestra base de datos y daremos nombre a nuestra primera colección.

![Paso 2](/Imagenes/Paso_2.png)

2. Crear Colecciones

- Una vez dentro de nuestra base de datos utilizaremos el boton Create collection.

![Paso 3](/Imagenes/Paso_3.png)

- Luego de eso se nos desplegara una ventana en la cual le daremos nombre a nuestra colección.

![Paso 4](/Imagenes/Paso_4.png)

3. Importar los .JSON en cada colección

- Dentro de las colecciones tendremos dos maneras de importar los archivos .JSON ya sea la colección estando vacia o teniendo documentos cargados.

**Colección Vacia**

- Directamente en el dashboard podras observar una advertencia que dice "This Collection has no Data" y debajo el boton Import data.

![Paso 5.1](/Imagenes/Paso_5.1.png)

**Colección con datos**

- Si la colección posee datos lo que haremos es utilizar la opción ADD DATA -- Import JSON or CSV file.

![Paso 5.2](/Imagenes/Paso_5.2.png)

- Una vez usada dichas opciones en cualquiera de los  se desplegara una ventana y lo que haremos es seleccionar el archivo .JSON que usaremos.

![Paso 6](/Imagenes/Paso_6.png)

**Hecho todo esto ya tendremos nuestra base de datos con sus respectivas colecciones y datos cargados.**

