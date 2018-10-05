# Fase Inicial del proyecto Web Empresarial

1. Clonar el proyecto del repositorio de la clase. [https://github.com/betodev90/DEMO-WEB](https://github.com/betodev90/DEMO-WEB)

2. En un directorio local de su máquina ejecutar el comando para clonar.

    `git clone https://github.com/betodev90/DEMO-WEB`

3. Activar el entorno virtual y de trabajo, recordar el comando.
    ```python
    pipenv shell
    ```
4. Verificar que este instalado django en su entorno virtual, con el comando.
    ```python
    pip list
    ```
    ó para instalar

    ```python
    pipenv install django
    ```

5. Crear un proyecto en django con el nombre de `website`. Ejecutar el siguiente comando:

    ```python
    django-admin.py startproject website .
    ```

6. Crear una aplicación llamarla `core`. Con el comando:

    ```python
        python manage.py startapp core
    ```
7. Declarar la aplicación `core` en el archivo de configuración del proyecto `settings.py`.

8. Crear un archivo `urls.py` en el directorio de la aplicación es decir en `core/urls.py`.

9. Crear las vistas para mostrar las paginas del sitio web, en el fichero `core/views.py`.

    * Inicio - home/
    * Historia - acerca-de/
    * Servicios - servicios/
    * Visítanos - tienda/
    * Contacto - contacto/
    * Blog - blog/

10. Agregar las urls del proyecto `acerca-de`, `tienda`, `inicio` con la configuración de `core/urls.py`.

    ```python
    from django.urls import path
    from . import views

    urlpatterns = [
        path('', views.home, name="home"),
        path('acerca-de/', views.about, name="about"),
        path('contacto/', views.about, name="contact"),
        path('blog/', views.about, name="blog"),
        path('tienda/', views.store, name="store"),
    ]
    ```

11. Configurar en el fichero `urls.py` principal del proyecto que se encuentra en `website/urls.py` las `urls` que se crearon en la aplicación `core`.

12. Crear un directorio para los templates en la aplicación `core`, de la siguiente manera `core/templates/core/`.

13. Fusionar el frontend con el backend, es decir revisar el directorio de ficheros estáticos `web-Frontend/` copiar los templates, y analizar las partes comunes para armar un template `core/templates/core/base.html`.
