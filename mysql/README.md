

```
mysql５.7　之后是mysql8, 修改变动比较大，使用方式也有改动，暂时只用mysql5.7

docker run --name mysql5.7-p 192.168.1.100:3306:3306 -v /data/docker/mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=pwd@123A -d mysql:5.7

docker run --name mysql5.7--net=host -v /data/docker/mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=pwd@123A -d mysql:5.7
```
---

```
不指定密码，默认123456
修改和授权
ALTER USER 'root'@'localhost' IDENTIFIED BY 'newpassword';
GRANT ALL ON *.* TO 'username'@'localhost' IDENTIFIED BY 'password' WITH GRANT OPTION;

mysql> show variables like "%character%";
+--------------------------+----------------------------+
| Variable_name            | Value                      |
+--------------------------+----------------------------+
| character_set_client     | utf8                       |
| character_set_connection | utf8                       |
| character_set_database   | utf8                       |
| character_set_filesystem | utf8                       |
| character_set_results    | utf8                       |
| character_set_server     | utf8                       |
| character_set_system     | utf8                       |
| character_sets_dir       | /usr/share/mysql/charsets/ |
+--------------------------+----------------------------+

```
