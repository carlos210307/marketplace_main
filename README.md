**Submódulo:**


**Construye aplicaciones web**


Herrera Alaniz Carlos Enrique


Jimenez Aquino Saul Enrique


Morales Garcia Tania Guadalupe


Oriza Gastelum Alondra Guadalupe


Vazquez Martinez Claudia Michelle


5AMPG


ÍNDICE


1.  [Introducción](#Introducción)..............................................................................2


2.  [Comandos](#Comandos)...............................................................................3


3. [MVT](#MVT)........................................................................................4


4.  [Comandos_py](#Comandos_py) .....................5


5.  [Código](#Código) ................................................................7


6.  [Ejecución](#Ejecución).................................................................................9


7.  [Decoradores](#Decoradores) ..13


8.  [Conclusión](#Conclusión)...............................................................................21


##Introducción


Django es un framework de desarrollo web de alto nivel, gratuito y de
código abierto, escrito en Python. Su popularidad se basa en el concepto
de "Baterías incluídas" (Batteries included), que busca acelerar el
desarrollo de aplicaciones complejas, seguras y estables, adhiriéndose
al principio de "No Te Repitas" (DRY).


![python](media/item_images/python.png/)


La ventaja principal de Django es su capacidad de desarrollo rápido (RAD). Proporciona
soluciones preconstruidas y robustas para tareas que de otra manera consumirían mucho tiempo. Esto incluye ORM (Mapeo Objeto-Relacional) que permite a los desarrolladores interactuar con bases de datos usando codificación a base de python en vez de SQL, y un panel de administración que se genera automáticamente, facilitando la gestión de contenido sin la necesidad de programar un backend desde cero. Además, maneja de forma integrada
sistemas esenciales como la autenticación de usuarios, sesiones y cacheos.


Otra razón para elegir Django es su seguridad intrínseca. El framework
está diseñado específicamente para mitigar automáticamente amenazas web
críticas, como la inyección SQL, el Cross-Site scripting (XSS) y la
Falsificación de Solicitudes en Sitios Cruzados (CSRF), lo que lo
convierte en una opción viable para proyectos
empresariales.![imagen 2](media/item_images/imagen2.png)


> Finalmente su escalabilidad y su ecosistema son grandes atractivos. Al
> estar basado en Python, un lenguaje versátil y maduro, Django es capaz
> de soportar arquitecturas de tráfico masivo(como las que usan empresas
> como Instagram y Spotify). Además, se beneficia de la vasta colección
> de librerías de Python para tareas avanzadas (como machine learning y
> análisis de datos), ofreciendo una versatilidad sin igual y contando
> con una comunidad de desarrolladores activa y una documentación
> extensa.


##Comandos


**2. Explicación con sus propias palabras de cada comando que vimos en
clase por ejemplo \"venv\\Scripts\\activate\", pip install django,
django-admin startproject marketplace_main.**


-   **cd documents:** Te mueve a la carpeta llamada documents desde
    > donde estás. Es para cambiar de directorio.


-   **md nombre:** Crea una nueva carpeta (directorio) con el nombre
    > nombre en tu ubicación actual.


-   **cd nombre:** Te mueves *dentro* de la carpeta que acabas de crear
    > (nombre).


-   **code .**: Abre el editor de código (como Visual Studio Code) para
    > ver y editar todos los archivos de la carpeta actual.


-   **dir:** Muestra una lista de todos los archivos y subcarpetas
    > dentro del directorio actual.


-   **python -m venv venv:** Crea una carpeta llamada venv que contiene
    > un entorno de desarrollo aislado para tu proyecto.


-   **venv\\Scripts\\activate:** Ejecuta un *script* para activar ese
    > entorno virtual, aislando las librerías del proyecto.


-   **pip install django:** Descarga e instala el *framework* Django en
    > tu entorno virtual activo.


-   **pip list:** Muestra una lista de todas las librerías instaladas en
    > tu entorno virtual (para verificar que Django esté ahí).


-   **cd marketplace_main:** Te mueves al directorio principal de tu
    > proyecto Django.


-   **manage.py:** Es el archivo principal que usas para interactuar con
    > tu proyecto Django desde la línea de comandos.


-   **python manage.py runserver:** Inicia el servidor web temporal de
    > Django para que puedas ver el proyecto en tu navegador. copiar
    > liga
    > [[http://127.0.0.1:8000/]{.underline}](http://127.0.0.1:8000/) Es
    > la dirección que copias y pegas en el navegador para acceder a tu
    > sitio web local.


-   **para borrar el servidor es: control c:** Es la combinación de
    > teclas para detener el servidor que está corriendo.


-   **python manage.py createsuperuser:** Inicia el proceso para crear
    > una cuenta de administrador con acceso total al panel de Django.


-   **manage.py migrate:** Aplica los cambios a la base de datos y crea
    > todas las tablas necesarias para las funcionalidades internas de
    > Django.


-   **python manage.py startapp store:** Crea un nuevo módulo o
    > aplicación llamada store dentro de tu proyecto Django (ej. para
    > manejar productos, usuarios, etc.).


-   **pip install pillow:** Instala la librería Pillow, necesaria en
    > Django para gestionar el manejo de imágenes.


-   **python manage.py makemigrations:** Revisa los cambios que hiciste
    > en tus modelos (estructura de la base de datos) y crea los
    > archivos para actualizarla.


-   **python manage.py migrate:** Aplica esos archivos de migración
    > creados para que los cambios se reflejen realmente en la base de
    > datos.


**3 ##MVT


![diagrama](media/item_images/imagen3.png)


La arquitectura MVT (Model-View-Template) es la forma en que Django
organiza una aplicación web. El Model maneja los datos y la base de
datos, el View contiene la lógica que decide qué mostrar, y el Template
es la parte visual que ve el usuario.


Cuando un usuario hace una petición, Django busca la vista
correspondiente, esta obtiene los datos del modelo, los envía al
template y finalmente se genera una página HTML que se devuelve al
usuario.


**4. ##Comandos_py


settigs.py


El archivo settings.py es uno de los archivos más importantes dentro de
un proyecto de


Django. Su función principal es almacenar toda la configuración del
proyecto, es decir,


los parámetros que Django necesita para funcionar correctamente.


Dentro de este archivo se encuentran definidas varias configuraciones
esenciales,


como:


INSTALLED_APPS: indica las aplicaciones que están activas dentro del
proyecto y que


Django debe reconocer.


DATABASES: contiene la configuración de la base de datos (por ejemplo,
tipo de base


de datos, nombre, usuario y contraseña).


TEMPLATES: define cómo se manejarán las plantillas HTML del proyecto.


STATIC_URL y MEDIA_URL: especifican las rutas donde se guardan los
archivos


estáticos (imágenes, CSS, JavaScript) y los archivos subidos por los
usuarios.


MIDDLEWARE: lista los componentes que procesan las peticiones y
respuestas entre


el navegador y el servidor.


DEBUG y ALLOWED_HOSTS: controlan el modo de desarrollo y los dominios permitidos para ejecutar el sitio web.


urls.py


El archivo urls.py tiene la función principal de controlar las rutas o
direcciones (URLs) que utiliza un proyecto de Django para acceder a las diferentes páginas o vistas del sitio web.


Cuando un usuario escribe una dirección en el navegador, Django utiliza
este archivo para determinar qué parte del código debe ejecutarse y qué contenido mostrar.
En otras palabras, el urls.py actúa como un mapa de navegación que conecta las
direcciones web con las funciones o vistas que deben responder a esas peticiones.


Dentro del archivo se definen patrones de URL mediante una lista llamada
urlpatterns, donde se asocian rutas con vistas.


Además, urls.py permite organizar las rutas de manera modular, ya que
cada aplicación dentro del proyecto puede tener su propio archivo urls.py, y todas
pueden conectarse al archivo principal del proyecto mediante la función include().


models.py


El archivo models.py es donde se define toda la parte de los datos de
una aplicación en Django.


Ahí es donde se crean las clases que representan las tablas de la base
de datos, por ejemplo una tabla de productos, usuarios o pedidos.


Cada modelo tiene sus campos, como nombre, precio, descripción o fecha,
y Django usa esa información para crear automáticamente las tablas en la base de
datos, sin que uno tenga que escribir código SQL.


En pocas palabras, el models.py sirve para decirle a Django qué tipo de
información va a


guardar la aplicación y cómo va a estar organizada.


Es como la base o la estructura de los datos que después se usan en las
vistas y en las


páginas del proyecto.


views.py


El archivo views.py en una aplicación de Django es el que se encarga de
la parte lógica,


o sea, de decidir qué va a pasar cuando un usuario entra a una página.


Por ejemplo, si alguien visita una ruta, el views.py puede mostrar una
lista de


productos, los detalles de uno, o guardar datos de un formulario.


Básicamente, las vistas reciben la petición del usuario y devuelven una
respuesta, ya


sea un texto, una página HTML o información desde la base de datos.


Es como el punto medio entre lo que el usuario pide y lo que Django
muestra.


En pocas palabras: el views.py es el cerebro que controla qué se ve y
qué se hace


dentro de cada parte del proyecto.


templates/store


La carpeta templates/store es una convención de Django que organiza los
archivos HTML utilizados para renderizar la interfaz de usuario
específica de una aplicación llamada, en este caso, \"store\". Actúa
como el módulo de presentación (la \"P\" de MTV - Modelo, Plantilla,
Vista) donde reside todo el diseño web y la estructura visual.


**5. ##Código

**settings.py:**


"""
Django settings for marketplace_main project.


Generated by 'django-admin startproject' using Django 5.2.7.


For more information on this file, see
https://docs.djangoproject.com/en/5.2/topics/settings/


For the full list of settings and their values, see
https://docs.djangoproject.com/en/5.2/ref/settings/
"""


from pathlib import Path


# Build paths inside the project like this: BASE_DIR / 'subdir'.
BASE_DIR = Path(__file__).resolve().parent.parent

# Quick-start development settings - unsuitable for production
# See https://docs.djangoproject.com/en/5.2/howto/deployment/checklist/

# SECURITY WARNING: keep the secret key used in production secret!
SECRET_KEY = 'django-insecure-abbqs8c_^$)&q+wqo%q%wnl!be&%y19ztn1^x_znattq#nk7)@'

# SECURITY WARNING: don't run with debug turned on in production!
DEBUG = True

ALLOWED_HOSTS = []
LOGIN_URL = '/store/login/'
LOGIN_REDIRECT_URL = '/'
LOGOUT_REDIRECT_URL = '/'

# Application definition

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',

    'store',
]

MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
]

ROOT_URLCONF = 'marketplace_main.urls'

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]

WSGI_APPLICATION = 'marketplace_main.wsgi.application'

# Database
# https://docs.djangoproject.com/en/5.2/ref/settings/#databases

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}

# Password validation
# https://docs.djangoproject.com/en/5.2/ref/settings/#auth-password-validators

AUTH_PASSWORD_VALIDATORS = [
    {
        'NAME': 'django.contrib.auth.password_validation.UserAttributeSimilarityValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.MinimumLengthValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.CommonPasswordValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.NumericPasswordValidator',
    },
]

# Internationalization
# https://docs.djangoproject.com/en/5.2/topics/i18n/

LANGUAGE_CODE = 'en-us'

TIME_ZONE = 'UTC'

USE_I18N = True

USE_TZ = True

# Static files (CSS, JavaScript, Images)
# https://docs.djangoproject.com/en/5.2/howto/static-files/

STATIC_URL = 'static/'
MEDIA_URL = 'media/'
MEDIA_ROOT = BASE_DIR / 'media'

# Default primary key field type
# https://docs.djangoproject.com/en/5.2/ref/settings/#default-auto-field

DEFAULT_AUTO_FIELD = 'django.db.models.BigAutoField'

**urls.py:**


from django.urls import path
from django.contrib.auth import views as auth_views
from .views import contact, detail, register, logout_user, add_item


from .forms import LoginForm


urlpatterns = [
    path('contact/', contact, name='contact'),
    path('register/', register, name='register'),
    path('login/', auth_views.LoginView.as_view(template_name='store/login.html', authentication_form=LoginForm), name='login'),
    path('logout/', logout_user, name='logout'),
    path('add_item/', add_item, name='add_item'),
    path('detail/<int:pk>/', detail, name='detail'),
]


**models.py:**


from django.contrib.auth.models import User
from django.db import models


class Category(models.Model):
    name = models.CharField(max_length=255)


    class Meta:
        ordering = ('name', )
        verbose_name_plural = 'categories'


    def __str__(self):
        return self.name
   
class Item(models.Model):
    category = models.ForeignKey(Category, related_name='items', on_delete=models.CASCADE)
    name = models.CharField(max_length=255)
    description = models.TextField(blank=True, null=True)  
    price = models.FloatField()
    image = models.ImageField(upload_to='item_images', blank=True, null=True)
    is_sold = models.BooleanField(default=False)
    created_by = models.ForeignKey(User, related_name='items', on_delete=models.CASCADE)
    create_at = models.DateTimeField(auto_now_add=True)


    def __str__(self):
        return self.name


**views.py:**


from django.shortcuts import render, get_object_or_404, redirect
from django.contrib.auth.decorators import login_required
from django.contrib.auth import logout


from .models import Item, Category


from .forms import SignupForm, NewItemForm


# Create your views here.
def home(request):
    items = Item.objects.filter(is_sold=False)
    categories = Category.objects.all()


    context = {
        'items': items,
        'categories': categories
    }
    return render(request, 'store/home.html', context)


def contact(request):
    context = {
        'msg': 'Quieres otros productos contactame!'
    }


    return render(request, 'store/contact.html', context)


def detail(request, pk):
    item = get_object_or_404(Item, pk=pk)
    related_items = Item.objects.filter(category=item.category, is_sold=False).exclude(pk=pk)[0:3]
    context={
        'item': item,
        'related_items': related_items
    }


    return render(request, 'store/item.html', context)


def register(request):
    if request.method == 'POST':
        form = SignupForm(request.POST)


        if form.is_valid():
            form.save()
            return redirect('login')
    else:
        form = SignupForm()


    context = {
        'form': form
    }


    return render(request, 'store/signup.html', context)


def logout_user(request):
    logout(request)


    return redirect('home')


@login_required
def add_item(request):
    if request.method == 'POST':
        form = NewItemForm(request.POST, request.FILES)


        if form.is_valid():
            item = form.save(commit=False)
            item.created_by = request.user
            item.save()


            return redirect('detail', pk=item.id)
    else:
        form = NewItemForm()
        context = {
            'form': form,
            'title': 'New Item'
        }


    return render(request, 'store/form.html', context)


**templates/store/index.html:**\


<! DOCTYPE html>
‹html lang-"es">
<head>
‹meta charset="UTF-g">
‹title›Marketplace</title>
</head›
<body>
<hi>Bienvenido a Marketplace</h1>
<ul>
{% for producto in productos %} <li>({ producto.nombre }] - $({ producto.precio }}</li>
(% endfor %}
</u1>
</body>
</html>


**6. ##Ejecución


![codigo6](media/item_images/codigo6.png)


![codigo7](media/item_images/codigo7.png)


![codigo8](media/item_images/codigo8.png)![codigo9](media/item_images/codigo9.png)![codigo10](media/item_images/codigo10.png)
**7 ##Decoradores


En este archivo se definen los formularios que utiliza la aplicación  para interactuar con el usuario. Estos formularios permiten capturar información de manera estructurada y validarla antes de enviarla a la base de datos o procesarla en una vista.


**LoginForm**


Es un formulario sencillo diseñado para que un usuario pueda iniciar
sesión.\
Consta de dos campos:


username: el nombre de usuario registrado.


password: la contraseña del usuario (se muestra oculta por seguridad).


Su función principal es recibir las credenciales del usuario y enviarlas a la vista encargada del proceso de autenticación.


**SignupForm**


Formulario utilizado para registrar nuevos usuarios.\
Incluye campos como:


username, email, password1 y password2


Este formulario incorpora validaciones importantes, como:


Verificar si el nombre de usuario ya existe, Comprobar que las dos contraseñas coincidan.


Su objetivo es garantizar que el nuevo usuario cumpla los requisitos y evitar errores comunes antes de crear la cuenta en la base de datos del sistema.


**NewItemForm**


Formulario basado en un modelo (ModelForm) cuyo propósito es permitir que un usuario agregue un nuevo artículo al marketplace.\ Contiene campos tales como: Nombre del artículo ,Descripción ,Precio ,Imagen y Categoría del producto.


Automáticamente toma la estructura del modelo Item, reduciendo la cantidad de código necesario y garantizando consistencia entre la base de datos y la interfaz de usuario.


from django import forms
from django.contrib.auth.forms import UserCreationForm, AuthenticationForm
from django.contrib.auth.models import User


from .models import Item


class LoginForm(AuthenticationForm):
    username = forms.CharField(widget=forms.TextInput(
        attrs={
            'placeholder': 'Tu usuario',
            'class': 'form-control'
        }
    ))


    password = forms.CharField(widget=forms.PasswordInput(
        attrs={
            'placeholder': 'password',
            'class': 'form-control'
        }
    ))


class SignupForm(UserCreationForm):
    class Meta:
        model = User
        fields = ('username', 'email', 'password1', 'password2')


    username = forms.CharField(widget=forms.TextInput(
        attrs={
            'placeholder': 'Tu Usuario',
            'class': 'form-control'
        }
    ))


    email = forms.CharField(widget=forms.EmailInput(
        attrs={
            'placeholder': 'Tu Email',
            'class': 'form-control'
        }
    ))






**Views.py (login(), logout_user(), detail(), add_item())**


Las vistas controlan la lógica que ocurre cuando un usuario accede a una ruta específica. Cada vista procesa datos, interactúa con la base de datos y devuelve una plantilla HTML renderizada.


**login() o login_user()**


Esta vista recibe los datos del formulario de inicio de sesión.\
Sus funciones principales son:


Recibir las credenciales enviadas por un formulario, Autenticar al usuario utilizando el sistema interno de Django, Iniciar la sesión si los datos son correctos, Redirigir al usuario a la página principal del marketplace.\
Si las credenciales son incorrectas, simplemente vuelve a mostrar el formulario.


**logout_user()**


Esta vista cierra la sesión del usuario.\
Acciones que realiza: Termina la sesión actual, Limpia los datos de sesión almacenados,Redirige al usuario a la página de inicio de sesión.


Se utiliza normalmente desde un botón en la barra de navegación.


**detail()**


Vista encargada de mostrar un artículo específico.\
Sus funciones: Recibir el identificador (ID) del artículo, Buscar el artículo en la base de datos, Si existe, enviarlo a una plantilla para mostrar sus datos.\
Si no existe, mostrar una página de error.


Es la vista que muestra:


Imagen del artículo, Descripción, Precio, Usuario que lo publicó


**add_item()**


Permite a los usuarios agregar un artículo nuevo al marketplace.


Funciones principales: Mostrar un formulario vacío si es la primera vez que se accede, Recibir los datos enviados por el usuario, Validar que toda la información sea correcta, Guardar el artículo en la base de datos, Asociar el artículo al usuario que lo creó,Redirigir al listado de artículos.


Esta vista está protegida con \@login_required para evitar que personas
no autenticadas publiquen productos.


from django.shortcuts import render, get_object_or_404, redirect
from django.contrib.auth.decorators import login_required
from django.contrib.auth import logout


from .models import Item, Category


from .forms import SignupForm, NewItemForm


# Create your views here.
def home(request):
    items = Item.objects.filter(is_sold=False)
    categories = Category.objects.all()


    context = {
        'items': items,
        'categories': categories
    }
    return render(request, 'store/home.html', context)


def contact(request):
    context = {
        'msg': 'Quieres otros productos contactame!'
    }


    return render(request, 'store/contact.html', context)


def detail(request, pk):
    item = get_object_or_404(Item, pk=pk)
    related_items = Item.objects.filter(category=item.category, is_sold=False).exclude(pk=pk)[0:3]
    context={
        'item': item,
        'related_items': related_items
    }


    return render(request, 'store/item.html', context)


def register(request):
    if request.method == 'POST':
        form = SignupForm(request.POST)


        if form.is_valid():
            form.save()
            return redirect('login')
    else:
        form = SignupForm()


    context = {
        'form': form
    }


    return render(request, 'store/signup.html', context)


def logout_user(request):
    logout(request)


    return redirect('home')


@login_required
def add_item(request):
    if request.method == 'POST':
        form = NewItemForm(request.POST, request.FILES)


        if form.is_valid():
            item = form.save(commit=False)
            item.created_by = request.user
            item.save()


            return redirect('detail', pk=item.id)
    else:
        form = NewItemForm()
        context = {
            'form': form,
            'title': 'New Item'
        }


    return render(request, 'store/form.html', context)






**Explicar decorador \@login_required**


Es un decorador que se coloca encima de una vista para indicar que esa función solo puede ser utilizada por usuarios que ya hayan iniciado sesión.
Lo que hace es:


> Revisar si el usuario está autenticado.


-   Si sí está autenticado, permite entrar a la vista sin problema.


-   Si NO está autenticado, lo redirige automáticamente a la página de
    > inicio de sesión.


Se utiliza para proteger funcionalidades importantes como:


Publicar artículos, Editar información, Acceder al perfil y Realizar
compras


En este proyecto, protege la vista add_item().


**Urls.py (Las rutas a cada acción nueva en views)**


Este archivo contiene las rutas que conectan las URLs del navegador con
las funciones (vistas) que las procesan.


En este proyecto se agregaron rutas nuevas para:


**/login/**


Ruta que muestra el formulario de inicio de sesión y procesa la
autenticación del usuario.\
Llama a la vista: login_user()


**/logout/**


Ruta que cierra la sesión del usuario y lo envía de vuelta al login.\
Llama a la vista: logout_user()


**/item/\<id\>/**


Ruta dinámica que muestra el detalle de un artículo según su ID.\
Llama a la vista: detail()


**/add-item/**


Ruta que muestra el formulario y procesa la creación de un nuevo
artículo.\
Llama a la vista: add_item()


Estas rutas permiten navegar entre las partes principales de la
aplicación store.


from django.urls import path
from django.contrib.auth import views as auth_views
from .views import contact, detail, register, logout_user, add_item


from .forms import LoginForm


urlpatterns = [
    path('contact/', contact, name='contact'),
    path('register/', register, name='register'),
    path('login/', auth_views.LoginView.as_view(template_name='store/login.html', authentication_form=LoginForm), name='login'),
    path('logout/', logout_user, name='logout'),
    path('add_item/', add_item, name='add_item'),
    path('detail/<int:pk>/', detail, name='detail'),
]




**store/templates (item.html, login.html, signup.html,**


**navigation.html, form.html)**


Estas plantillas son archivos HTML que muestran la información al
usuario.\
Usan el motor de templates de Django para insertar variables,
formularios y lógica básica.


**item.html**


Plantilla que muestra la información detallada de un artículo
seleccionado.\
Incluye:


Imagen, Nombre del artículo, Precio, Descripción, Información del
usuario que creó la publicación\
Es renderizada por la vista detail().


{%extends 'store/base.html' %}


{% block title%} {{item.name}}|{%endblock%}


{%block content%}
<div class="container mt-4 mb-4">
 <div class="row">
    <div class="col-4">
        <img src="{{item.image.url}}" alt=""
        class="rounded" width="100%">''
    </div>
    <div class="col-8 p-4 rounded bg-light">
        <h1 class="mb-4 text-center">
            {{item.name}}
        </h1>
       <hr>
       <h4><strong>Precio ${{item.price}}</strong></h4>
       <h4><strong>Vendedor ${{item.created_by.username}}</strong></h4>


       {% if item.description %}
       <p>{{item.description}}</p>
       {% endif %}


       <a href="" class="btn btn-dark">Contacta a el vendedor</a>


    </div>
    </div>
 </div>
{%endblock%}






**login.html**


Pantalla donde el usuario ingresa sus credenciales.\
Incluye el formulario LoginForm y un botón para enviar la información.


Se renderiza con la vista login_user().


{% extends 'store/base.html' %}


{% block title %}Login| {% endblock %}


{% block content %}


<div class="row p-4 d-flex justify-content-center align-items-center">
    <div class="col-6 bg-light p-4">
        <h4 class="mb-6 text-center">Registro</h4>
        <hr>
        <form action="." method="POST">
            {% csrf_token %}
            <div class="form-floating mb-3">
                <h6>Username:</h6>
                {{form.username}}
            </div>
            <div class="form-floating mb-3">
                <h6>Password:</h6>
                {{form.password}}
            </div>




            {% if form.errors or form.non_field_errors %}
            <div class="mb-4 p-6 bg-danger text-white rounded">
                {% for field in form %}
                field.errors
                {% endfor %}
                {{ form.non_field_errors }}
            </div>
            {% endif %}
            <div class="d-flex justify-content-center align-items-center">
                <button class="btn btn-primary mb-6">Login</button>
            </div>
            <div class="d-flex justify-content-center align-items-center">
                <a href="{% url 'register' %}">¿No tienes cuenta? registrate aqui!</a>
            </div>
        </form>
    </div>
</div>






{% endblock %}








**signup.html**


Pantalla donde un usuario puede registrarse con un nuevo nombre de usuario y contraseña.\
Utiliza el formulario SignupForm.


{% extends 'store/base.html' %}


{% block title %}Registro| {% endblock %}


{% block content %}
<div class="row p-4 d-flex justify-content-center align-items-center">
    <div class="col-6 bg-light p-4">
        <h4 class="mb-6 text-center">Registro</h4>
        <hr>
        <form action="." method="POST">
            {% csrf_token %}
            <div class="form-floating mb-3">
                <h6>Username:</h6>
                {{form.username}}
            </div>
            <div class="form-floating mb-3">
                <h6>Email:</h6>
                {{form.email}}
            </div>
            <div class="form-floating mb-3">
                <h6>Password:</h6>
                {{form.password1}}
            </div>
            <div class="form-floating mb-3">
                <h6>Repite Password:</h6>
                {{form.password2}}
            </div>


            {% if form.errors or form.non_field_errors %}
                <div class="mb-4 p-6 bg-danger rounded">
                    {% for field in form %}
                        <h5 class="text-white">
                            {{field.errors}}
                        </h5>
                       
                    {% endfor %}
                    {{ form.non_field_errors }}
                </div>
            {% endif %}


            <div class="d-flex justify-content-center align-items-center">
                <button class="btn btn-primary mb-6">Register</button>
            </div>
            <div class="d-flex justify-content-center align-items-center">
                <a href="{% url 'login' %}">¿Ya tienes cuenta? Accesa aqui!</a>
            </div>
        </form>
    </div>
</div>
{% endblock %}






**navigation.html**


Es una barra de navegación que aparece en todas las páginas
importantes.\
Muestra opciones dependiendo de si el usuario está autenticado o no.\
Ejemplos:


Si está logueado → "Agregar artículo", "Cerrar sesión".


Si no está logueado → "Iniciar sesión".


Esta plantilla se incluye en el archivo base (layout general del sitio).


<nav class="navbar navbar-expand-lg bg-dark" data-bs-theme="dark">
    <div class="container-fluid">
        <a href="{% url 'home' %}" class="navbar-brand">Marketplace</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-control="navBarNav" aria-expanded="false" aria-label="Toggle Navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto">
                <li class="nav-item">
                    <a href="" class="nav-link active">
                        Home
                    </a>
                </li>
                <li class="nav-item">
                    <a href="{% url 'contact' %}" class="nav-link active">
                        Contact
                    </a>
                </li>
               
                {% if request.user.is_authenticated %}
                    <!-- nuevo link -->
                    <li class="nav-item">
                        <a class="nav-link" href="{% url 'add_item'%}">Add Item</a>
                    </li>
                    <li class="nav-item">
                        <a href="{% url 'logout' %}" class="nav-link active">
                            Logout
                        </a>
                    </li>
                {% else %}
                    <li class="nav-item">
                        <a href="{% url 'login' %}" class="nav-link active">
                            Login
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="{% url 'register' %}" class="nav-link active">
                            Register
                        </a>
                    </li>
                {% endif %}
            </ul>
        </div>
    </div>
</nav>






**form.html**


Es una plantilla reutilizable que muestra formularios en formato
ordenado.\
Se utiliza para:


Crear artículos, Iniciar sesión, Registrarse, Permite evitar repetir
código en múltiples plantillas.


{% extends 'store/base.html' %}


{% block title %} {{ title }} {% endblock %}


{% block content%}
    <h4 class="mb-4 mt-4">{{ title }}</h4>
    <hr>
    <form action="." method="POST" enctype="multipart/form-data">
        {% csrf_token %}
        <div>
       
            {{ form.as_p }}
        </div>


        {% if form.errors or form.non_field_errors %}
            <div class="mb-4 p-6 bg-danger">
                {% for field in form %}
                    {{ field.errors }}
                {% endfor %}


                {{ form.non_field_errors }}
            </div>
        {% endif %}


        <button class="btn btn-primary mb-6">Register</button>
    </form>
{% endblock%}






**Avance**


![avance](media/item_images/imagen12.png)
![avance](media/item_images/imagen13.png)
![avance](media/item_images/imagen14.png)
![avance](media/item_images/imagen15.png)
![avance](media/item_images/imagen16.png)








**8. ##Conclusión


**Conclusión:**


Django es una herramienta muy buena que permite crear aplicaciones web
de manera estructurada y profesional. Su arquitectura MVT facilita la
separación de las capas del proyecto, lo que hace que el código sea más
limpio, entendible y fácil de realizar.


El proyecto marketplace_main nos ayuda a comprender cómo se integran los
componentes básicos de un sitio web: desde la base de datos hasta la
interfaz de usuario. Además, al usar el entorno virtual, mantenemos la
instalación de paquetes ordenada y sin conflictos.


Finalmente, trabajar con Django fomenta buenas costumbres como
programador en programación web. Aprendimos a crear proyectos,
aplicaciones, vistas, modelos y plantillas, comprendiendo el flujo de
datos entre el servidor y el cliente, algo fundamental para el
desarrollo profesional en Python.



