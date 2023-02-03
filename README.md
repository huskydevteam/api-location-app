# api-location-app
Api contruida en laravel para proporcionar direcciones a un cliente de mapas

los comando necesarios para que funcione la API, requiere un servicio de base de datos corriendo, dicha base de datos tiene que tener los datos en el archivo .env de la raiz.

Para ejecutar los comandos es necesario tener instalado PHP version 7, se usa la version 7 ya que es la que soporta el servidor donde esta alojada la version online, ademas composer

`composer install`

o

`php composer.phar install`

Luego es necesario migrar los modelos a la base de datos, ademas de correr el seeder (en este caso se usa una factory para generar multitud de entradas)

`php artisan migrate:fresh --seed`

por ultimo para iniciar el servidor

`php artisan serve`

Estara corriendo el http://localhost:8000/
las direccion de la peticion GET http://localhost:8000/api/location esta devuelve un objeto JSON con una paginacion de 100 registros por pagina. tambien existen las diferentes rutas para el CRUD.

GET http://localhost:8000/api/location/{id}
POST http://localhost:8000/api/location
PUT http://localhost:8000/api/location
DELETE http://localhost:8000/api/location

El archivo Dockerfile esta configurado para correr en railway bajo una base de datos MySQL