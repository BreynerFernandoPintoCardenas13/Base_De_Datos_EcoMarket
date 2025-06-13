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

## Actividad a relizar

### Consultas mediante expresiones regulares a realizar

#### Colección Usuarios

1. Buscar usuarios cuyo correo sea de una empresa específica (por ejemplo: @empresa.com) para segmentación B2B.

2. Filtrar usuarios con nombres que incluyan un guion o doble apellido (como “Juan-Pablo” o “Martínez López”) para corrección de formularios.

3. Detectar direcciones que incluyan la palabra “rural” o “campo” para envíos con condiciones especiales.

4. Identificar usuarios cuyo teléfono tiene un formato erróneo (por ejemplo, letras mezcladas o sin prefijo).

5. Buscar usuarios con nombre que contenga abreviaturas (ej: "Sr.", "Dr.") para personalización de comunicaciones.

#### Colección Productos

6. Filtrar productos cuya descripción indique que están libres de BPA para destacar seguridad alimentaria.

7. Buscar productos con nombre que indique tamaño o formato (como “Pack”, “XL”, “Mini”) para agrupar variantes.

8. Detectar productos cuyo nombre comienza con número (ej: “3 en 1”, “100% natural”) para ordenarlos correctamente en catálogo.

9. Encontrar productos cuya descripción mencione “hecho a mano” o “artesanal” para etiquetarlos como premium.

10. Identificar productos que mencionen una oferta o promoción (“2x1”, “descuento”, “rebaja”) en su descripción.

#### Colección Pedidos

11. Buscar pedidos realizados en días festivos (identificables por fechas como 25/12, 01/01) para análisis de demanda especial.

12. Detectar pedidos que incluyan productos con identificadores de un lote retirado (ej: código que empieza con "RET").

13. Filtrar pedidos con método de pago "contra entrega" para identificar posibles riesgos o fraudes.

14. Localizar pedidos de usuarios cuya ID indica que pertenecen a una suscripción mensual (ej: terminan en “S01”).

15. Buscar pedidos con estado que indique errores en envío (“fallido”, “devuelto”, etc.) para auditoría logística.

#### Colección Marcas

16. Buscar marcas que tengan en su nombre la palabra “Eco”, “Bio” o “Verde” para crear una categoría ecológica destacada.

17. Identificar marcas cuyo sitio web no usa HTTPS (problema de seguridad).

18. Filtrar marcas de países específicos según inicial del país (ej: que empiecen con “A” para agrupar por región).

19. Detectar marcas cuyo nombre sea una sigla (por ejemplo, solo mayúsculas) para darles estilo visual distinto.

20. Buscar marcas que en su descripción mencionen colaboraciones con ONGs o certificaciones (ej: “Fair Trade”, “B Corp”).

#### Colección Reseñas

21. Buscar reseñas que usen emojis para analizarlas por tono emocional en visualizaciones.

22. Identificar reseñas que mencionen explícitamente el nombre del producto (uso directo, ayuda a SEO).

23. Filtrar reseñas donde se utilicen frases como “no volvería a comprar” o “muy decepcionado” para detección de críticas severas.

24. Detectar reseñas con comentarios que contienen preguntas (signo “?”) para responderlas desde atención al cliente.

25. Buscar reseñas que incluyan palabras como “alergia”, “reacción” o “irritación” para productos con potencial riesgo.
