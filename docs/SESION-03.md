# Fase Inicial del proyecto Web Empresarial

1. Clonar el proyecto del repositorio de la clase. [https://github.com/betodev90/DEMO-WEB](https://github.com/betodev90/DEMO-WEB)

2. En un directorio local de su máquina ejecutar el comando para clonar.

    `git clone https://github.com/betodev90/DEMO-WEB`

3. Activar el entorno virtual y de trabajo, recordar el comando.
    
    ```python
    pipenv shell
    ```

4. Crear una aplicación llamarla `core`.

    ```python
        python manage.py startapp core
    ```
5. Declarar la aplicación `core` en el archivo de configuración del proyecto `settings.py`.

6. Crear un archivo `urls.py` en el directorio de la aplicación es decir en `core/urls.py`.

7. Crear las vistas para mostrar las paginas del sitio web, en el fichero `core/views.py`.

    * Inicio - home/
    * Historia - acerca-de/
    * Servicios - servicios/
    * Visítanos - tienda/
    * Contacto - contacto/
    * Blog - blog/

8. Agregar las urls del proyecto `acerca-de`, `tienda`, `inicio` con la configuración de `core/urls.py`.

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