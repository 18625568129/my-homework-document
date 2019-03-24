#js笔记


## 1.js组成
### 1.组成部分
	 ecmascript   js标准 js基础语法
      dom        通过js操作网页元素  网页中的任意标签被称为dom元素
      bom        通过api操作浏览器
### 2.特点
     简单易用，解释执行
	 编译执行  java  c#  转化为.class可执行文件==>电脑读取.class可执行文件
	 基于对象，面向过程
### 3.作用
	表单验证，轮播特效，开发游戏
## 2.JS书写位置
	a.内嵌式
	<script type="text/javascript">
		alert("欢迎您")；
	</script>
	
	b外链式
		<meta charset="utf-8">
		<title>js</title>
		<script src="./js/main.js"></script>
### 2.1.js输出内容
	1.alert()  在页面弹出一个对话框，早期JS调试使用。
	2.Confirm()  在页面弹出一个对话框, 常配合if判断使用。
	3.console.log()  将信息输入到控制台，用于js调试。
	4.document.write()在页面输出消息    几乎不用
	document.write不仅能输出信息，还能输出标签。
	转义字符 \
	\”   转双引
	\’转单引
	\n转换行
	\r 转回车
### 2.2.JS注释
	快捷键  ctrl+/
	单行注释   //
	多行注释  /*  */
## 3.变量
	与代数一样，JavaScript 变量可用于存放值（比如 x=2）和表达式（比如 z=x+y）。
	变量可以使用短名称（比如 x 和 y），也可以使用描述性更好的名称（比如 age, sum, totalvolume）。

	变量必须以字母开头
	变量也能以 $ 和 _ 符号开头（不过我们不推荐这么做）
	变量名称对大小写敏感（y 和 Y 是不同的变量）
	***提示：JavaScript 语句和 JavaScript 变量都对大小写敏感。***
## 4.JavaScript 数据类型
	JavaScript 变量还能保存其他数据类型，比如文本值 (name="Bill Gates")。
	在 JavaScript 中，类似 "Bill Gates" 这样一条文本被称为字符串。
	JavaScript 变量有很多种类型，但是现在，我们只关注数字和字符串。
	当您向变量分配文本值时，应该用双引号或单引号包围这个值。
	当您向变量赋的值是数值时，不要使用引号。如果您用引号包围数值，该值会被作为文本来处理。
	
	例如
	var pi=3.14;
	var name="Bill Gates";
	var answer='Yes I am!';
## 5.数据类型
### 5.1简单数据类型 
	Number   数字类型
	包含正数  负数  小数
	Var   age = 10,
	Var money = 999999999 
	
	
	数字类型的表达方式
	var  age = 1000;  
	var  number = 20;
	字符串  String
	凡是用双引号或者单引号引起的都是字符串。
	var  name = ‘张三’;
	var name2 = “李四李四李四李四李四李四”

	布尔数据类型    Boolean
	只有2个值一个是true, 一个是false.   实际运算中true=1,false=0
	约定 男：true ， 女：false;
	var sex = true; 


	undefined    变量未初始化
	定义了变量，没有给变量赋值
	
	null  变量未引用  值为空   object


	基本数据类型：Number string Boolean undefined null
### 5.2复杂数据类型
	object  对象
	array  数组
### 5.3判断数据类型
	typeof
### 5.4算术运算符
	a + 加号
    两个数字类型的变量相加，得到的是一个数字类型。
    一个数字类型和一个字符串相加，得到的是一个字符串(拼接)。
	b - 减号
	  两个数字类型的变量相减，得到的是一个数字类型。
    一个数字类型和一个数字字符串相减，得到的是一个数字类型。（数据类型隐式转换）
    一个数字类型和一个非数字字符串相减，得到的是NaN,是一个数字类型。
	NaN,    not a number
	
	c / 除号
	两个数字类型的变量相除，得到的是一个数字类型。
	一个数字类型和一个数字字符串相除，得到的是一个数字类型。
	一个数字类型和一个非数字字符串相除，得到的是NaN,是一个数字类型。
	0做为除数的时候，得到结果	Infinity （无限大），是一个数字类型。
	d %  取余数
	◆优先级  有()先计算()里边的
### 5.5自增自减
	☞ i++    ++i
	如果变量没有直接参与运行中，i++  和  ++i表示的含义是：在变量原来值的基础上加1。
	i++   i先参与运算，再执行++   i+=6
	++i   ++执行，i再参与运算

	如果i++或者++i参与到运算中。 
	var   i=123;
	var   n1=i++;   该段代码的含义是： 先将i的值赋值给变量n1,然后变量i的值再加1。

	var   n2=++i;   该段代码的含义是： 先将i的值加1,然后变量i加1后的值赋值给变量n2。
## 6.Date和Math对象使用
### 6.1Date对象方法
	方法			描述
	Date()	返回当日的日期和时间。
	getDate()	从 Date 对象返回一个月中的某一天 (1 ~ 31)。
	getDay()	从 Date 对象返回一周中的某一天 (0 ~ 6)。
	getMonth()	从 Date 对象返回月份 (0 ~ 11)。
	getFullYear()	从 Date 对象以四位数字返回年份。
	getYear()	请使用 getFullYear() 方法代替。
	getHours()	返回 Date 对象的小时 (0 ~ 23)。
	getMinutes()	返回 Date 对象的分钟 (0 ~ 59)。
	getSeconds()	返回 Date 对象的秒数 (0 ~ 59)。
	getMilliseconds()	返回 Date 对象的毫秒(0 ~ 999)。
	getTime()	返回 1970 年 1 月 1 日至今的毫秒数。
	getTimezoneOffset()	返回本地时间与格林威治标准时间 (GMT) 的分钟差。
	getUTCDate()	根据世界时从 Date 对象返回月中的一天 (1 ~ 31)。
	getUTCDay()	根据世界时从 Date 对象返回周中的一天 (0 ~ 6)。
	getUTCMonth()	根据世界时从 Date 对象返回月份 (0 ~ 11)。
	getUTCFullYear()	根据世界时从 Date 对象返回四位数的年份。
	getUTCHours()	根据世界时返回 Date 对象的小时 (0 ~ 23)。
	getUTCMinutes()	根据世界时返回 Date 对象的分钟 (0 ~ 59)。
	getUTCSeconds()	根据世界时返回 Date 对象的秒钟 (0 ~ 59)。
	getUTCMilliseconds()	根据世界时返回 Date 对象的毫秒(0 ~ 999)。
	parse()	返回1970年1月1日午夜到指定日期（字符串）的毫秒数。
	
### 6.2Math对象方法
	方法		描述
	abs(x)	返回数的绝对值。
	acos(x)	返回数的反余弦值。
	asin(x)	返回数的反正弦值。
	atan(x)	以介于 -PI/2 与 PI/2 弧度之间的数值来返回 x 的反正切值。
	atan2(y,x)	返回从 x 轴到点 (x,y) 的角度（介于 -PI/2 与 PI/2 弧度之间）。
	ceil(x)	对数进行上舍入。
	cos(x)	返回数的余弦。
	exp(x)	返回 e 的指数。
	floor(x)	对数进行下舍入。
	log(x)	返回数的自然对数（底为e）。
	max(x,y)	返回 x 和 y 中的最高值。
	min(x,y)	返回 x 和 y 中的最低值。
	pow(x,y)	返回 x 的 y 次幂。
	random()	返回 0 ~ 1 之间的随机数。
	round(x)	把数四舍五入为最接近的整数。
	sin(x)	返回数的正弦。
	sqrt(x)	返回数的平方根。
	tan(x)	返回角的正切。
	toSource()	返回该对象的源代码。
	valueOf()	返回 Math 对象的原始值。
###6.3Math对象
	Math.ceil()   天花板函数
              返回一个数字的整数部分。对该数字进行向上舍入。
    注意：该方法不会对数字进行四舍五入运算
	 Math.floor()  地板函数
	Math.max(x,y)
           返回x，y之间的最大值
	Math.min(x,y)	
	返回x，y之间的最小值

	 Math.random()  伪随机 
	 返回0~1之间的数值，范围[0,1)
	 Math.pow(x,y)
	返回x值的y次方
	 Math.round(x) 
	Round 本身会出错
	电脑存在舍入误差  2.999999999999999999999999   3.0
	1.多了  要么完全舍弃 要么完全算进去
	2.工程中 奇数位进偶数位不进
##7关系运算符
	无限元无限次方程组求值
	二元一次方程组
	X+y = 6
	x-y = 1
	x^2  + y^2 = ..
	线性代数  矩阵
	
	Js是弱类型语言    js解释执行，如果出错 停止进行
	Var  name= ‘zhangsan’
	Var  age = 20;
	Var   sex = true;
	
	Java, c是强类型语言  编译执行，如果有错，无法编译通过，更不用说执行
	String name = ‘zhangsan’
	Number   int  float  double  long  short  ….
	Int  age = 20 
	Boolean  sex = true;
	
	变量是容器
	Var name = ‘zhangsan ‘

	>	大于号
	<	小于号
	>= 	大于或等于
	<=  小于或等于
	== 	等于
	=== 全等于  首先对比类型，在对比值  在js中  比较一般使用 === 
	!=	不等于
	!== 不全等于

	关系运算符，得到的结果都是布尔值，也就是说得到的东西要么是true，要么是false

	注意，在JS中=符号只有一个意思！表示赋值！！
	如果想判断两个东西，是否相等，需要使用符号==
	
	不能用一个等号，来表示等于的关系：
	== 这个符号，还可以验证字符串是否相同：
	==等等不严谨，会将不同类型的东西，转为相同类型进行比较：
	全等于，就是三个等号===
	也就是说，==两个等号，不严谨，”5”和5是true； ===三个等号更为严谨，”5”和5是false。
	

	!= 就是==的反面；   !==就是===的反面
##8.逻辑运算符
###8.1
	逻辑运算符有三个：
	&& 与（且）
	||	或
	!	非
##9 If...Else 语句
	if 语句 - 只有当指定条件为 true 时，使用该语句来执行代码
	if...else 语句 - 当条件为 true 时执行代码，当条件为 false 时执行其他代码
	if...else if....else 语句 - 使用该语句来选择多个代码块之一来执行
	switch 语句 - 使用该语句来选择多个代码块之一来执行
   
	语法
	if (条件)
	 {
	   只有当条件为 true 时执行的代码
	 }
	
	if...else语句
	语法
	if (条件)
	 {
	 	当条件为 true 时执行的代码
	 }
		else
	 {
		当条件不为 true 时执行的代码
	 }


	If...else if...else 语句
	if (条件 1)
	{
		当条件 1 为 true 时执行的代码
	}
		else if (条件 2)
	{
		当条件 2 为 true 时执行的代码
	}
		else
	{
		当条件 1 和 条件 2 都不为 true 时执行的代码
	}

	
##10JavaScript Switch 语句
	语法
	switch(n)
	{
	case 1:
		执行代码块 1
		break;
	case 2:
		执行代码块 2
		break;
	default:
		n 与 case 1 和 case 2 不同时执行的代码
	}
	工作原理：首先设置表达式 n（通常是一个变量）。随后表达式的值会与结构中的每个 case 的值做比较。如果存在匹配，则与该 case 关联的代码块会被执行。请使用 break 来阻止代码自动地向下一个 case 运行。
##11For循环
	JavaScript 支持不同类型的循环：
	for - 循环代码块一定的次数
	for/in - 循环遍历对象的属性
	while - 当指定的条件为 true 时循环指定的代码块
	do/while - 同样当指定的条件为 true 时循环指定的代码块
	

	For循环语法
	for (语句 1; 语句 2; 语句 3)
	{
		被执行的代码块

	}

	语句 1 在循环（代码块）开始前执行
	语句 2 定义运行循环（代码块）的条件
	语句 3 在循环（代码块）已被执行之后执行
### For/In 循环
	JavaScript for/in 语句循环遍历对象的属性
	实例
	var person={fname:"John",lname:"Doe",age:25};

	for (x in person)
	{
	txt=txt + person[x];
	}
### While 循环
	While 循环会在指定条件为真时循环执行代码块。
###
	语法
	while (条件)
	{
		需要执行的代码
	}

	实例
	while (i<5)
	{
		x=x + "The number is " + i + "<br>";
		i++;
	}
###do/while 循环
	do/while 循环是 while 循环的变体。该循环会执行一次代码块，在检查条件是否为真之前，然后如果条件为真的话，就会重复这个循环
	
	语法
	
	do
	{
		需要执行的代码
	}
		while (条件);
### Break 和 Continue 语句
	break 语句用于跳出循环。
	continue 用于跳过循环中的一个迭代。

	break 语句可用于跳出循环。
	break 语句跳出循环后，会继续执行该循环之后的代码（如果有的话）：
	
	实例
	for (i=0;i<10;i++)
	{
	if (i==3)
    {
    break;
    }
	x=x + "The number is " + i + "<br>";
	}

	Continue 语句
	
	continue 语句中断循环中的迭代，如果出现了指定的条件，然后继续循环中的下一个迭代。

	