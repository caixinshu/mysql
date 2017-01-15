# mysql
1、首先将mysqld服务停掉

2、在命令行中，cd 到MySQL的bin目录下，然后执行如下命令

  mysqld  --skip-grant-tables

此时命令行会停止不动，然后你另起一个命令行

3、在新的命令行中输入：mysql

就可以进入mysql了，然后在在mysql的命令行中输入修改root密码的命令；如下

>use mysql

>update user set password=password("new_pass") where user="root";

>flush privileges;

>exit

4、然后在重启mysql服务就可以了
