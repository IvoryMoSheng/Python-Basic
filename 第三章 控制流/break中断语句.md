# break中断语句
break语句是用来终止循环语句的，即哪怕循环条件没有称为False或序列还没有被完全递归，也停止执行循环语句。

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
* 反复地取得用户地输入，然后打印每次输入的长度。提供了一个特别的条件来停止程序，即检验用户的输入是否是'quit'。通过终止循环到达程序结尾来停止程序。
* 输入字符串的长度通过内建的len函数取得。
* break语句也可以在for循环中使用。

Tip:

1.如果从for或while循环中终止 ，任何对应的循环else块将不执行。

```
	输入
	for i in range(5):
		if i = 2:
			break
		print(i)
	else:
		print('Done')
	输出
	0
	1
```

2.循环所迭代的序列是空的，else分支依然会被执行，因为循环仍然是正常完成的。

```
输入
for i in []:
	print(i)
else:
	print('Done')
输出
Done
```
3.else语句在循环中常用来实现循环查找，例如在查找一个满足特定条件的项目(item)，同时需要进行附加处理（或者在未发现可接受的值时生成一个错误）
```
for x in data:
	if meets_condition(x):
		break
else:
  # raise error or do additional processing
```
如果没有else语句的话，需要设置一个标志，然后在后面对其检测，以此确定是否存在满足条件的值。
```
condition_is_met = False
for x in data:
	if meets_condition(x):
		condition_is_met = True
if not condition_is_met:
	# raise error or do additional processing