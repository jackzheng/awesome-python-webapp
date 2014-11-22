#学习 python 教程！

## 学python目的就是能利用各种web api，比如豆瓣 https://github.com/qiuxiang/pydoubanfm


2014-11-20 
关于语法部分已经看了一遍，但是在实战的时候 感觉看的太粗了，重看一次！

结合开源的代码一起看，

11-21

#####数据类型 list tuple 

- list 是有序集合 方法 append insert pop 
- tuple元组 一旦确定就不能更改

#####循环

for x in [1,2,3,4]
while n > 0


#####数据类型 dict set

- dict 和js 中的对象一样 key-value dict的key必须是不可变对象。
- set和dict类似，也是一组key的集合，但不存储value。由于key不能重复，所以，在set中，没有重复的key。


#####函数 ：

def my_abc(x):

#####参数

1. 默认参数功能
2. 可变参数 def calc(*numbers):
3. *args是可变参数，args接收的是一个tuple； **kw是关键字参数，kw接收的是一个dict。

#####函数高级特性

1. 切片 L[0:3]
2. 迭代
3. generator 生成器 有点难理解 【待看】


####函数式编程

#####高阶函数 像map()函数这种能够接收函数作为参数的函数，称之为高阶函数

1. map()函数接收两个参数，一个是函数，一个是序列，map将传入的函数依次作用到序列的每个元素，并把结果作为新的list返回。
2. reduce() reduce把一个函数作用在一个序列[x1, x2, x3...]上，这个函数必须接收两个参数，reduce把结果继续和序列的下一个元素做累积计算，
3. 匿名函数 lambda x: x * x （支持有限 不赞成大用）
4. 装饰器 decorator就是一个返回函数的高阶函数。所以，我们要定义一个能打印日志的decorator，
	- now.__name__ 可以拿到函数的名
	def log(func):
    def wrapper(*args, **kw):
        print 'call %s():' % func.__name__
        return func(*args, **kw)
    return wrapper
    
    装饰器这块还是不懂
    
5. 偏函数int2 = functools.partial(int, base=2)
6. 模块 每一个包目录下面都会有一个__init__.py的文件，这个文件是必须存在的，否则，Python就把这个目录当成普通目录，而不是一个包。__init__.py可以是空文件，也可以有Python代码，因为__init__.py本身就是一个模块，而它的模块名就是mycompany。
7. 使用模块 导入模块
	' a test module '

	__author__ = 'Michael Liao'

	import sys

	def test():
    args = sys.argv
    if len(args)==1:
        print 'Hello, world!'
    elif len(args)==2:
        print 'Hello, %s!' % args[1]
    else:
        print 'Too many arguments!'

	if __name__=='__main__':
    	test()


 
 
 
###面向对象

> 如果采用面向对象的程序设计思想，我们首选思考的不是程序的执行流程，而是Student这种数据类型应该被视为一个对象，这个对象拥有name和score这两个属性（Property）。如果要打印一个学生的成绩，首先必须创建出这个学生对应的对象，然后，给对象发一个print_score消息，让对象自己把自己的数据打印出来 

	class Student(object):

    def __init__(self, name, score):
        self.name = name
        self.score = score

    def print_score(self):
        print '%s: %s' % (self.name,self.score)
        
        
        
        
####类和实例
面向对象最重要的概念就是类（Class）和实例（Instance），必须牢记类是抽象的模板，比如Student类，而实例是根据类创建出来的一个个具体的“对象”，每个对象都拥有相同的方法，但各自的数据可能不同。

	class Student(object):

    def __init__(self, name, score):
        self.name = name
        self.score = score

注意到__init__方法的第一个参数永远是self，表示创建的实例本身，因此，在__init__方法内部，就可以把各种属性绑定到self，因为self就指向创建的实例本身。

有了__init__方法，在创建实例的时候，就不能传入空的参数了，必须传入与__init__方法匹配的参数，但self不需要传，Python解释器自己会把实例变量传进去：

#### 访问限制

如果要让内部属性不被外部访问，可以把属性的名称前加上两个下划线__，在Python中，实例的变量名如果以__开头，就变成了一个私有变量（private），只有内部可以访问，外部不能访问，所以，我们把Student类改一改：

	class Student(object):

    def __init__(self, name, score):
        self.__name = name
        self.__score = score

    def print_score(self):
        print '%s: %s' % (self.__name,self.__score)


##### 继承 多态
在OOP程序设计中，当我们定义一个class的时候，可以从某个现有的class继承，新的class称为子类（Subclass），而被继承的class称为基类、父类或超类（Base class、Super class）。

> 多态部分 需要在实例中理解


#### 获取对象信息
1. type()
2. isinstance()
3. dir() 如果要获得一个对象的所有属性和方法，可以使用dir()函数，它返回一个包含字符串的list，


####使用@property









    
	
	 





