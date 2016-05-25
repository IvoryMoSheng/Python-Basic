# try..finally
假如在读一个文件的时候，希望在无论异常发生与否的情况下都关闭文件，可以使用finally块来完成。
注意，在一个try块下，可以同时使用except从句和finally块。如果要同时使用它们的话，需要把一个嵌入另外一个。

	输入
	# Filename: finally.py
	import time
	try:
	f = file('poem.txt')
	while True: # our usual file-reading idiom
	line = f.readline()
	if len(line) == 0:
	break
	time.sleep(2)
	print line,
	finally:
	f.close()
	print 'Cleaning up...closed the file'
	输出
	$ python finally.py
	Programming is fun
	When the work is done
	Cleaning up...closed the file
	Traceback (most recent call last):
	File "finally.py", line 12, in ?
	time.sleep(2)
	KeyboardInterrupt
进行通常的读文件工作，但是有意在每打印一行之前用time.sleep方法暂停2秒钟。这样做的原因是让程序运行得慢一些（Python由于其本质通常运行得很快）。
在程序运行的时候，按Ctrl-c中断/取消程序。可以观察到KeyboardInterrupt异常被触发，程序退出。但是在程序退出之前，finally从句仍然被执行，把文件关闭。