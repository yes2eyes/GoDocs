# PostgreSQL


> 如何学、按类型分类、按关系分类



## 1. 安装

```
brew install postgresql

```

## 2. 初始化

```
init /usr/local/var/postgres

```

## 3. 启动

```

pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log start

```

## 4. 查看状态

```

pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log status

```

## 5. 停止

```

pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log stop -s -m fast

```


## 6. 创建数据库

默认的用户：xiewei

```

createdb -O xiewei dbname

createdb dbname -O postgres

```

## 7. 删除数据库


默认的用户：xiewei

```

dropdb -U xiewei  dbname
dropdb dbname

```

## 8. 增删改查


根据数据类型：

- 数值类型
  - 比较操作
  - 函数统计操作
- 文本类型
  - 拼接
  - index
  - 切片
- 时间类型
  - 比较操作
  - 年月日时分秒：单位
- 数组类型
  - 值搜索：any
  - 两数组操作

根据表：

- 单表
- 多表：连接查询：根据表之间的共同字段等: 集合的角度
  - inner join
  - full outer join
  - left outer join
  - right outer join


## 9. 常用操作


## 10. 自增序列

```sql

CREATE TABLE "students" (
    "id" int NOT NULL DEFAULT nextval('students_id_seq'::reglass),
) 


----删除前先解除 id 对该序列的依赖
ALTER TABLE tablename ALTER COLUMN id SET DEFAULT null;

DROP SEQUENCE IF EXISTS sequence_name;

---- id_max 即 id 目前的最大值，可写为1，可通过 “SELECT MAX(id) FROM tablename” 得到
CREATE SEQUENCE sequence_name START WITH id_max;
ALTER TABLE tablename ALTER COLUMN id SET DEFAULT nextval('sequence_name'::regclass);
```




- [官方文档](https://www.postgresql.org/)

## 导出

```
\o name.txt
query
\o

copy (query) to 'filepath/filename.txt' 

```