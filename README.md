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

