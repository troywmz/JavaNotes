# 类型和运算

## 字面量和常量

**常量** ：程序中固定不变的值

**字面量**：直接给出的一个值

常量分类：
1. 字面值常量：如整数常量1,2,3，
2. `final` 变量

## 变量

### 变量的特点

**变量**：表示存储空间用来存储某一类型的常量。
特点：
1. 占据内存中某块存储区域
2. 该区域有名称（变量名）和类型（数据类型）
3. 可以被重复使用
4. 数据可以再同一类型范围内不断变化

### 变量的分类

1. 成员变量/字段：
	- 直接定义在类中（方法外）
	- 使用static修饰
2. 局部变量
	- 除了成员变量

### 变量的作用域

1. 成员变量：所定义的类中起作用
2. 局部变量：定义的地方到最近的`}`之间

#### tips：

1. 成员变量可以先使用后定义，局部变量先定义后使用
2. 就近局部变量覆盖全局变量

## 表达式

###表达式定义

**表达式**：由数字、运算符、数字分组符（括号）、常量、变量等能求得有意义结果的组合

## 数据类型和分类

- 基本/原生 类型
	- 数值型
		- 整数类型
			- byte：1字节
			- short：2字节
			- int：4字节
			- long：8字节
		- 小数类型
			- float：4字节
			- double：8字节
	- 字符型
		-char：2字节
	- 布尔型
		- boolean：1位
- 引用/对象 类型
	- 类
	- 接口
	- 数组

### boolean类型

通常用于逻辑运算

只能使用 `true` 和 `false` 表示，不能使用0和非零整数

### 整数类型

常见形式
1. 二进制：`0B` / `0b` 开头
2. 八进制：`0` 开头
3. 十进制
4. 十六进制：`0X` / `0x` 开头
5. long类型：`l`/`L` 结尾

#### tips：
**java7** 开始，数字之间可加下划线，eg. `0011_1110`

### 小数/浮点 类型
`float`：单精度

`double`：双精度

表现形式：
1. 十进制：3.14, 6.280, .628
2. 科学计数法：3.14e2, 3.14e-2

#### tips：
`float` `double` 都不能精确地表示小数

小数常量默认是 `double`类型, 末尾加 `f` / `F` 表示 `float`。所以赋值给 `float` 变量需要加 `f` / `F`

科学计数法返回 `double` 类型，可在末尾加 `f` / `F`

银行使用 `BigDecimal` 表示任意精度

### 字符类型
**char**类型：16位无符号整数或 `Unicode` 字符

表现形式：
1. 直接使用字符表示，如 `'A'`, `'7'`
2. 作为十进制整数使用，打印出的依然是ASCII字符(0~127)
3. 使用十六进制表示，eg. `'\u0061'`（四位十六进制数）

### 字符串类型

**String**类型

#### tips

1. 字符串和任意数据类型连接，结果都是字符串 eg. `7 + 8 + hello`
2. 字符串赋值必须有双引号， eg. `String a = 17` 错误

## 基本数据类型转换

### 数据过大和溢出
