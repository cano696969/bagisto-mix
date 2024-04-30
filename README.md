# WebbyCrown Blog Extension for Bagisto

## 1. Introduction:

# Instalar usando el instalador GUI

Para instalar Bagisto usando nuestro instalador GUI, siga estos pasos:

1.  [Descargar Bagisto (abre una nueva ventana)](https://bagisto.com/en/download/)desde nuestro sitio web.
    

4.  Ejecute el siguiente comando:





composer install




APP_URLSetting .env Variables
Once the process has been executed, open the .env file using editors and set your .env variable, especially the ones below:


~~~
http(s)://localhost/bagisto/public
~~~

or

~~~
http(s)://example.com/public
~~~


DB_CONNECTION
DB_HOST
DB_PORT
DB_DATABASE
DB_USERNAME
DB_PASSWORD


cp .env.example .env

and also set all the .env variable as mentioned above. Once the variables have been set, generate the application key

php artisan key:generate


Instalación​
Ejecute los siguientes comandos para continuar con el proceso de instalación.



php artisan migrate

Ahora la base de datos se inicializará con datos predeterminados utilizando clases de inicialización.

php artisan db:seed


php artisan vendor:publish


-> Press 0 and then press enter to publish all assets and configurations.


php artisan storage:link



### FINISH

-----------


admin@example.com


##### b. Extract the contents of zip and execute the project in your browser:




**How to log in as admin:**

> _http(s)://example.com/admin/login_

```
email:admin@example.com
password:admin123

```

## Extensiónes



## 2. Requirements:

* **PHP**: 8.0 or higher.
* **Bagisto**: v2.0.*
* **Composer**: 1.6.5 or higher.

## 3. Installation:

- Run the following command
```
composer require webbycrown/blog-for-bagisto:dev-main
```

- Run these commands below to complete the setup
```
composer dump-autoload
```

- Run these commands below to complete the setup
```
php artisan migrate
```
```
php artisan storage:link
```
```
php artisan optimize:clear
```
```
php artisan vendor:publish --all
```

- Now to use the admin side:
```
https://example.com/admin/blog
```

- Now to use the eCommerce side:
```
https://example.com/blog
```