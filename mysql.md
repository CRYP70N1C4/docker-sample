#### ����Mysql����
```
docker pull mysql:5.7
```

#### ����mysql
```
docker run -p 3306:3306 --name mymysql -v $PWD/conf/my.cnf:/etc/mysql/my.cnf -v $PWD/logs:/logs -v $PWD/data:/mysql_data -e MYSQL_ROOT_PASSWORD=123456 -d mysql:5.7 imageId
```
    -p 3306:3306����������3306�˿�ӳ�䵽������3306�˿�
    -v $PWD/logs:/logs����������ǰĿ¼�µ�logsĿ¼���ص�������/logs
    -e MYSQL_ROOT_PASSWORD=123456����ʼ��root�û�������