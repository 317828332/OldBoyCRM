# OldBoyCRM

# CRM���л���
python3����д����Ϊpython3.5.1��
# �����Ȳ鿴 install �ļ����� ����.
�ֹ������ļ��� logs
## ��װ˳��
### ��������
pip install -r ./install/requirement/commd.txt
###��������
pip install -r ./install/requirement/dev.txt
## pychram ����
������ֱ��������������.��ʹ��dev��������.������ز���.
dev ��������ʱ.���޸�


# �������
## celery
######��settings������
CELERY_BROKER_URL = 'amqp://guest:guest@localhost:5672/'
CELERY_ACCEPT_CONTENT = ['json']
CELERY_RESULT_BACKEND = 'db+sqlite:///results.sqlite'
CELERY_TASK_SERIALIZER = 'json'
CELERY_RESULT_SERIALIZER = 'json'

## �첽����
Ĭ��ʹ��rabbitmq��Ϊ�첽���У�������settings���޸�����ʹ����������
rabbitmq���ص�ַ:[www.rabbitmq.com/download.html](http://www.rabbitmq.com/download.html)

# ����������С��
## rabbitmq
service rabbitmq-server start
## celery
celery -A OldboyCRM worker -l info (��OLDBOYCRMĿ¼��)
## CRM
python manage.py runserver (��OLDBOYCRMĿ¼��)