# 列表list
列表是处理一组有序项目的数据结构，即可以在一个列表中存储一个序列的项目。在Python中，每个项目之间用逗号分割。  
列表中的项目应该包括在方括号中，这样Python就知道是在指明一个列表。一旦创建了一个列表，可以添加、删除或是搜索列表中的项目。由于可以增加或删除项目，所以列表是可变的数据类型，即这种类型是可以被改变的。

	输入
	# Filename: using_list.py

	# This is my shopping list
	shoplist = ['apple', 'mango', 'carrot', 'banana']
	print 'I have', len(shoplist),'items to purchase.'
	print 'These items are:', # Notice the comma at end of the line
	for item in shoplist:
		print item,
	print '\nI also have to buy rice.'
	shoplist.append('rice')
	print 'My shopping list is now', shoplist
	print 'I will sort my list now'
	shoplist.sort()
	print 'Sorted shopping list is', shoplist
	print 'The first item I will buy is', shoplist[0]
	olditem = shoplist[0]
	del shoplist[0]
	print 'I bought the', olditem
	print 'My shopping list is now', shoplist
	输出
	$ python using_list.py
	I have 4 items to purchase.
	These items are: apple mango carrot banana
	I also have to buy rice.
	My shopping list is now ['apple', 'mango', 'carrot', 'banana', 'rice']
	I will sort my list now
	Sorted shopping list is ['apple', 'banana', 'carrot', 'mango', 'rice']
	The first item I will buy is apple
	I bought the apple
	My shopping list is now ['banana', 'carrot', 'mango', 'rice']
变量shoplist是列表。在shoplist中，只存储购买的东西的名字字符串，但是记住，可以在列表中添加任何种类的对象 包括数甚至其他列表。  
使用了for..in循环在列表中各项目间递归。列表也是一个序列。  
注意，在print语句的结尾使用了一个逗号来消除每个print语句自动打印的换行符。这样
做有点难看，不过确实简单有效。  
接下来，使用append方法在列表中添加了一个项目，然后通过打印列表的内容来检验这个项目是否确实被添加进列表了。打印列表只需简单地把列表传递给print语句，就可以得到一个整洁的输出。  
再接下来，使用列表的sort方法来对列表排序。需要理解的是，这个方法影响列表本身，而不是返回一个修改后的列表，这与字符串工作的方法不同。即列表是可变的而字符串是不可变的。  
最后，指出想要删除列表中的哪个项目，而del语句为从列表中删除它。指明想要删除列表中的第一个元素，因此使用del shoplist[0]（记住，Python从0开始计数）。  
如果想要知道列表对象定义的所有方法，可以通过help(list)获得完整的知识。