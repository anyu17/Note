# 约束：

**概念**:①约数的作用是用于表中列上的规则,用于限制加入表的数据.

    ②约束的存在保证数据库中数据的正确性,有效性和完整性.

| 约束名称           | 描述                                                        | 关键字      |
| ------------------ | ----------------------------------------------------------- | ----------- |
| **非空约束** | 保证所有数据不能有null                                      | Not Null    |
| **唯一约束** | 保证列中说有数据各不相同                                    | Unique      |
| **主键约束** | 主键是一行数据的唯一标识,要求非空且唯一                     | Primary Key |
| **检查约束** | 保证列中的值满足某一条件                                    | CHECK       |
| **默认约束** | 保存数据时,未指定值则采用默认值                             | DEFAULT     |
| **外键约束** | 外键用来让两个表的数据之间建立连接,保证数据的一致性和完整性 | FOREIGN KEY |

**Tips:MYSQL不支持检查约束(检查约束的功能在代码中实现)**

```MySQL

DROP TABLE
IF EXISTS emp;SHOW TABLES;CREATE TABLE emp (
	id INT PRIMARY KEY auto_increment,-- ID 不重复且自动增长.
	ename VARCHAR(50) NOT NULL UNIQUE,-- 非空且不重复
	joindate DATE NOT NULL,-- 非空
	salary DOUBLE(7, 2) NOT NULL,-- 非空
	bonus DOUBLE(7, 2) DEFAULT 0 -- 没有默认为0
);SELECT * FroM emp;
desc emp;
insert into emp(id,ename,joindate,salary, bonus)
values (1,'zhang3','1999-11-11',8800,5000);
-- 主键约束,非空且唯一
insert into emp(id,ename,joindate,salary, bonus)
values (2,'li4','1999-11-11',8800,5000);
insert into emp(id,ename,joindate,salary)
values ('wang5','1999-11-11',8888);
SELECT * FROM EMP;-- auto_incrementID的不给值,自动增长
DROP table if exists emp;INSERT into emp(ename,joindate,salary,bonus)
values ('张3','1999-11-11',8800,NULL);
INSERT into emp(id,ename,joindate,salary,bonus)
VALUES(null,'li4','1999-11-11',5000,2);
ALTER TABLE emp
MODIFY COLUMN ename VARCHAR(50) CHARACTER SET utf8 COLLATE utf8_general_ci;
update emp set ename ='李四' where id = 1;
select * from emp;
update emp set ename = '张三' WHERE id = 2;`
```
<<<<<<< HEAD
=======

>>>>>>> 7651f1f80abf828c76cfd0a5ea7b733388303100
