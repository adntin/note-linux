未成功

### NodeJS 官网下载

https://nodejs.org/en/download/

Source Code


1. 下载源码(Source Code)

- cd ~
- wget https://nodejs.org/dist/v10.15.3/node-v10.15.3.tar.gz

2. 解压源码

- tar -zxvf node-v10.15.3.tar.gz
- cd node-v10.15.3

3. 生成编译文件

- mkdir -p /root/node/10.15.3
- ./configure --prefix=/root/node/10.15.3

4. 编译

- make

5. 安装

- make install

6. 添加环境变量

- echo 'export PATH=/root/node/10.15.3/bin:$PATH' >> /etc/profile

7. 生效环境变量

- source /etc/profile

8. 查看版本

- node -v

---

### 编译报错

WARNING: C++ compiler too old, need g++ 4.9.4 or clang++ 3.4.2 (CXX=g++)
注意: 如果版本号低于4.9.4，请先升级gcc

### 检查 gcc 的版本

gcc -v
