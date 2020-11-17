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

**Paso 3.**

Crear proyecto de **DJANGO**

```sh
django-admin startproject yaramerca
```

ingresamos a nuestro proyecto

```sh
cd yaramerca
```

**Paso 4.**

Listamos lo que hay dentro de nuestro proyecto

```sh
ls
```
Se crea nuestra **app** que se llamara reto1

```sh
./manage.py startapp reto1
```

ingresamos a la carpeta **yaramerca** y se agrega el perfil que va a tener nuestra **app** en este caso **reto1** así que verificamos el archivo denominado **settings.py**

```sh
vim settings.py
```
En la opción **INSTALLED_APPS** se agregan las siguientes lineas, las cuales son los perfiles de nuestra app y el framwork de **DJANGO**

```sh
'reto1',                                                                
'rest_framework', 
```
![2020-11-16_21-06](https://user-images.githubusercontent.com/42874558/99337464-4da3b080-2850-11eb-826e-c21ae7decbb9.png)


**Paso 5.**

Ingresamos a la carpeta de nuestra app que se denomina **reto1** y editamos el archivo denominado **models.py** el cual tendra los campos de nuestra BD

```sh
 class reglayara(models.Model):                                              
    nombre=models.CharField(max_length=200)                                 
    regla=models.TextField(max_length=5000)  
```
Guardamos cambios.

**Paso 6.**

Realizamos la migración del **modelo** 

```sh
 ./manage.py makemigrations 
 ./manage.py makemigrate
 ./manage.py migrate
```

**Paso 7.**

Nos devolvemos  ala carpeta **yaramerca** editamos el archivo denominado **admin.py** donde agregamos nuestro proyecto


```sh
from .models import reglayara                                             
                                               
class reglayaraadmin(admin.ModelAdmin):                                     
  pass                                                                    
admin.site.register(reglayara,reglayaraadmin) 
```

