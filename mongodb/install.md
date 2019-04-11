
### MongoDB 官网下载

https://www.mongodb.com/download-center#community

### 演示目录

cd ~

### 下载安装包

wget https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-rhel70-4.0.8.tgz

###  解压安装包

tar -zxvf mongodb-linux-x86_64-rhel70-4.0.8.tgz

### 进入 mongodb 目录

cd mongodb-linux-x86_64-rhel70-4.0.8.tgz

### 创建配置文件

vim mongodb.conf

```
dbpath=/data/db
logpath=/data/db/mongodb.log
port=27017
fork=true # 后台运行
```

### 启动服务端

./bin/mongod -config mongodb.conf

### 查看 mongodb 进程

ps aux | grep mongo

### 启动客户端

./bin/mongo

