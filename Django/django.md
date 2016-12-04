# Install Djando

    # pip install django

	>>> import django
	>>> django.VERSION      # test if installation succeed

	# django-admin --version

# Create a project

    # django-admin startproject mysite

生成如下目录：

	mysite/
		manage.py
		mysite/
			__init__.py
			settings.py
			urls.py
			wsgi.py

# Run development server

	# python manage.py runserver

The default port is 8000, visit the web site via http://localhost:8000/


Specify the web port:

	# python manage.py runserver 80

修改 mysite/settings.py， ALLOWED_HOSTS=['192.168.137.188']，以如下方式启动development server，虚拟机外的机器可以访问：

	# python manage.py runserver 0.0.0.0：8000

# Create a webapp

	# python manage.py startapp polls 

生成如下目录：

	polls/
		__init__.py
		admin.py
		apps.py
		models.py
		tests.py
		views.py
		migrations./
			__init__.py
