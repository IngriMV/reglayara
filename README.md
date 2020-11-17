# reglayara

La siguiente **API** tiene como objetivo la integración de las reglas de **YARA** para identificar patrones que sean IoCs de malware, archivos o textos maliciosos.

**Paso 1.**

Crear un ambiente virtual con **python3**
```sh
virtualenv env --python=python3 
```

Activar el ambiente virtual
```sh
source bin/activate
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
