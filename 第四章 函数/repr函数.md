# repr函数
repr函数用来取得对象的规范字符串表示，反引号（转换符）可以完成相同的功能。  
注意，在多数时候有eval(repr(object))==object

	输入
	i=[]
	i.append('item')
	`i`
	
	repr(i)
	输出
	"['item']"
	
	"['item']"
基本上，repr函数和反引号用来获取对象的可打印的表示形式。可以通过定义类的__repr__方法来控制对象在被repr函数调用的时候返回的内容。