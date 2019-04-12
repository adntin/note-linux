未成功

系统环境：Centos7.4

今天在安装 Nodejs10.15.3 的时候，报了一个警告：

WARNING: C++ Compiler too old, need g++ 4.9.4 or clang++ 3.4.2 (CXX=g++)

然后，查了一下自己系统上安装的gcc版本：4.8.5
gcc -v

好吧，不能用 yum 升级了，那就手动安装了吧

### gcc 官网下载

https://ftp.gnu.org/gnu/gcc/

1. 下载源码

- cd ~
- wget https://ftp.gnu.org/gnu/gcc/gcc-8.3.0/gcc-8.3.0.tar.gz

2. 解压源码

- tar -zxvf gcc-8.3.0.tar.gz
- cd gcc-8.3.0

3. 下载依赖

- ./contrib/download_prerequisites

4. 生成编译文件

- mkdir -p /root/gcc
- ./configure --prefix=/root/gcc --enable-checking=release --enable-languages=c,c++ --disable-multilib

5. 编译

- make
// 注：这个过程非常耗时，我的1核1G内存大约花了一个半小时

6. 安装

- make install

7. 添加环境变量

- echo 'export PATH=/root/gcc/bin:$PATH' >> /etc/profile

8. 生效环境变量

- source /etc/profile

9. 查看版本

- gcc -v