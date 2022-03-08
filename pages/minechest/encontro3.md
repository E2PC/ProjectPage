---
title: 3° Encontro
layout: template
filename: encontro3
button: Encontro3
type: minechest
--- 
- Criar a pasta "<a href="https://github.com/E2PC/ProjectPage/blob/gh-pages/assets/archieves/static.rar?raw=true" download>static</a>"
  - Criar a Pasta dos arquivos css
    - Desenvolver os arquivos de fonte/estilo
  - Criar a Pasta dos arquivos de imagem
    - Inserir as imagens necessárias no projeto
- Na pasta MineChest
  - Arquivo de configurações "<a href="#gotoseecode" onclick="Mudarestado('settings')">settings.py</a>"
- Na pasta "<a href="https://github.com/E2PC/ProjectPage/blob/gh-pages/assets/archieves/templates-3E.rar?raw=true" download>templates</a>"
  - Alterar os arquivos html inserindo a estrutura e importando os arquivos estáticos
	
<br><br>  
<div style="display:none" class="TableBody" id="settings">
<textarea readonly rows='20' cols='100'>
#Arquivo MineChest/settings.py
{% raw %}
from pathlib import Path
import os
import allauth

BASE_DIR = Path(__file__).resolve().parent.parent

SECRET_KEY = 'django-insecure-wgx)lh*&*2dhx*2j$vgk828)98wsb+^kp5y&8^c&&v+=zr64(w'

DEBUG = True

ALLOWED_HOSTS = []


INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    "django.contrib.sites", 
	# 3rd party
	"allauth",
	"allauth.account",
	"allauth.socialaccount",
	"crispy_forms",
    "pages.apps.PagesConfig",
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

ROOT_URLCONF = 'MineChest.urls'

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [BASE_DIR / "templates"],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
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

WSGI_APPLICATION = 'MineChest.wsgi.application'


DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}

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

MEDIA_ROOT = 'static/'
RANDOM_IMAGE_DIR = '/item/'
RANDOM_IMAGE_EXTENSIONS = ['.jpg','.jpeg','.png','.gif']
MEDIA_URL = '/img/item/'

STATICFILES_DIRS = [
   os.path.join(BASE_DIR, 'static')
]

LANGUAGE_CODE = "pt-br"

TIME_ZONE = 'UTC'

USE_I18N = True

USE_L10N = True

USE_TZ = True

STATIC_URL = '/static/'

SITE_ID = 1

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
<div type="hidden" id="gotoseecode"></div><br>	
	
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
