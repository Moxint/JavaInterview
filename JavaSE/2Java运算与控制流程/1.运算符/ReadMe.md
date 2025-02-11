# 算数运算符

Java语言包括的算术运算符:

![](img/算术运算符.png)

在Java中，整数使用以上运算符，无论怎么计算，都不会得到小数

“++”运算，变量自己增1，反之"--"运算，变量自己会减1
	
- 独立运算：
	+ 变量在独立运算时，前++和后++没有区别
	+ 变量前++，例如++i
	+ 变量后++，例如i++

- 混合运算
	+ 和其他变量放在一起，前++和后++就产生了不同
	+ 变量前++，变量a自己加1，将加1后的结果赋值给b，也就是说a先计算，a和b的结果都是2
	+ 变量后++，变量a先将自己的值1，赋值给变量b，此时变量b的值就是1，变量a自己再加1，a的结果为2，b的结果是1
	
"+"符号在字符串中的操作
- +符号在遇到字符串的时候，表示连接、拼接的含义
- "a"+"b"的结果为"ab"，连接含义


# 赋值运算符	

Java语言包括的赋值运算符:

![](img/赋值运算符.png)

赋值运算符，就是将符号右边的值，赋值给左边的变量

# 比较运算符

Java语言包括的比较运算符:

![](img/比较运算符.png)

比较运算符，是两个数据之间进行比较的运算，运算结果都是布尔值true或false

# 逻辑运算符

Java语言包括的逻辑运算符:

![](img/逻辑运算符.png)

逻辑运算符，是用来连接两个布尔类型结果的运算符，运算结果都是布尔值true或false

# 三元运算符

格式：
	
	数据类型 变量名 = 布尔类型表达式？结果1：结果2

三元运算符的计算方式：
	
- 布尔类型表达式结果是true，三元运算符整体结果为结果1，赋值给变量。
- 布尔类型表达式结果是false，三元运算符整体结果为结果2，赋值给变量。

[]()