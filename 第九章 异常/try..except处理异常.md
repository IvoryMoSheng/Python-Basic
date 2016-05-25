# try..except处理异常
尝试读取用户的一段输入。按Ctrl-d

	>>> s = raw_input('Enter something --> ')
	Enter something --> Traceback (most recent call last):
	File "<stdin>", line 1, in ?
	EOFError
Python引发了一个称为EOFError的错误，这个错误基本上意味着它发现一个不期望的文件尾（由Ctrl-d表示）。
可以使用try..except语句来处理异常。把通常的语句放在try-块中，而把错误处理语句放在except-块中。
	
	输入
	# Filename: try_except.py
	import sys
	try:
	s = raw_input('Enter something --> ')
	except EOFError:
	print '\nWhy did you do an EOF on me?'
	sys.exit() # exit the program
	except:
	print '\nSome error/exception occurred.'
	# here, we are not exiting the program
	print 'Done'
	输出
	$ python try_except.py
	Enter something -->
	Why did you do an EOF on me?
	$ python try_except.py
	Enter something --> Python is exceptional!
	Done
把所有可能引发错误的语句放在try块中，然后在except从句/块中处理所有的错误和异常。except从句可以专门处理单一的错误或异常，或者一组包括在圆括号内的错误/异常。如果没有给出错误或异常的名称，它会处理所有的错误和异常。
对于每个try从句，至少都有一个相关联的except从句。  
如果某个错误或异常没有被处理，默认的Python处理器就会被调用。它会终止程序的运行，并且打印一个消息。
可以让try..excpet块关联上一个else从句。当没有异常发生的时候，else从句将被执行。