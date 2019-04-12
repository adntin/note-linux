
### MongoDB 官网下载

https://www.mongodb.com/download-center#community

```
Name: MongoDB Community Server
Verson: 4.0.8 (current release)
OS: RHEL 7.0 Linux 64-bit x64
Package: TGZ
```

1. 下载安装包

- cd ~
- wget https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-rhel70-4.0.8.tgz

2. 解压安装包

- tar -zxvf mongodb-linux-x86_64-rhel70-4.0.8.tgz
- cd mongodb-linux-x86_64-rhel70-4.0.8

3. 创建配置文件

- mkdir -p /data/db
- vim mongodb.conf

```
dbpath=/data/db
logpath=/data/db/mongodb.log
port=27017
fork=true # 后台运行
```

4. 启动服务端(后台运行)

- ./bin/mongod -config mongodb.conf

5. 查看 mongodb 进程

- ps aux | grep mongo

6. 启动客户端

- ./bin/mongo

7. 添加环境变量

- echo 'export PATH=/root/mongodb-linux-x86_64-rhel70-4.0.8/bin:$PATH' >> /etc/profile

8. 生效环境变量

- source /etc/profile

9. 查看版本

- mongod --version
- mongo --version

---

### 关闭 mongod 服务端

1. 第一种方法

- pkill mongod

2. 第二种方法

- killall mongodb

3. 第三种方法

- kill -9 MONGO-PID

4. 第四种方法

- mongo 
- db.shutdownServer()


