# WebbyCrown Blog Extension for Bagisto

## 1. Introduction:

# Instalar usando el instalador GUI

Para instalar Bagisto usando nuestro instalador GUI, siga estos pasos:

1.  [Descargar Bagisto (abre una nueva ventana)](https://bagisto.com/en/download/)desde nuestro sitio web.
    
2.  Extraiga el contenido del archivo zip descargado Navegue hasta el directorio raíz del proyecto.
    
4.  Ejecute el siguiente comando:


composer install



APP_URL
DB_CONNECTION
DB_HOST
DB_PORT
DB_DATABASE
DB_USERNAME
DB_PASSWORD


If you have downloaded the zip file, you will get the .env.example file. Just make a copy of that file as .env

cp .env.example .env

and also set all the .env variable as mentioned above. Once the variables have been set, generate the application key

php artisan key:generate










Instalación​
Ejecute los siguientes comandos para continuar con el proceso de instalación.

Ejecute el siguiente comando para crear una tabla de migración en la base de datos como se define en su archivo .env



php artisan migrate

Ahora la base de datos se inicializará con datos predeterminados utilizando clases de inicialización.

php artisan db:seed


php artisan vendor:publish
-> Press 0 and then press enter to publish all assets and configurations.


php artisan storage:link

This is the end of the installation process




admin@example.com


##### b. Extract the contents of zip and execute the project in your browser:

~~~
http(s)://localhost/bagisto/public
~~~

or

~~~
http(s)://example.com/public
~~~



```bash
curl -o bagisto-v2.1.2.zip https://codeload.github.com/bagisto/bagisto/legacy.zip/refs/tags/v2.1.2
```



# Descomprimir el archivo ZIP

```bash
unzip bagisto-v2.1.2.zip

cd bagisto-bagisto-9eb1882
```



```bash

composer install && php artisan migrate && php artisan db:seed && php artisan vendor:publish && php artisan key:generate

```



**How to log in as admin:**

> _http(s)://example.com/admin/login_

```
email:admin@example.com
password:admin123

```


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