# Django Celery Example

Example used in the blog post [How to Use Celery and RabbitMQ with Django](https://simpleisbetterthancomplex.com/tutorial/2017/08/20/how-to-use-celery-with-django.html?utm_source=github&utm_medium=repository)

## Running Locally

```bash
git clone https://github.com/sibtc/django-celery-example.git
```

```bash
pip install -r requirements.txt
```

```bash
python manage.py migrate
```

```bash
python manage.py runserver
```


For Celery 4.0+ on Win10 install gevent 
```bash
pip install gevent
celery -A mysite worker -l info -P gevent
```

Make sure you have RabbitMQ service running.

```bash
rabbitmq-server
```

Using Docker
```bash
docker pull rabbitmq:3-management
docker run --rm -it --hostname my-rabbit -p 15672:15672 -p 5672:5672 rabbitmq:3-management
```
 http://localhost:15672 
 guest:guest

For more info see the Blog post.