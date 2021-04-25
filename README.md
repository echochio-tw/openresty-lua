# openresty-lua
```
systemctl disable firewalld
systemctl stop firewalld
wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
yum clean all
yum makecache
yum update
yum install -y epel-release
yum install -y readline-devel pcre-devel openssl-devel
yum install libpcre3-dev libssl-dev perl make build-essential curl libreadline-dev libncurses5-dev
yum install pcre-devel openssl-devel gcc curl
yum repolist all
yum groups mark convert "Development Tools"
yum groupinstall "Development Tools"
yum install perl-Digest-MD5 -y
tar zxvf nginx-accesskey-2.0.5.tar.gz
tar zxvf openresty-1.19.3.1.tar.gz
cd openresty-1.19.3.1
./configure --add-module=/root/nginx-accesskey-2.0.5
```
