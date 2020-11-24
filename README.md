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