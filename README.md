# 开发环境准备（Linux）
## 安装jdk1.8
* 参考教程  
  + [https://blog.csdn.net/pxmxx/article/details/80106239](https://blog.csdn.net/pxmxx/article/details/80106239)
  + [https://blog.csdn.net/c4each/article/details/80584138](https://blog.csdn.net/c4each/article/details/80584138)
* 方式一
  + 官方下载压缩包  
    [http://www.oracle.com/technetwork/java/javase/downloads/index.html](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
  + 解压  
  ```
  sudo tar -zxvf jdk-8u171-linux-x64.tar.gz 
  ```
  + 配置  
  ```
  sudo gedit ~/.bashrc
  ```
  然后把如下命令复制到最底部
  ```
  export JAVA_HOME=/usr/local/java/jdk1.8.0_25  
  export JRE_HOME=${JAVA_HOME}/jre  
  export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib  
  export PATH=${JAVA_HOME}/bin:$PATH
  ```
  export JAVA_HOME=后面要填写自己解压后的jdk的路径
  + 生效~/.bashrc文件
  ```
  source ~/.bashrc
  ```
  + 测试是否安装成功
  ```
  java -version
  ```
* 方式二
  + 命令安装（按照教程没有成功，只能选择第一种）
## 安装git

* 首先，通过运行以下命令确保您的系统和apt包列表完全更新：  
```
apt-get update -y
apt-get upgrade -y
```
* 在Ubuntu 18.04上安装Git  
```
apt install git
```
您可以使用以下命令来检查已安装的git版本  
```
git --version
```
* 在Ubuntu 18.04上配置Git  
```
git config --global user.name "***"
git config --global user.email "***"
```
* 参考教程  
[https://www.linuxidc.com/Linux/2018-05/152610.htm](https://www.linuxidc.com/Linux/2018-05/152610.htm)

## 安装maven
* 参考教程
  + [https://www.jianshu.com/p/ce3f3df35387](https://www.jianshu.com/p/ce3f3df35387)
* 下载 Maven 安装包
  + 下载地址: [http://mirror.bit.edu.cn/apache/maven/maven-3/](http://mirror.bit.edu.cn/apache/maven/maven-3/)
* 解压安装包
  ```
  cd /usr/local
  sudo tar -xzf apache-maven-3.6.1-bin.tar.gz
  ```
* 配置环境变量, 编辑文件 ~/.bashrc, 在末尾添加
  ```
  # maven config  
  export M2_HOME=/usr/local/apache-maven-3.6.1  
  export M2=$M2_HOME/bin  
  export MAVEN_OPTS="-Xms256m -Xmx512m"  
  export PATH=$M2:$PATH  
  ```
* 使环境变量生效
  ```
  source ~/.bashrc
  ```
* 测试是否安装成功
  ```
  mvn --version  或者  mvn -v
  ```


