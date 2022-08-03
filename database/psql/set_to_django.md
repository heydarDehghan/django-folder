
# How to set up Postgres in your Django project ?

### Steps
1.Install and configure Postgres.\
2.Install dependencies. \
3.Set it up in our Django project. 

## 1. Install and configure Postgres

Download Postgres here for your operating system. 

Install it.\
If you run into problems, you can check detailed instructions for your operating system here. \
Start your Postgres server/ db. 


## 2. Install dependencies

In your work environment, install psycopg2 using this command:  **pip install psycopg2**

## 3.Set it up in your Django Project

Make sure that your Postgres server/db is running. \
Click here if you don't know how.

Navigate to your project's settings.py file, and replace the DATABASE dictionary with the following:

#myProject/settings.py

'''

DATABASES = {

    'default': {

        'ENGINE': 'django.db.backends.postgresql',
        'NAME': ‘<db_name>’,
        'USER': '<db_username>',
        'PASSWORD': '<password>',
         HOST': '127.0.0.1',
        'PORT': '5432',

    }

}

'''

Use your host as 'localhost' and your port as 5432 (or to whichever port you changed to during configuration).

You can now migrate your database using **./manage.py** migrate or **python manage.py migrate** . \
Your Django Project is now using Postgres as its database.

