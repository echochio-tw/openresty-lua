# openresty-lua
```
systemctl disable firewalld
systemctl stop firewalld
wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
yum clean all
yum makecache
yum update -y
yum install -y epel-release
yum install -y readline-devel pcre-devel openssl-devel
yum install libpcre3-dev libssl-dev perl make build-essential curl libreadline-dev libncurses5-dev -y
yum install pcre-devel openssl-devel gcc curl
yum install perl-Digest-MD5 -y
tar zxvf ngx_cache_purge-2.3.tar.gz
tar zxvf nginx-accesskey-2.0.5.tar.gz
tar zxvf openresty-1.19.3.1.tar.gz
cd openresty-1.19.3.1
./configure  --with-threads --with-file-aio --add-module=/root/nginx-accesskey-2.0.5 --add-module=/root/ngx_cache_purge-2.3
gmake
gmake install
cd ..
export PATH="/usr/local/openresty/bin:$PATH"
opm get openresty/lua-resty-string
mkdir work
cd work
mkdir conf
mkdir logs
vi conf/nginx.conf
vi /etc/systemd/system/nginx.service
systemctl enable nginx.service
systemctl start nginx.service
ls
```

```
total 28
drwx------ 2 nobody root 4096 Apr 25 23:17 client_body_temp
drwxr-xr-x 2 root   root 4096 Apr 25 23:10 conf
drwx------ 2 nobody root 4096 Apr 25 23:17 fastcgi_temp
drwxr-xr-x 2 root   root 4096 Apr 25 23:18 logs
drwx------ 2 nobody root 4096 Apr 25 23:17 proxy_temp
drwx------ 2 nobody root 4096 Apr 25 23:17 scgi_temp
drwx------ 2 nobody root 4096 Apr 25 23:17 uwsgi_temp
[root@localhost work]#
```

```
yum clean all
yum group list
yum repolist all
yum groups mark install "Development Tools"
yum groups mark convert "Development Tools"
yum groupinstall "Development Tools"
```
