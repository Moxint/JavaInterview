# SQL语言的功能有哪些
	
SQL是结构化查询语句(Structured Query Language)的缩写，
其功能包括

- 数据查询

数据查询是是最常见的操作，通过select语句可以得到所需的信息；
SELECT 选择符合条件的记录 

	SELECT * FROM table_name WHERE 条件语句;
						
- 数据操作

	DML(Data Manipulation Language, DML)主要是包括插入数据、修改数据、以及删除数据3种语言，即插改删；
	
		INSERT 插入一条记录 
		语法格式：INSERT INTO table_name (字段1, 字段2, ...) VALUES (值1, 值2, ...);
		
		UPDATE 更新语句
		语法格式：UPDATE TABLE SET 字段名 = 字段值 WHERE 条件表达式;
		
		DELETE 删除记录
		语法格式：DELETE FROM table_name WHERE 条件表达式;
				
				
- 数据定义
		DLL(Data Definition Language)实现数据定义的功能，可以对数据库用户、视图、撤销、索引进行定义与撤销；
		
		CREATE 数据表的建立
		CREATE TABLE table_name (字段1, 字段2, ....);
		
		DROP 数据表的删除
		DROP TABLE table_name;
							
- 数据控制

	DCL(Data Control Language)用于对数据库进行统一的控制管理，保证数据在多用户共享下能够按期
	
		GRANT 为用户授予系统权限
		GRANT <系统权限> | <角色> [, <系统权限> | <角色>] ...TO <用户名> | <角色> PUBLIC [, <用户名> | <角色>]...[WHIT ADMIN OPTION];
		
		REVOKE 收回系统权限				
		REVOKE <系统权限> | <角色> [, <系统权限> | <角色>] ...FROM <用户名> | <角色> PUBLIC [, <用户名> | <角色>]...
