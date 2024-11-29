API de superhéroes – Celia Isabel Bensadón
Este proyecto, desarrollado con Node.js y MongoDB, permite gestionar un catálogo de superhéroes mediante operaciones CRUD (actualmente habilitadas para GET). También es posible buscar superhéroes según atributos específicos como edad o planeta de origen.
Tabla de contenidos
1.	Descripción
2.	Tecnologías utilizadas
3.	Requisitos
4.	Instalación
5.	Uso
6.	Estructura del proyecto
7.	Rutas de la API
8.	Capturas y videos
9.	Autor
________________________________________
Descripción
La API facilita la gestión de datos relacionados con superhéroes. Las principales funcionalidades incluyen:
•	Obtén una lista completa de superhéroes.
•	Buscar superhéroes basándose en atributos específicos como edad o planeta de origen.
•	Filtrar superhéroes con más de 30 años.
________________________________________
Tecnologías utilizadas
•	Node.js
•	Express.js
•	MongoDB junto con Mongoose
________________________________________
Requisitos
Antes de comenzar, asegúrese de contar con los siguientes elementos instalados:
•	Node.js
•	Una base de datos MongoDB (local o en servicios como MongoDB Atlas).
•	Postman o cualquier otra herramienta para pruebas de API (opcional).
________________________________________
Estructura del proyecto
La estructura de carpetas del proyecto es la siguiente:
 ________________________________________
Validación en la API
Se utiliza express-validator para validar la entrada del usuario. Las reglas de validación se centralizan en el archivo superHeroValidator.mjs.
Reglas de Validación
1.	crearSuperHeroeValidation : Para validar la creación de un nuevo superhéroe.
2.	actualizarSuperHeroeValidation : Para validar la actualización de datos.
3.	eliminarSuperHeroeValidation : Para validar la eliminación de un superhéroe.
Cada regla está definida como un middleware que emplea funciones como body()y param()de query()validador expreso.
Uso en el Proyecto
1.	Rutas
•	Los middleware se aplican en las rutas de creación, actualización y eliminación.
•	Un middleware adicional ( validationHandler) gestiona los errores derivados de validaciones.
2.	Controladores
•	Las funciones como crearSuperheroeControllery actualizarSuperheroeControllerejecutan la lógica de las solicitudes, posterior a la validación.
Este enfoque modular mejora la organización y robustez del código, asegurando entradas válidas en todo momento.

