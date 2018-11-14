# databasenotes
database notes

## 基本命令

```shell
# 显示授予用户的权限
SHOW GRANTS;

# 显示所有数据库
SHOW DATABASES;

# 使用指定数据库
USE `database_name`;

# 显示创建数据库的MySQL语句
SHOW CREATE DATABASE `database_name`;

# 显示所有表
SHOW TABLES;

# 显示表结构
DESC `table_name`;
```

## 查询

```shell
# 查询所有字段
SELECT * FROM `table_name`;

# 指定查询字段
SELECT `field1_name`,`field2_name` FROM `table_name`;

# 排序
SELECT * FROM `table_name` ORDER BY `field_name`;

# 限制数量
SELECT * FROM `table_name` ORDER BY `field_name` LIMIT 1;
```

### 过滤条件

```shell
SELECT * FROM `table_name` WHERE id = 25;

# OR 操作符
SELECT * FROM `table_name` WHERE id = 25 or id = 35;

# AND 操作符
SELECT * FROM `table_name` WHERE (tall = 175 or tall = 180) and age >= 25;

# IN 操作符
SELECT * FROM `table_name` WHERE id IN (25, 35);

# NOT 操作符
SELECT * FROM `table_name` WHERE id NOT IN (25, 35);

# LIKE 操作符
SELECT * FROM `table_name` WHERE name LIKE '%James%';
```

## 使用函数


## 联结表

## 内联结

```bash

```


## MySQL慢查询

```bash
# my.cnf

log-slow-queries=/var/lib/mysql/slowquery.log
long_query_time=2
log-queries-not-using-indexes
log-long-format
```

```bash
mysqldumpslow -s c -t 20 host-slow.log   # 访问次数最多的20个sql语句
mysqldumpslow -s r -t 20 host-slow.log   # 返回记录集最多的20个sql
mysqldumpslow -t 10 -s t -g "left join" host-slow.log    # 按照时间返回前10条里面含有左连接的sql语句


show global status like '%slow%'; # 查看现在这个session有多少个慢查询
show variables like '%slow%';     # 查看慢查询日志是否开启，如果slow_query_log和log_slow_queries显示为on，说明服务器的慢查询日志已经开启
show variables like '%long%';     # 查看超时阀值
create index text_index on wei(text);   # 创建索引
```
