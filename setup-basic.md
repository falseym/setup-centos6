# New User
1. Create the user:
```ssh
useradd matthew
passwd matthew
```
2. Add the user to the wheel group for sudo privileges:
```ssh
cd /etc
chmod +w sudoers
vi sudoers
[Edit sudoers file, enable %wheel
chmod -w sudoers

usermod -aG wheel matthew
```

# Git
```
sudo yum install git
```

# wget
```
sudo yum install wget
```

# Java
http://tecadmin.net/install-java-8-on-centos-rhel-and-fedora/#

```ssh
cd /opt/
wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u91-b14/jdk-8u91-linux-x64.tar.gz"

tar xzf jdk-8u91-linux-x64.tar.gz
```

```ssh
cd /opt/jdk1.8.0_91/
alternatives --install /usr/bin/java java /opt/jdk1.8.0_91/bin/java 2
alternatives --config java


There are 3 programs which provide 'java'.

  Selection    Command
-----------------------------------------------
*  1           /opt/jdk1.7.0_71/bin/java
 + 2           /opt/jdk1.8.0_45/bin/java
   3           /opt/jdk1.8.0_77/bin/java
   4           /opt/jdk1.8.0_91/bin/java

Enter to keep the current selection[+], or type selection number: 4
```

# Cassandra
http://docs.datastax.com/en/cassandra/3.0/cassandra/cassandraAbout.html
http://docs.datastax.com/en/cassandra/3.0/cassandra/install/installRHEL.html
http://docs.datastax.com/en/cassandra/3.0/cassandra/initialize/initSingleDS.html

# Update python
```ssh
sudo yum groupinstall "Development Tools"
sudo yum groupinstall "Additional Development"
sudo yum install zlib
sudo yum install zlib-devel
```

http://ask.xmodulo.com/install-python3-centos.html
http://thecpaneladmin.com/how-to-upgrade-python-on-centos/
```
sudo yum groupinstall -y "Development tools"
sudo yum install -y zlib-devel
sudo yum install -y bzip2-devel
sudo yum install -y openssl-devel
wget http://www.python.org/ftp/python/2.7.6/Python-2.7.6.tar.xz
tar xf Python-2.7.6.tar.xz
cd Python-2.7.6
./configure --prefix=/usr
make
sudo make altinstall
```
