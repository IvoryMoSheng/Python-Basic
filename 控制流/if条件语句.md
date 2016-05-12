# if语句
if语句用来检验一个条件， 如果条件为真，我们运行一块语句（称为 if-块），否则处理另外一块语句（称为 else-块）。else从句是可选的。


	输入
	number = 23
	guess = int(raw_input('Enter an integer : '))
	if guess == number:
	  print 'Congratulations, you guessed it.' # New block starts here
	  print "(but you do not win any prizes!)" # New block ends here
	elif guess < number:
	  print 'No, it is a little higher than that' # Another block
	# You can do whatever you want in a block ...
	else:
	  print 'No, it is a little lower than that'
	# you must have guess > number to reach here
	print 'Done'
	# This last statement is always executed, after the if statement is executed

    输出
	Enter an integer : 50
	No, it is a little lower than that
	Done
	$ python if.py
	Enter an integer : 22
	No, it is a little higher than that
	Done
	$ python if.py
	Enter an integer : 23
	Congratulations, you guessed it.
	(but you do not win any prizes!)
	Done
使用了缩进层次来告诉Python每个语句分别属于哪一个块，坚持“每个缩进层一个制表符”  
注意if语句在结尾处包含一个冒号——通过它告诉Python下面跟着一个语句块  
把if else-if else合并为if-elif-else  
可以在一个if块中使用另外一个if语句，等等——这被称为嵌套的if语句  
elif和else部分是可选的
  
	if True:
	print 'Yes, it is true'
在Python执行完一个完整的if语句以及与它相关联的elif和else从句之后，它移向if语句块的下一个语句。在这个例子中，if这个语句块是主块。程序从主块开始执行，而下一个语句是print'Done'语句。在这之后，Python看到程序的结尾，简单的结束运行. 