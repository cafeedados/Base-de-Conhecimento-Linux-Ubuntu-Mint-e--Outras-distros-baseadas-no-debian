# MYSQL LEARNING BANK

## INSTALLING MYSQL ON LINUX MINT / UBUNTU

First we have to update linux with the commands

```bash
$ sudo apt upgrade && update
```

Then we will install MySql

```bash
$ sudo apt install mysql-server
```

Later we will create mySql access passwords with the command:

```bash
$ sudo mysql_secure_installation
```

And then we will configure ** bind-address ** for that we will access the conf file. you can use gdit or nano. i prefer gedit.

```bash
$ sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```

and inside the file we will look for the line that is written ** bind-address ** and make the following change.

```bash
From:
bind-address            = 127.0.0.1
to:
bind-address            = 0.0.0.0
```

I recommend that you download the workbench through the application window.

Usually when you log in we encounter the following error:

<img src="/img/01.png">

and we will enter the MySql terminal with the command:

```bash
$ sudo mysql -u root
```
and then we will do the root password identification

```Sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'YouKey';

```