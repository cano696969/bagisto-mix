# WebbyCrown Blog Extension for Bagisto

## 1. Introduction:

# Instalar usando el instalador GUI

Para instalar Bagisto usando nuestro instalador GUI, siga estos pasos:

1.  [Descargar Bagisto (abre una nueva ventana)](https://bagisto.com/en/download/)desde nuestro sitio web.
    
2.  Extraiga el contenido del archivo zip descargado.
    
3.  Navegue hasta el directorio raíz del proyecto.
    
4.  Ejecute el siguiente comando:



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