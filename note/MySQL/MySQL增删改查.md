# MySQL的增删改查

### 一、数据库文件的操作

1. 打开MySQL客户端

   1. phpMyAdmin

      打开浏览器输入：localhost/phpmyadmin

   2. shell中打开

      打开shell输入：mysql -u root -p 确认后输入密码即可；

2. 查看数据库文件

   ```sql
   show databases;
   ```

3. 创建数据库

   ```sql
   create database 库名;
   ```

4. 删除数据库

   ```sql
   drop database 库名;
   ```

5. 选择数据库

   ```sql
   use 库名;
   ```

### 二、数据类型

![image-20191026152037410](/Users/eric/Library/Application Support/typora-user-images/image-20191026152037410.png)

### 三、数据表操作

1. 创建数据表

```sql
CREATE TABLE table_name(
	`id` INT AUTO_INCREMENT,
	`title` VARCHAR(40),
  PRIMARY KEY ( `id` )
)
```

2. 删除数据表

```sql
DROP TABLE table_name;
```

3. 插入数据

```sql
INSERT INTO table_name (field1, field2,……fieldN)
											VALUES
											( value1, value2,……valueN)；
```

4. 删除数据

```sql
DELETE FROM table_name WHERE Clause;
```

5. 修改数据

```sql
UPDATE table_name SET field1=new-value1, field2=new-value2 WHERE Clause;
```

5. 查询数据

```sql
 -- 查询表中所有学生的信息。
select * from student 

-- 查询表中所有学生的姓名和对应的英语成绩。;
select name ,english from student

-- 统计每个学生的总分。
select chinese+english+math 总份额 from student;

-- 在所有学生总分数上加10分特长分。
select chinese+english+math+10 总份额 from student;

-- 使用别名表示学生分数。
select chinese 中文,english 英语,math 数学 from student;

-- 查询姓名为李一的学生成绩
select chinese,english,math from student where name ='李一'

-- 查询英语成绩大于90分的同学
select NAME from student where english>90                                         
 
-- 查询总分大于200分的所有同学
select NAME from student where (chinese+english+math)>200;

-- 查询英语分数在 80－90之间的同学
SELECT NAME from student where english between 80 and 90;
```

