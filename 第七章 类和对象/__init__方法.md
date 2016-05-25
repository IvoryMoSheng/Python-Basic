# __init__方法
__init__方法在类的一个对象被建立时马上运行。这个方法可以用来对对象做一些希望的初始化.注意，这个名称的开始和结尾都是双下划线。

	输入
	#Filename:class_init.py
	class Person:
		def __init__(self,name):
			self.name = name
		def sayHi(self):
			print 'my name is',self.name
	p = Person('Mosheng')
	p.sayHi()
	# This short example can also be written as Person('Swaroop').sayHi()
	输出
	$ python class_init.py
	my name is Mosheng
把__init__方法定义为取一个参数name（以及普通的参数self）。在这个__init__里，只是创建一个新的域，也称为name。注意它们是两个不同的变量，尽管它们有相同的名字。点号能够区分它们。  
最重要的是，没有专门调用__init__方法，只是在创建一个类的新实例的时候，把参数包括在圆括号内跟在类名后面，从而传递给__init__方法。这是这种方法的重要之处。  
之后则能够在方法中使用self.name域。这在sayHi方法中得到了验证。

tips:
1. __init__方法类似于C++、C#和Java中的 constructor