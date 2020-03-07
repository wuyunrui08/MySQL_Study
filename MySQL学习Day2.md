# MySQL学习

### 目录

- [约束分类](#constraints)
- [约束解释](#explain)
- - [主键约束](#main)
- - [默认值约束](#default)
- - [唯一约束](#only)
- - [外键约束](#outside)
- - [非空约束](#unnull)
- [其他(语句)](#other)

---

<h2 id="constraints"></h2>

约束分类

> 约束是一种限制,它通过对表的行或列的数据做出限制,来确保表的数据的完整性、唯一性

|约束类型|主键|默认值|唯一|外键|非空|
|:-:|:-:|:-:|:-:|:-:|:-:|
|关键字|``PRIMARY KEY``(primary key)|``DEFAULT``(default)|``UNIQUE``(unique)|``FOREIGN KEY``(foreign key)|``NOT NULL``(not null)|

---

<h2 id="explain"></h2>

### 解释:

<h2 id="main"></h2>

#### 主键:

主键是用于约束表中的一行,作为这一行的唯一的标识符,在一张表中能够精确定位到某一行,主键十分重要并且不能重复。

声明主键:

```MySQL

create table <表名>(
列1 类型 PRIMARY KEY,
列2 类型 ,
...
);

```

<h2 id="default"></h2>

#### 默认值

默认值约束算是可有可无,系统定义的一个默认的文本或者其他数据

default在使用insert into语句时体现出来比较明显。比如一个表中含有id,name,ownWords,如果使用``insert into Values('0001','Amy');``,而ownWords没有写,那么ownWords就为默认值,使用语句``select * from <表名>``可以看到该默认值是什么。

<h2 id="only"></h2>

#### 唯一约束

唯一约束规定表中的一列的值不得有重复,即这个值是唯一的。

<h2 id="outside"></h2>

#### 外键约束

外键既能确保数据的完整性,也能表现表之间的关系。

一个表可以有多个外键,每个外键必须(REFERENCES references)参考另一个表中的主键,被外键约束的列,取值必须在它的参考的列中有对应的值

<h2 id="unnull"></h2>

#### 非空约束

非空约束(NOT NULL),听名字就能够知道,被非空约束的列,在插入值时必须为非空。

---

<h2 id="other"></h2>

- 添加文件中的数据,在MySQL控制台上输入``source <路径>;``
- 添加自增guanjianzi``AUTO_INCREMENT(auto_incerment)``
- 可以使用``alter``去更改约束信息
> - 比如添加外键``alter table <表名> add foreign key(列名) references <第二个表名><第二个表名中的列名>``
> - 删除主键约束``alter table <表名> drop primary key``
> - 修改主键约束``alter table <表名> modify <列名><变量类型> primary key``

---

## DAY2 OVER
