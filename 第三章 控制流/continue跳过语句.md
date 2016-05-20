# continue跳过语句
continue语句被用来告诉Python跳过当前循环块中的剩余语句，然后继续进行下一轮循环。

	输入
	while True:
		s = raw_input('Enter something : ')
		if s == 'quit':
			break
		if len(s) < 3:
			continue
		print 'Input is of sufficient length'
		# Do other kinds of processing here...
	
	输出
	Enter something : a
	Enter something : 12
	Enter something : abc
	Input is of sufficient length
	Enter something : quit
* 从用户处取得输入，仅仅当它们有至少3个字符长的时候才处理它们。所以使用内建的len函数来取得长度。如果长度小于3，将使用continue语句忽略块中的剩余的语句。否则，这个循环中的剩余语句将被执行，可以在这里做希望的任何处理。
* continue语句也可以在for循环中使用。