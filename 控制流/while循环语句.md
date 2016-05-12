# while语句
只要在一个条件为真的情况下，while语句允许你重复执行一块语句。while语句是所谓 循环 语句的一个例子。while语句有一个可选的else从句。

	输入
	number = 23
	running = True
	while running:
	guess = int(raw_input('Enter an integer : '))
	if guess == number:
	print 'Congratulations, you guessed it.'
	running = False # this causes the while loop to stop
	elif guess < number:
	print 'No, it is a little higher than that'
	else:
	print 'No, it is a little lower than that'
	else:
	print 'The while loop is over.'
	# Do anything else you want to do here
	print 'Done'

	输出
	Enter an integer : 50
	No, it is a little lower than that.
	Enter an integer : 22
	No, it is a little higher than that.
	Enter an integer : 23
	Congratulations, you guessed it.
	The while loop is over.
	Done
把raw_input和if语句移到了while循环内，并且在while循环开始前把running变量设置为True。首先，我们检验变量running是否为True，然后执行后面的 while-块 。在执行了这块程序之后，再次检验条件，在这个例子中，条件是running变量。如果它是真的，我们再次执行while-块，否则，我们继续执行可选的else-块，并接着执行下一个语句。当while循环条件变为False的时候，else块才被执行——这甚至也可能是在条件第一次被检验的时候。如果while循环有一个else从句，它将始终被执行，除非你的while循环将永远循环下去不会结束！  
True和False被称为布尔类型。你可以分别把它们等效地理解为值1和0。在检验重要条件的时候，布尔类型十分重要，它们并不是真实的值1。  
else块事实上是多余的，因为你可以把其中的语句放在同一块（与while相同）中，跟在while语
句之后，这样可以取得相同的效果。