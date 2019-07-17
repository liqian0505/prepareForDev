# 开发环境准备（Linux）
## 安装git——下载源代码

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
