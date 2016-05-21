# 模块的__name__
每个模块都有一个名称，在模块中可以通过语句来找出模块的名称。  
这在一个场合特别有用，就如前面所提到的，当一个模块被第一次输入的时候，这个模块的主块将被运行。假如只想在程序本身被使用的时候运行主块，而在它被别的模块输入的时候不运行主块，这可以通过模块的__name__属性完成。
	
	输入
	# Filename: using_name.py
	if __name__ == '__main__':
		print 'This program is being run by itself'
	else:
		print 'I am being imported from another module'
	输出
	$ python using_name.py
	This program is being run by itself
	$ python
	>>> import using_name
	I am being imported from another module
	>>>
每个Python模块都有它的__name__，如果它是'__main__'，这说明这个模块被用户单独运行，可以进行相应的恰当操作。