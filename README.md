# Learn-Django-Celery-with-RabbitMQ
https://www.youtube.com/watch?v=fBfzE0yk97k

Commands:
python3 -m venv venv """makes a python 3 virtual environment"""
source venv/bin/activate """activates venv"""
pip install celery django """install celery and django"""
django-admin startproject proj . """the dot avoids nested folder proj/proj"""
sudo apt-get install rabbitmq-server """installs rabbit mq"""
sudo systemctl enable rabbitmq-server """enable rabbitmq server"""
sudo systemctl start rabbitmq-server """start rabbitmq server"""
systemctl status rabbitmq-server """check its working"""
celery -A proj worker -l info """run celery"""

Following this open django shell using:
python3 manage.py shell

Then:
from app1.tasks import add 
add.delay(4,4) """uses add to add 4 + 4"""
add.apply_async((3,3), countdown=5) """adds 5 second delay to count"""

If celery is running in one terminal and django shell in another you will see the result of the calculation in the celery terminal following any delay