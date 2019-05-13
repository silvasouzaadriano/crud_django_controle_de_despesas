# crud_django_controle_de_despesas
# Instalar python 3.7.x (https://www.python.org/downloads/)
# Instalar IDE PyCharm versçao Community (https://www.jetbrains.com/pycharm/download/#section=windows) 
1- Note que esse item é opcional

# Comandos para criar o projeto e instalar o Django no ambiente virtual do projeto
 1- mkdir meuProjeto
 2- c:\meuProjeto\python -m venv venv
 3- c:\meuProjeto\venv\scripts\activate
 4- c:\meuProjeto\pip install django
 5- c:\meuProjeto\django-admin startproject <nome do projeto, ie: controle_gastos> .

# Criando uma app
 1- c:\meuProjeto\python manage.py startapp contas
Registrar a app criado, no setting.py (tópico INSTALLED_APPS)
 i.e: 
 INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'contas',
]


# Instalando o bootstrap
 1- c:\meuProjeto\pip install django-bootstrap-form
Registrá-lo no setting.py (tópico INSTALLED_APPS).
 i.e: 
 INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'contas',
    'bootstrapform',
]

# Criando usuário admin da aplicação (superuser)
 1- Execute Control-C para parar o servidor, depois execute:
c:\meuProjeto\python manage.py createsuperuser
user=admin
psw=django01

# Criando o DB sqlite3
1- c:\meuProjeto\python manage.py migrate

# Após criar seus models, execute os comandos abaixo para criar as tabelas no DB. Note que o servidor deve estar fora do ar
1- python manage.py makemigrations
python manage.py migrate

# Após criar as tabelas, registrá-las no django admin(admin.py) para que elas possam ficar disponíveis no módulo admin
1- i.e:
admin.site.register(Categoria)
admin.site.register(Transacao)

# Rodando a aplicação (http://127.0.0.1:8000/home)
1- c:\meuProjeto\python manage.py runserver







