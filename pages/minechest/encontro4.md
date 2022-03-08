---
title: 4° Encontro
layout: template
filename: encontro4
button: Encontro4
type: minechest
--- 
- Criar a pasta "<a href="https://github.com/E2PC/ProjectPage/blob/gh-pages/assets/archieves/static-4E.rar?raw=true" download>static</a>"
  - Criar a Pasta dos arquivos css
    - Desenvolver os arquivos de fonte/estilo
  - Criar a Pasta dos arquivos de imagem
    - Inserir as imagens necessárias no projeto
  - Criar a Pasta dos arquivos de scripts
    - Desenvolver a função de drag and drop
- Na pasta "<a href="https://github.com/E2PC/ProjectPage/blob/gh-pages/assets/archieves/templates-4E.rar?raw=true" download>templates</a>"
  - Alterar os arquivos html inserindo a estrutura e importando os arquivos estáticos
- Na pasta MineChest
  - Arquivo de configurações "<a href="#gotoseecode" onclick="Mudarestado('settings')">settings.py</a>"
- Na pasta users
  - Arquivo de configurações "<a href="#gotoseecode" onclick="Mudarestado('admin')">admin.py</a>"
  - Arquivo de configurações "<a href="#gotoseecode" onclick="Mudarestado('models')">models.py</a>"
  - Arquivo de configurações "<a href="#gotoseecode" onclick="Mudarestado('forms')">forms.py</a>"
  - Arquivo de configurações "<a href="#gotoseecode" onclick="Mudarestado('apps')">apps.py</a>"
  - Criar a Pasta dos arquivos de "templatetags"
    - Arquivo de configurações "<a href="#gotoseecode" onclick="Mudarestado('random_image')">random_image.py</a>"
	- Arquivo de configurações "<a href="#gotoseecode" onclick="Mudarestado('random_numbers')">random_numbers.py</a>"

	
<br><br>  
<div type="hidden" id="gotoseecode"></div>
<br><br>
<div style="display:none" class="TableBody" id="random_image">
<textarea readonly rows='20' cols='100'>
#Arquivo users/random_image.py
{% raw %}
import os
import random
from django import template
from django.conf import settings

register = template.Library()

@register.simple_tag
def random_image(image_dir):
    try:
        valid_extensions = settings.RANDOM_IMAGE_EXTENSIONS
    except AttributeError:
        valid_extensions = ['.jpg','.jpeg','.png','.gif',]

    if image_dir:
        rel_dir = image_dir
    else:
        rel_dir = settings.RANDOM_IMAGE_DIR
    rand_dir = os.path.join(settings.MEDIA_ROOT, rel_dir)

    files = [f for f in os.listdir(rand_dir) if os.path.splitext(f)[1] in valid_extensions]

    return os.path.join(rel_dir, random.choice(files))
    

{% endraw %}
</textarea>
</div>

<div style="display:none" class="TableBody" id="random_numbers">
<textarea readonly rows='20' cols='100'>
#Arquivo users/random_numbers.py
{% raw %}
import random
from django import template

register = template.Library()

# Para gerar o numero aleatorio para a meta
@register.simple_tag
def random_int():
    randomnumber = random.randint(15, 50)
    return randomnumber
  
# Usado para qualquer estrutura de repetição
@register.filter(name='times') 
def times(number):
    return range(number)
 
{% endraw %}
</textarea>
</div>

<div style="display:none" class="TableBody" id="admin">
<textarea readonly rows='20' cols='100'>
#Arquivo users/admin.py
{% raw %}
from django.contrib import admin
from django.contrib.auth import admin as auth_admin

from .forms import UserChangeForm, UserCreationForm
from .models import User


@admin.register(User)
class UserAdmin(auth_admin.UserAdmin):
    form = UserChangeForm
    add_form = UserCreationForm
    model = User
    fieldsets = auth_admin.UserAdmin.fieldsets + (
        ("Informações Pessoais", {"fields": ("bio",)}),
    )
{% endraw %}
</textarea>
</div>	

<div style="display:none" class="TableBody" id="models">
<textarea readonly rows='20' cols='100'>
#Arquivo users/models.py
{% raw %}
from django.contrib.auth.models import AbstractUser
from django.db import models

class User(AbstractUser):
    bio = models.TextField(blank=True)
{% endraw %}
</textarea>
</div>	

<div style="display:none" class="TableBody" id="forms">
<textarea readonly rows='20' cols='100'>
#Arquivo users/forms.py
{% raw %}
from django.contrib.auth import forms

from .models import User


class UserChangeForm(forms.UserChangeForm):
    class Meta(forms.UserChangeForm.Meta):
        model = User


class UserCreationForm(forms.UserCreationForm):
    class Meta(forms.UserCreationForm.Meta):
        model = User
{% endraw %}
</textarea>
</div>	

<div style="display:none" class="TableBody" id="apps">
<textarea readonly rows='20' cols='100'>
#Arquivo users/apps.py
{% raw %}
from django.apps import AppConfig

class UsersConfig(AppConfig):
    name = 'users'
{% endraw %}
</textarea>
</div>	

<div style="display:none" class="TableBody" id="settings">
<textarea readonly rows='20' cols='100'>
#Arquivo MineChest/settings.py
{% raw %}
from pathlib import Path
import os
import allauth

BASE_DIR = Path(__file__).resolve().parent.parent


# SECURITY WARNING: keep the secret key used in production secret!
SECRET_KEY = "3dg*3m4!^iu&3bym0f_0h&7_nykish33o_-vgrfv014ltza00g"

# SECURITY WARNING: don't run with debug turned on in production!
DEBUG = True

ALLOWED_HOSTS = []


INSTALLED_APPS = [
    # django
    "django.contrib.admin",
    "django.contrib.auth",
    "django.contrib.contenttypes",
    "django.contrib.sessions",
    "django.contrib.messages",
    "django.contrib.staticfiles",
    "django.contrib.sites",
    # 3rd party
    "allauth",
    "allauth.account",
    "allauth.socialaccount",
    "crispy_forms",
    # local pages
    "users.apps.UsersConfig",
    "pages.apps.PagesConfig",
] 

AUTH_USER_MODEL = "users.User"

MIDDLEWARE = [
    "django.middleware.security.SecurityMiddleware",
    "django.contrib.sessions.middleware.SessionMiddleware",
    "django.middleware.common.CommonMiddleware",
    "django.middleware.csrf.CsrfViewMiddleware",
    "django.contrib.auth.middleware.AuthenticationMiddleware",
    "django.contrib.messages.middleware.MessageMiddleware",
    "django.middleware.clickjacking.XFrameOptionsMiddleware",
]

ROOT_URLCONF = "MineChest.urls"  

TEMPLATES = [
    {
        "BACKEND": "django.template.backends.django.DjangoTemplates",
        "DIRS": [BASE_DIR / "templates"],
        "APP_DIRS": True,
        "OPTIONS": {
            "context_processors": [
                "django.template.context_processors.debug",
                "django.template.context_processors.request",
                "django.contrib.auth.context_processors.auth",
                "django.contrib.messages.context_processors.messages",
            ],
        },
    },
]

TEMPLATE_CONTEXT_PROCESSORS = (
    "django.contrib.auth.context_processors.auth",
    "django.core.context_processors.debug",
    "django.core.context_processors.i18n",
    "django.core.context_processors.media",
    "django.core.context_processors.static",
    "django.contrib.messages.context_processors.messages"
)

WSGI_APPLICATION = "MineChest.wsgi.application"

DATABASES = {
    "default": {
        "ENGINE": "django.db.backends.sqlite3",
        "NAME": BASE_DIR / "db.sqlite3",
    }
}

AUTH_PASSWORD_VALIDATORS = [
    {
        "NAME": "django.contrib.auth.password_validation.UserAttributeSimilarityValidator",
    },
    {
        "NAME": "django.contrib.auth.password_validation.MinimumLengthValidator",
    },
    {
        "NAME": "django.contrib.auth.password_validation.CommonPasswordValidator",
    },
    {
        "NAME": "django.contrib.auth.password_validation.NumericPasswordValidator",
    },
]

# IMG URL
MEDIA_ROOT = 'static/'
RANDOM_IMAGE_DIR = '/item/'
RANDOM_IMAGE_EXTENSIONS = ['.jpg','.jpeg','.png','.gif']
MEDIA_URL = '/img/item/'

STATICFILES_DIRS = [
   os.path.join(BASE_DIR, 'static')
]

LANGUAGE_CODE = "pt-br"

TIME_ZONE = "UTC"

USE_I18N = True

USE_L10N = True

USE_TZ = True


STATIC_URL = '/static/'


# Django-allauth

AUTHENTICATION_BACKENDS = [
    "django.contrib.auth.backends.ModelBackend",
    "allauth.account.auth_backends.AuthenticationBackend",
]

SITE_ID = 1
EMAIL_BACKEND = "django.core.mail.backends.console.EmailBackend"
LOGIN_REDIRECT_URL = "/"
ACCOUNT_SESSION_REMEMBER = True
ACCOUNT_SIGNUP_PASSWORD_ENTER_TWICE = False
ACCOUNT_USERNAME_REQUIRED = False
ACCOUNT_AUTHENTICATION_METHOD = "email"
ACCOUNT_EMAIL_REQUIRED = True
ACCOUNT_UNIQUE_EMAIL = True


# crispy-forms

CRISPY_TEMPLATE_PACK = "bootstrap4"

{% endraw %}
</textarea>
</div>	

<script>
	function Mudarestado(id) {
		document.querySelectorAll(".TableBody").forEach(function(div) {
		if (div.id == id) {
			div.style.display = div.style.display == "none" ? "block" : "none";
		} else {
			div.style.display = "none";
		}
	  });
	}
</script>
