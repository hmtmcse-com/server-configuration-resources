#### MariaDB Installation on CentOS 7
```bash
yum install mariadb-server -y
systemctl enable mariadb
systemctl start mariadb
```


#### Create Database with Encoding
```bash
CREATE DATABASE database_name default character set utf8 default collate utf8_general_ci;
```