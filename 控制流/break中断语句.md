# break中断语句
break语句是用来 终止 循环语句的，即哪怕循环条件没有称为False或序列还没有被完全递归，也停止执行循环语句。

一个重要的注释是，如果你从for或while循环中 终止 ，任何对应的循环else块将不执行。

	输入
	while True:
		s = raw_input('Enter something : ')
		if s == 'quit':
			break
		print 'Length of the string is', len(s)
	print 'Done'

	输出
	Enter something : Programming is fun
	Length of the string is 18
	Enter something : When the work is done
	Length of the string is 21
	Enter something : if you wanna make your work also fun:
	Length of the string is 37
	Enter something : use Python!
	Length of the string is 12
	Enter something : quit
	Done
反复地取得用户地输入，然后打印每次输入地长度。提供了一个特别的条件来停止程序，即检验用户的输入是否是'quit'。通过 终止 循环到达程序结尾来停止程序。

输入字符串的长度通过内建的len函数取得。

记住，break语句也可以在for循环中使用。