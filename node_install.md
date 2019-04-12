
### NodeJS 官网下载

https://nodejs.org/en/download/

Linux Binaries (x64)


### 直接使用已编译好的包(Linux Binaries (x64))

1. 下载

- cd ~
- wget https://nodejs.org/dist/v10.9.0/node-v10.9.0-linux-x64.tar.xz

2. 解压

- tar xf  node-v10.9.0-linux-x64.tar.xz

3. 进入解压目录

- cd node-v10.9.0-linux-x64

4. 执行node命令 查看版本

- ./bin/node -v

5. 解压文件的 bin 目录底下包含了 node、npm 等命令，我们可以使用 ln 命令来设置软连接：

- ln -sf /root/node-v10.9.0-linux-x64/bin/npm /usr/local/bin/
- ln -sf /root/node-v10.9.0-linux-x64/bin/node /usr/local/bin/

6. 查看版本

- node -v
- npm -v