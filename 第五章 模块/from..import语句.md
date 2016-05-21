# from..import语句
如果想要直接输入argv变量到程序中（避免在每次使用它时打sys.），那么可以使用from sys import argv语句。如果想要输入所有sys模块使用的名字，那么可以使用from sysimport *语句，这对于所有模块都适用。  
但是一般说来，应该避免使用from..import而使用import语句，因为这样可以使程序更加易读，也可以避免名称的冲突。