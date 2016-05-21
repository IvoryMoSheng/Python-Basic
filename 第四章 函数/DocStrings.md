# DocStrings
Python有一个很奇妙的特性，称为文档字符串，它通常被简称为docstrings 。DocStrings是一个重要的工具，由于它帮助程序文档更加简单易懂，应该尽量使用它。甚至可以在程序运行的时候，从函数恢复文档字符串！

	输入
	def printMax(x, y):
		'''Prints the maximum of two numbers.

		The two values must be integers.'''
		x = int(x) # convert to integers, if possible
		y = int(y)
		if x > y:
			print x, 'is maximum'
		else:
			print y, 'is maximum'
	printMax(3, 5)
	print printMax.__doc__
	输出
	5 is maximum
	Prints the maximum of two numbers.

	The two values must be integers.
* 在函数的第一个逻辑行的字符串是这个函数的文档字符串。
* 注意，DocStrings也适用于模块和类。
* 文档字符串的惯例是一个多行字符串，它的首行以大写字母开始，句号结尾。第二行是空行，从第三行开始是详细的描述。 强烈建议在函数中使用文档字符串时遵循这个惯例。
* 可以使用__doc__（注意双下划线）调用printMax函数的文档字符串属性（属于函数的名称）。请记住Python把每一样东西都作为对象，包括这个函数。
* 如果已经在Python中使用过help()，那么已经看到过DocStings的使用了！它所做的只是抓取函数的__doc__属性，然后整洁地展示出来。可以对上面这个函数尝试一下，只是在程序中包括help(printMax)。记住按q退出help。
* 自动化工具也可以以同样的方式从你的程序中提取文档。因此，强烈建议对所写的任何正式函数编写文档字符串。随Python发行版附带的pydoc命令，与help()类似地使用DocStrings。