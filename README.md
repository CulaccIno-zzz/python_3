# python_3
字符串
	在python中可以用一对双引号或者一对单引号定义字符串。
	循环遍历：
		str1 = 我是谁
		for h in str1：
			print（h）
		结果为 我
			   是
			   谁
	
	统计字符串的长度 ：    len （字符串）
	统计某一个小字符串出现的次数 ：字符串 . count（需要统计的字符串）
	某一个子字符串在字符串中的位置 ：字符串 . index（子字符串）
	判断类型
		is：
			String.isspace（）     如果string中包含空格或者空白字符，则返回true
			String.isalnum（）    如果string中至少有一个字符并且所有字符都是字母或数字，返回true
			String.isalpha（）     如果string中至少有一个字符并且所有字符都是字母，返回trur
			
			String.isdeciaml（）  如果string中只包含数字返回true，全角数字。
			String.isdigit（）        如果string中只包含数字返回true，全角数字，（1），\u00b2
			String.isnumeric（）   如果string中只包含数字返回true，全角数字，汉字数字
				都不能判断小数
				
			String.istitle（）         如果string是标题化的（每个单词首字母大写）则返回true
			String.islower（）      如果string中包含至少一个区分大小写的字符，并且所有这些（区分大                小写）字符都是小写，则返回true
			String.isupper（）     如果string中至少包含一个区分大小写的字符，并且所有这些（区分大小写）字符都是大写，则返回true
			
	查找和替换
			string.startswith(str)    检查字符串是否是以 str开头，是则返回True
			string.endswith(str)     检查字符串是否是以str结束，是则返回True
			string.find(str, start=0,end=len(string))  检测str是否包含在string 中，如果start和end指定范围，则检查是否包含在指定范围内，如果是返回开始的索引值，否则返回-1
			string.rfind(str, start=0,end=len(string))     类似于find0函数，不过是从右边开始查找
			string.index(str,start=0,end=len(string))      跟find0方法类似，只不过如果str不在string 会报错
			string.rindex(str,start=0,end=len(string))       类似于index（） 不过是从右边开始
			string.replace(old _str,new_str,num)     把string中的old. _str替换成new _str,如果num指定，则替换不超过num次，replace方法执行完后，会返回一个新的字符串，原有的字符串不会被修改
	大小写转换
			string.capitalize() | 把字符串的第一个字符大写 
			string.title() | 把字符串的每个单词首字母大写 
			string.lower() | 转换 string 中所有大写字符为小写 
			string.upper() | 转换 string 中的小写字母为大写 
			string.swapcase() | 翻转 string 中的大小写 
	文本对齐
			| string.ljust(width，方式) | 返回一个原字符串左对齐，并使用空格填充至长度 width 的新字符串，不规定方式，则默认用英文空格填充 |
			| string.rjust(width，方式) | 返回一个原字符串右对齐，并使用空格填充至长度 width 的新字符串 ，不规定方式，则默认用英文空格填充下·|
			| string.center(width，方式) | 返回一个原字符串居中，并使用空格填充至长度 width 的新字符串 ，不规定方式，则默认用英文空格填充|
	去除空白字符
			| string.lstrip() | 截掉 string 左边（开始）的空白字符 |
			| string.rstrip() | 截掉 string 右边（末尾）的空白字符 |
			| string.strip() | 截掉 string 左右两边的空白字符 |
	拆分和连接
			| string.partition(str) | 把字符串 string 分成一个 3 元素的元组 (str前面, str, str后面) |
			| string.rpartition(str) | 类似于 partition() 方法，不过是从右边开始查找 |
			| string.split(str="", num) | 以 str 为分隔符拆分 string，如果 num 有指定值，则仅分隔 num + 1 个子字符串，str 默认包含 '\r', '\t', '\n' 和空格 |
			| string.splitlines() | 按照行('\r', '\n', '\r\n')分隔，返回一个包含各行作为元素的列表 |
			| string.join(seq) | 以 string 作为分隔符，将 seq 中所有的元素（的字符串表示）合并为一个新的字符串 |
	字符串的切片
			切片是用索引值来限定范围，从一个大的字符串中切出小的字符串。
			列表和元组都是有序的集合，都能够通过索引值获取到对应的数据。
			字典是一个无序的集合，是使用键值对保存数据的。
		语法
			字符串【开始索引：结束索引：步长】     不包含结束索引的内容，如果步长为负数，则是倒着切。
			顺序 从左到右 0到正无穷
			逆序 从右到左 由-1开始递减，正数和负数是等价的，可以互换。
		
公共方法
	内置函数
		len（item）     计算容器中元素个数
		del（item）     删除变量
		max（item）   返回容器中元素最大值     如果是字典，只对key比较（键）
		min（item）   返回容器中元素最小值      如果是字典，只对key比较（键）
		cmp（item1，item2）  比较两个值，-1小于，0相等，1大于   python3.x取消了该函数
	运算符
		+   【1，2】+【3，4】  结果为【1，2，3，4】  支持数据类型：字符串，列表，元组
		*  【“HI”】*4         结果为【“HI”“HI”“HI”“HI”】   支持数据类型：字符串，列表，元组
		In    3in（1，2，3）  结果为true    元素是否存在  支持数据类型： 字符串，列表，元组，字典
			对字典操作的时候，判断的是字典的键（key）
		Not in   4 not in（1，2，3） 结果为ture   元素是否不存在  支持数据类型：字符串，列表，元组，字典
			对字典操作的时候，判断的是字典的键（key）
			In      not in被称为成员运算符
		>  >=    ==    <   <=          支持数据类型：字符串，列表，元组
for循环
	for 变量 in 集合：
		循环体代码
	else
		如果使用通过break退出循环，则不会执行else里的代码。
	
