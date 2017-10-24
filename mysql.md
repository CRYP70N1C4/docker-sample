#### 下载Mysql镜像
```
docker pull mysql:5.7
```

#### 启动mysql
```
docker run -p 3306:3306 --name mymysql -v $PWD/conf/my.cnf:/etc/mysql/my.cnf -v $PWD/logs:/logs -v $PWD/data:/mysql_data -e MYSQL_ROOT_PASSWORD=123456 -d mysql:5.7 imageId
```
    -p 3306:3306：将容器的3306端口映射到主机的3306端口
    -v $PWD/logs:/logs：将主机当前目录下的logs目录挂载到容器的/logs
    -e MYSQL_ROOT_PASSWORD=123456：初始化root用户的密码