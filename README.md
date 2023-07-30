C:\Users>cd..

C:\>cd xampp

C:\xampp>cd mysql

C:\xampp\mysql>cd bin

C:\xampp\mysql\bin>mysql -u root
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 8
Server version: 10.4.27-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> show tables
    ->
    -> Bye
Ctrl-C -- exit!

C:\xampp\mysql\bin>show databases;
'show' is not recognized as an internal or external command,
operable program or batch file.

C:\xampp\mysql\bin>mysql -u root
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 9
Server version: 10.4.27-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| nana1              |
| nana2              |
| performance_schema |
| phpmyadmin         |
| s1                 |
| test               |
+--------------------+
8 rows in set (0.038 sec)

MariaDB [(none)]> create database jashu;
Query OK, 1 row affected (0.001 sec)

MariaDB [(none)]> use jashu;
Database changed
MariaDB [jashu]> create table details(name varchar(10),phone int,roll int);
Query OK, 0 rows affected (0.018 sec)

MariaDB [jashu]> desc details;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| name  | varchar(10) | YES  |     | NULL    |       |
| phone | int(11)     | YES  |     | NULL    |       |
| roll  | int(11)     | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
3 rows in set (0.015 sec)

MariaDB [jashu]> insert into details values("jashwanth",7485909384,41111094);
Query OK, 1 row affected, 1 warning (0.074 sec)

MariaDB [jashu]> show table details;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'details' at line 1
MariaDB [jashu]> desc details;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| name  | varchar(10) | YES  |     | NULL    |       |
| phone | int(11)     | YES  |     | NULL    |       |
| roll  | int(11)     | YES  |     | NULL    |       |
+-------+-------------+------+-----+---------+-------+
3 rows in set (0.029 sec)

MariaDB [jashu]> select * from details;
+-----------+------------+----------+
| name      | phone      | roll     |
+-----------+------------+----------+
| jashwanth | 2147483647 | 41111094 |
+-----------+------------+----------+
1 row in set (0.001 sec)

MariaDB [jashu]> insert into details values("hema",6488394749,41110061);
Query OK, 1 row affected, 1 warning (0.005 sec)

MariaDB [jashu]> select * from details;
+-----------+------------+----------+
| name      | phone      | roll     |
+-----------+------------+----------+
| jashwanth | 2147483647 | 41111094 |
| hema      | 2147483647 | 41110061 |
+-----------+------------+----------+
2 rows in set (0.001 sec)

MariaDB [jashu]> select * from details group by name;
+-----------+------------+----------+
| name      | phone      | roll     |
+-----------+------------+----------+
| hema      | 2147483647 | 41110061 |
| jashwanth | 2147483647 | 41111094 |
+-----------+------------+----------+
2 rows in set (0.001 sec)

MariaDB [jashu]> select * from details group by name desc;
+-----------+------------+----------+
| name      | phone      | roll     |
+-----------+------------+----------+
| jashwanth | 2147483647 | 41111094 |
| hema      | 2147483647 | 41110061 |
+-----------+------------+----------+
2 rows in set (0.001 sec)

MariaDB [jashu]> select * from details group by phone;
+-----------+------------+----------+
| name      | phone      | roll     |
+-----------+------------+----------+
| jashwanth | 2147483647 | 41111094 |
+-----------+------------+----------+
1 row in set (0.001 sec)

MariaDB [jashu]> select *from details group by roll;
+-----------+------------+----------+
| name      | phone      | roll     |
+-----------+------------+----------+
| hema      | 2147483647 | 41110061 |
| jashwanth | 2147483647 | 41111094 |
+-----------+------------+----------+
2 rows in set (0.001 sec)

MariaDB [jashu]> select * from details group by phone desc;
+-----------+------------+----------+
| name      | phone      | roll     |
+-----------+------------+----------+
| jashwanth | 2147483647 | 41111094 |
+-----------+------------+----------+
1 row in set (0.001 sec)

MariaDB [jashu]>
