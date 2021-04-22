# python_django_drf_api_token_authentication_hello_1_server

python_django_drf_api_token_authentication_hello_1_server

[SERVER SIDE]

[Project Tree]

manage.py

myapi/

 |__ core/
 
 |    |__ migrations/
 
 |    |__ __init__.py
 
 |    |__ admin.py
 
 |    |__ apps.py
 
 |    |__ models.py
 
 |    |__ tests.py
 
 |    +__ views.py
 
 |__ __init__.py
 
 |__ settings.py
 
 |__ urls.py
 
 +__ wsgi.py
 

[run]

manage.py makemigrations

manage.py migrate

python manage.py runserver

settings.py

SECRET_KEY = '..........................'


http://127.0.0.1:8000/

(err)

http://127.0.0.1:8000/hello/
{

    "detail": "Authentication credentials were not provided."
    
}

http://127.0.0.1:8000/hello/?format=json

{"detail":"Authentication credentials were not provided."}

curl http://127.0.0.1:8000/hello/

{"detail":"Authentication credentials were not provided."}

http http://127.0.0.1:8000/hello/
{

    "detail": "Authentication credentials were not provided."
    
}

# 401 Unauthorized

or

# HTTP 403 Forbidden error.

create a user account :

python manage.py createsuperuser --username user1 --email a@example.com

password : k87654321


generate a token (the easiest way) :

python manage.py drf_create_token user1 

Generated token 3d6972c7f1d9d2a950c16fec6ca48b921ba253c4 for user user1

random string (to use next to authenticate) :

3d6972c7f1d9d2a950c16fec6ca48b921ba253c4


