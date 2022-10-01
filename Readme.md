Parcial 01 - MCGA

Consigna:

Crear un servidor web usando Node.js, NPM y Express.js respetando la arquitectura API REST.
Debe contar con una serie de endpoints que contemple las acciones básicas de un CRUD de productos.
Los datos de los productos afectados deben estar persistidos en un base de datos NoSQL, usando Mongoose como ODM y Mongo Atlas como servicio en la nube en donde alojar la base de datos.

Crear un esquema de mongoose para los productos el cual tenga las siguientes propiedades:

* id
* name
* price
* stock
* description

Cada una debe contar con al menos la validación de tipo de dato.

Crear 6 endpoints respetando los métodos HTTP para manejar el CRUD:

* GET: para hacer ping al servidor y que devuelva 'OK' en caso que el server y la BD estén levantadas
* GET: para conseguir la lista entera de productos
* GET: para conseguir un producto por name O id
* POST: para agregar un producto a la BD
* DELETE: para eliminar un producto
* PUT: para editar algún campo de un producto

El proyecto debe manejar variables de entorno utilizando la librería dotEnv, en donde deben ir los valores sensibles que no deben ser subidos al repositorio, como por ejemplo el string de conexión a la base de datos.

El desarrollo se debe subir a un repositorio de Github en la cuenta del alumno.
Debe contar con un Readme prolijo y detallado, dando información sobre la aplicación desarrollada, tecnologías usadas, problemática resuelta, etc.
Debe contar al menos con 5 commits, todos realizados por el dueño del repositorio (alumno).

La cuenta de MongoAtlas utilizada para la base de datos debe ser del alumno.
Es necesario tener acceso a la base de datos para visualizarla al momento de exponer el parcial.

------------------------------------------------*********--------------------------------------------------

Desarrollo del Parcial:

En primer instancia se instaló en la pc el paquete Node.js

La estructura utilizada para resolver la problemática planteada es:

MCGA_PARCIAL_1
	|__ src
		|__ controllers
			|__ products.js
		|__ models
			|__ Products.js
		|__ routers
			|__ index.js
			|__ products.js
			|__ system.js
		|__ index.js
	|__ .env
	|__ .gitignore
	|__ package-lock.json
	|__ package.json
	|__ Readme.md

Dentro de la carpeta principal “MCGA_PARCIAL_1” encontramos lo siguiente:

	src —> Esta es una carpeta contenedora. Aquí encontraremos:
		|__ Una Controladora, un Modelo, un Router, y un Index.js principal.

	.env —> Este es un archivo con información del environment de nuestro proyecto. En este caso contiene los datos de conexión a nuestra base de datos, esto es: la URL y el Puerto de conexión.

	.gitignore —> Este es un archivo con información sobre lo que queremos ignorar a la hora de sincronizar nuestro proyecto con GitHub	. En este caso, ignoramos la carpeta node_modules que contiene todas las librerías que tenemos instaladas, y también los datos de environment.

	packages-lock.json —> Este es un archivo generado automáticamente cuando se instalan paquetes o dependencias en el proyecto. Su finalidad es mantener un historial de los paquetes instalados y optimizar la forma en que se generan las dependencias del proyecto y los contenidos de la carpeta node_modules/ .

	package.json —> Este es un archivo generado automáticamente con la metadata del proyecto actual y dependencias.

	Readme.md —> Este archivo contiene las consignas del parcial y la estructura de lo desarrollado.

	Dentro de la capeta “src” tenemos las siguientes:

		|__ controllers: Esta es una carpeta que maneja toda la lógica detrás de nuestro proyecto.
		|__ models: Esta carpeta contiene la estructura de los documentos que se van a guardar en la base de datos.
		|__ routers: Esta carpeta contiene un middleware router de Express y los archivos con las rutas que se configuran en el router.

FIN.