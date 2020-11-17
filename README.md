# reglayara

La siguiente **API** tiene como objetivo la integración de las reglas de **YARA** para identificar patrones que sean IoCs de malware, archivos o textos maliciosos.

**Paso 1.**

Crear un ambiente virtual con **python3**
```sh
virtualenv env --python=python3 
```

Activar el ambiente virtual
```sh
source env/bin/activate
```

**Paso 2.**

Instalar las instancias del framwork **DJANGO**

```sh
pip3 install djangorestframework
pip3 install djangorestframework
pip3 install markdown 
pip3 install django-filter
```

**paso 3.**

Crear proyecto de **DJANGO**

```sh
django-admin startproject yaramerca
```

ingresamos a nuestro proyecto

```sh
cd yaramerca
```

**paso 4.**

Listamos lo que hay dentro de nuestro proyecto

```sh
ls
```
Se crea nuestra **app** que se llamara reto1

```sh
./manage.py startapp reto1
```

ingresamos a la carpeta **yaramerca** y se agrega el perfil que va a tener nuestra app en este caso **reto1** así que verificamos el archivo denominado **settings.py**

```sh
vim settings.py
```
En la opción **INSTALLED_APPS** se agrega la las lineas 

```sh
'reto1',                                                                
'rest_framework', 
```

