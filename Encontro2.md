---
title: 2° Encontro
layout: template
filename: Encontro2
button: Encontro2
blocker: 1
--- 
- Na pasta MineChest
  - Arquivo de configurações "<a href="#gotoseecode" onclick="Mudarestado('settings')">settings.py</a>"
  - Arquivo das urls "<a href="#gotoseecode" onclick="Mudarestado('minechesturls')">urls.py</a>"
- Na pasta pages
  - Arquivo das urls "<a href="#gotoseecode" onclick="Mudarestado('pagesurls')">urls.py</a>"
  - Arquivo de views "<a href="#gotoseecode" onclick="Mudarestado('pagesviews')">views.py</a>"
- Criar a pasta "<a href="https://github.com/E2PC/ProjectPage/blob/gh-pages/archieves/templates.rar?raw=true" download>templates"</a>
  - Criar a página Base.html
  - Criar a página home.html
  - Na pasta templates, criar a pasta "account"
    - Criar a página login.html
    - Criar a página logout.html
    - Criar a página signup.html
	
<br><br>  
<div type="hidden" id="gotoseecode"></div><br>
<div style="display:none" class="TableBody" id="pagesurls">
<textarea readonly rows='20' cols='100'> 
#Arquivo Pages/urls.py
{% raw %}
from django.urls import path
from . import views

app_name = "pages"

urlpatterns = [
	path("", views.HomePageView.as_view(), name="home"),
]
{% endraw %}
</textarea>
</div>

<div style="display:none" class="TableBody" id="pagesviews">
<textarea readonly rows='20' cols='100'> 
#Arquivo Pages/views.py
{% raw %}
from django.views.generic import TemplateView
from django.http import HttpResponse
from django.shortcuts import render

class HomePageView(TemplateView):
	template_name = "home.html"
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

LANGUAGE_CODE = 'en-us'

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
	
<div style="display:none" class="TableBody" id="minechesturls">
<textarea readonly rows='20' cols='100'>
#Arquivo MineChest/Urls
{% raw %}
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
	path("admin/", admin.site.urls),
	path("accounts/", include("allauth.urls")),
	# Local
	path("", include("pages.urls", namespace="pages")),
]
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
