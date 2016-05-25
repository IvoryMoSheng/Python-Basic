# self
类的方法与普通的函数只有一个特别的区别,它们必须有一个额外的第一个参数名称，但是在调用这个方法的时候,不用为这个参数赋值，Python会提供这个值。这个特别的变量指对象本身，按照惯例它的名称是self。

虽然可以给这个参数任何名称，但是强烈建议使用self这个名称，其他名称都是不赞成使用的。

self的原理  
有一个MyClass类和这个类的一个实例MyObject。当调用这个对象的方法MyObject.method(arg1, arg2)的时候，这会由Python自动转为MyClass.method(MyObject, arg1,arg2)

如果有一个不需要参数的方法，还是得给这个方法定义一个self参数。

tips:

1. Python中的self等价于C++中的self指针和Java、C#中的this.