# exec和eval语句
exec语句用来执行储存在字符串或文件中的Python语句。例如，可以在运行时生成一个包含Python代码的字符串，然后使用exec语句执行这些语句。下面是一个简单的例子。
	
	输入
	exec 'print "Hello World"'
	输出
	Hello World
eval语句用来计算存储在字符串中的有效Python表达式。下面是一个简单的例子。

	输入
	eval('2*3')
	输出
	6