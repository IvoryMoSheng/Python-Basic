# return语句
return语句用来从一个函数返回，即跳出函数。也可选从函数返回一个值。

	输入
	def maximum(x, y):
		if x > y:
			return x
		else:
			return y
	print maximum(2, 3)
	输出
	3
maximum函数返回参数中的最大值，在这里是提供给函数的数。它使用简单的if..else语句来找
出较大的值，然后返回那个值。
  
注意，没有返回值的return语句等价于return None。None是Python中表示没有任何东西的特殊类型。例如，如果一个变量的值为None，可以表示它没有值。
  
除非提供自己的return语句，每个函数都在结尾暗含有return None语句。通过运行下面的程序，可以明白这一点。

	输入
	def someFunction():
		pass
	print someFunction()
函数someFunction没有使用return语句，其中pass语句在Python中表示一个空的语句块。