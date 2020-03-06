# MySQL学习

---

### 目录

- [注意内容](#attion)
- [启动数据库](#startmysql)
- [创建流程](#createprocess)
- [数据类型](#datatype)
- [部分功能](#partfunction)

---

<h2 id="attion"></h2>

> #### 注意: 在结尾的``;``不能漏掉

<h2 id="startmysql"></h2>

使用数据库之前得先启动数据库服务

- Linux下:``sudo service mysql start``
- windows下:``cmd -> net start mysql``

---

<h2 id="createprocess"></h2>

- 我们可以创建一个数据库,使用命令``CREATE DATABASE <数据库名称>;``
- 使用刚刚创建的数据库``USE <数据库名称>;``
- 查看数据库中有几张表``SHOW TABLES;``
> - 表是数据库中的重要组成的部分之一,数据库只是一个框架,表才是实质内容。
> - 一般情况下,一个数据库由多个表组成,而每个表之间又存在关联。

- 创建表的格式``CREATE TABLE <表的名字> (列名a 数据类型,列名2 数据类型,列名3 数据类型,......);``
- 经过创建列表的时候,可以通过``SHOW TABLES;``看到刚刚创建的表
- 向表中插入,有三种插入方式,使用以下语句
- - ``INSERT INTO <表名>(列名a,列名b,列名c......) VALUES(值1,值2,值3......)``
- - ``INSERT INTO <表名> VALUES(值1,值2,值3......)``
- - ``INSERT INTO <表名>(列名a,列名b,...[可以不全]) VALUES(值1,值2...)``
- 经过插入之后,便可以进行查询。查询可用语句``SELECT * FROM <表名>``

---

<h2 id="datatype"></h2>

### 数据类型

|数据类型|大小(字节)|用途|格式|
|-|-|-|-|
|INT|4|整数||
|FLOAT|4|单精度浮点数||
|DOUBLE|8|双精度浮点数||
|ENUM|--|单选|ENUM('a','b','c')|
|SET|--|多选|SET('a','b','c')|
|DATE|3|日期|YYYY-MM-DD|
|TIME|3|时间点或持续时间|HH:MM:SS|
|YEAR|1|年份值|YYYY|
|CHAR|0~255|定长字符串||
|VARCHAR|0~255|变长字符串||
|TEXT|0~65535|长文本数据||

---

<h2 id="partfunction"></h2>

### 部分功能

|功能|命令|
|-|-|
|使用root形式登录|mysql -u root -p + 回车|
|查看数据库|show databases;|
|连接数据库|use <数据库名称>|
|创建表|create table <表名>(列名1 类型,列名2 类型......)|
|表中添加东西|insert into <表名> (列名1,列名2,列名3) values(值1,值2,值3...)|
|查看表|show tables;|
|查看表的内容|select * from <表名>|
|退出|quit;或者exit;|

---

## DAY ONE STUDY OVER!



