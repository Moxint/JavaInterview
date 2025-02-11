## 概述

由于运算的时候,float类型和double很容易丢失精准度
所以,为了能精确的表示,计算浮点数,Java提供了BigDecimal

BigDecimal类:不可变、任意精度的有符号十进制数,可以解决数据丢失问题。

常用于金融及价格计算;

## 两大类型的构造器

- 数值构造器

BigDecimal(数值类型 val)

- String字符串构造器(推荐，尽量使用字符串构造器)

BigDecimal(String val) 

## 加减乘除法

- 加法 add() 

- 减法 subtract()

- 乘法 multipy()    

- 除法 divide()    

- 绝对值 abs()

## 除法 divide() 参数使用
使用除法函数在divide的时候要设置各种参数，要精确的小数位数和舍入模式，不然会出现报错

我们可以看到divide函数配置的参数如下

	public BigDecimal divide(BigDecimal divisor, int scale, int roundingMode)  

- BigDecimal divisor 除数， 
- int scale 精确小数位，  
- int roundingMode 舍入模式)

## 8种舍入模式

- ROUND_UP

舍入远离零的舍入模式。

在丢弃非零部分之前始终增加数字(始终对非零舍弃部分前面的数字加1)。

注意，此舍入模式始终不会减少计算值的大小。

- ROUND_DOWN

接近零的舍入模式。

在丢弃某部分之前始终不增加数字(从不对舍弃部分前面的数字加1，即截短)。

注意，此舍入模式始终不会增加计算值的大小。

- ROUND_CEILING

接近正无穷大的舍入模式。

如果 BigDecimal 为正，则舍入行为与 ROUND_UP 相同;

如果为负，则舍入行为与 ROUND_DOWN 相同。

注意，此舍入模式始终不会减少计算值。

- ROUND_FLOOR

接近负无穷大的舍入模式。

如果 BigDecimal 为正，则舍入行为与 ROUND_DOWN 相同;

如果为负，则舍入行为与 ROUND_UP 相同。

注意，此舍入模式始终不会增加计算值。

- ROUND_HALF_UP

向“最接近的”数字舍入，如果与两个相邻数字的距离相等，则为向上舍入的舍入模式。

如果舍弃部分 >= 0.5，则舍入行为与 ROUND_UP 相同;否则舍入行为与 ROUND_DOWN 相同。

注意，这是我们大多数人在小学时就学过的舍入模式(四舍五入)。

- ROUND_HALF_DOWN

向“最接近的”数字舍入，如果与两个相邻数字的距离相等，则为上舍入的舍入模式。

如果舍弃部分 > 0.5，则舍入行为与 ROUND_UP 相同;否则舍入行为与 ROUND_DOWN 相同(五舍六入)。

- ROUND_HALF_EVEN

向“最接近的”数字舍入，如果与两个相邻数字的距离相等，则向相邻的偶数舍入。

如果舍弃部分左边的数字为奇数，则舍入行为与 ROUND_HALF_UP 相同;

如果为偶数，则舍入行为与 ROUND_HALF_DOWN 相同。

注意，在重复进行一系列计算时，此舍入模式可以将累加错误减到最小。

此舍入模式也称为“银行家舍入法”，主要在美国使用。四舍六入，五分两种情况。

如果前一位为奇数，则入位，否则舍去。

以下例子为保留小数点1位，那么这种舍入方式下的结果。

1.15>1.2 1.25>1.2

- ROUND_UNNECESSARY

断言请求的操作具有精确的结果，因此不需要舍入。


