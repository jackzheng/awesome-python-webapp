学习 python 教程！

真的

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
    
    
	
	 





