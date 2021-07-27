```python

bin()    # 十进制数转八进制
hex()    # 十进制数转十六进制
range()    # 函数：可以生成一个整数序列
type()    # 查看数据类型
len()    # 计算字符串长度
format()    # 格式化字符串，类似%s，传递值能多不能少

# 数学运算
abs：求数值的绝对值
abs(-2)
 
divmod：返回两个数值的商和余数
divmod(5,2)
divmod(5.5,2)
 
max：返回迭代对象中的元素的最大值或者所有参数的最大值
max(1,2,3)   # 传入3个参数 取3个中较大者
max('1234')   # 传入1个可迭代对象，取其最大元素值
max(-1,0,key=abs)   # 传入了求绝对值函数，则参数都会进行求绝对值后再取较大者
 
min：返回可迭代对象中的元素的最小值或者所有参数的最小值
min(1,2,3)　　# 传入3个参数 取3个中较小者
min('1234')   # 传入1个可迭代对象，取其最小元素值
min(-1,-2,key=abs)   # 传入了求绝对值函数，则参数都会进行求绝对值后再取较小者
 
pow：返回两个数值的幂运算值或其余指定整数的模值
pow(2,3)
 
round：对浮点数进行四舍五入求值
round(1.1111,1)
 
sum：对元素类型是数值的可迭代对象中的每个元素求和
sum((1,2,3,4))   # 传入可迭代对象、元素类型必须是数值型

#类型转换

bool：根据传入的参数的逻辑值创建一个新的布尔值
bool()或bool(0)    # 数值0、空值为False
 
int：根据传入的参数创建一个新的整数
int()    # 不传入参数时，得到结果0
 
float：根据传入的参数创建一个新的浮点数
float()   # 不提供参数的时候，返回0.0
 
complex：根据传入参数创建一个新的复数
complex()   # 当两个参数都不提供时，返回复数 0j
 
str：返回一个对象的字符串表现形式(给用户)


bytearray：根据传入的参数创建一个新的字节数组
bytearray('中文','utf-8') 
bytearray(b'\xe4\xb8\xad\xe6\x96\x87')
 
bytes：根据传入的参数创建一个新的不可变字节数组
bytes('中文','utf-8')
b'\xe4\xb8\xad\xe6\x96\x87'
 
memoryview：根据传入的参数创建一个新的内存查看对象
v=memoryview(b'asdf')
print(v[0])   # 97
print(v[-1])   # 102
 
ord：返回Unicode字符对应的整数
print(ord('a'))
 
chr：返回整数所对应的Unicode字符
print(chr(97))
 
bin：将整数转换成2进制字符串
oct：将整数转化成8进制数字符串
hex：将整数转换成16进制字符串
 
tuple：根据传入的参数创建一个新的元组
list：根据传入的参数创建一个新的列表
dict：根据传入的参数创建一个新的字典
set：根据传入的参数创建一个新的集合
 
frozenset：根据传入的参数创建一个新的不可变集合
a=frozenset(range(10))
print(a)
# frozenset({0, 1, 2, 3, 4, 5, 6, 7, 8, 9})
 
enumerate：根据可迭代对象创建枚举对象
l1=['one','two','three','five']
print(list(enumerate(l1)))
# [(0, 'one'), (1, 'two'), (2, 'three'), (3, 'five')]
print(list(enumerate(l1,start=1))) # 指定起始值
# [(1, 'one'), (2, 'two'), (3, 'three'), (4, 'five')]
 
range：根据传入的参数创建一个新的range对象
iter：根据传入的参数创建一个新的可迭代对象
a=iter('asdf')
print(a)   # <str_iterator object at 0x00000190B4D99668>
print(next(a)) # a
print(next(a)) # s
print(next(a)) # d
print(next(a)) # f
print(next(a)) # 报错StopIteration
 
slice：根据传入的参数创建一个新的切片对象
c1=slice(5)
print(c1)  # slice(None, 5, None)
c1=slice(2,5)
print(c1)  # slice(2, 5, None)
c1=slice(1,4,7)
print(c1)  # slice(1, 4, 7)
 
super：根据传入的参数创建一个新的子类和父类关系的代理对象
# 定义父类A类
class A(object):
    def __init__(self):
        print(A.__init__)
 
# 定义子类，继承A
class B(A):
    def __init__(self):
        print(B.__init__)
        super().__init__()
 
# super调用父类方法
b=B()
print(b)
<function B.__init__ at0x0000023DB0CA76A8>
<function A.__init__ at0x0000023DB0CA7620>
 
object：创建一个新的object对象


# 序列操作
all：判断可迭代对象的每个元素是否都为True值
print(all([1,2]))   # 列表中每个元素逻辑值均为True，返回True
print(all([0,2]))    # 列表中0的逻辑值为False，返回False
 
any：判断可迭代对象的元素是否有为True值的元素
# 列表元素有一个为True，则返回True
# 列表元素全部为False，则返回False
 
filter：使用指定方法过滤可迭代对象的元素
 
map：使用指定方法去作用传入的每个可迭代对象的元素，生成新的可迭代对象
 
next：返回可迭代对象中的下一个元素值
# 传入default参数后，如果可迭代对象还有元素没有返回，则依次返回其元素值，如果所有元素已经返回，则返回default指定的默认值而不抛出StopIteration 异常
  
reversed：反转序列生成新的可迭代对象
 
sorted：对可迭代对象进行排序，返回一个新的列表
 
zip：聚合传入的每个迭代器中相同位置的元素，返回一个新的元组类型迭代器

# 对象操作
help：返回对象的帮助信息
dir：返回对象或者当前作用域内的属性列表
id：返回对象的唯一标识符
hash：获取对象的哈希值
type：返回对象的类型，或者根据传入的参数创建一个新的类型
len：返回对象的长度
ascii：返回对象的可打印表字符串表现方式
format：格式化显示值
 
vars：返回当前作用域内的局部变量和其值组成的字典，或者返回对象的属性列表
class A(object):
    pass
 
a=A()
print(a.__dict__)  # {}
print(vars(a))     # {}
a.name='buer'
print(a.__dict__)  # {'name': 'buer'}
print(vars(a))     # {'name': 'buer'}



#反射操作
__import__：动态导入模块
print(__import__('os'))
print(__import__('time'))
 
# <module 'os' from 'D:\\Python36\\lib\\os.py'>
# <module 'time' (built-in)>
 
isinstance：判断对象是否是类或者类型元组中任意类元素的实例
issubclass：判断类是否是另外一个类或者类型元组中任意类元素的子类
 
hasattr：检查对象是否含有属性
class Student:
    def __init__(self,name):
        self.name=name
 
s=Student('Ethan')
print(hasattr(s,'name'))   # 含有name属性为True
print(hasattr(s,'age'))    # 不含有age属性为False
 
getattr：获取对象的属性值
print(getattr(s,'name'))   # 存在属性name，Ethan
print(getattr(s,'age',20)) # 不存在属性age，但提供了默认值，返回默认值
print(getattr(s,'age'))    # 不存在属性age，未提供默认值，调用报错
报错如下：
Traceback (most recent call last):
  File "D:/test.py", line30,in <module>
    print(getattr(s,'age'))
AttributeError:'Student' object has no attribute'age'
 
setattr：设置对象的属性值
print(s.name)  # Ethan
setattr(s,'name','Tom')  # name属性存在，做赋值操作
setattr(s,'age',18)    # age属性不存在，创建这个属性
print(s.name)  # Tom
print(s.age)   # 18
 
delattr：删除对象的属性
class Student:
    def __init__(self,name):
        self.name=name
    def foo(self):
        print('hello %s' % self.name)
 
a=Student('Ethan')
 
print(a.name)  # Ethan
print(a.foo()) # hello Ethan
 
print(delattr(a,'name'))   # name属性被删除
print(a.name)  # 调用报错
Traceback (most recent call last):
  File "D:/test.py", line50,in <module>
    print(a.name)  # 调用报错
AttributeError:'Student' object has no attribute'name'
 
callable：检测对象是否可被调用
class B:
    def __call__(self,*args,**kwargs):
        print('instances are callable now')
 
print(callable(B)) # 类B是可调用对象
b=B()  # 调用类B
print(callable(b)) # 实例b是可调用对象
print(b()) # 调用实例b成功
# instances are callable now



# 变量操作
globals：返回当前作用域内的全局变量和其值组成的字典
locals：返回当前作用域内的局部变量和其值组成的字典



#交互操作
print：向标准输出对象打印输出
input：读取用户输入值
user=input('please input your name:')



#文件操作
open：使用指定的模式和编码打开文件，返回文件读写对象
# 写入文件
a= open('a.text','w')
a.write('124sdgadgahg ggadh')
 
# 读取文件
a= open('a.text','rt')
print(a.read())
a.close()


# 编译执行
compile：将字符串编译为代码或者AST对象，使之能够通过exec语句来执行或者eval进行求值
# 流程语句使用exec
code1='for i in range(5):print(i)'
compile1=compile(code1,'','exec')
exec (compile1)
# 0
# 1
# 2
# 3
# 4
 
# 简单求值表达式用eval
code2='1+2+3+4'
compile2=compile(code2,'','eval')
print(eval(compile2))  # 10
 
eval：执行动态表达式求值
print(eval('1+2+3+4')) # 10
print(eval('2*2*2'))   # 8
print(eval('10/2+2*2'))# 9.0
 
exec：执行动态语句块
exec ('a=1+2')
print(a)   # 3
exec ('b=4*3/2-1')
print(b)   # 5.0
 
repr：返回一个对象的字符串表现形式(给解释器)
a='hello world'
print(str(a))  # hello world
print(repr(a)) # 'hello world'


#装饰器
property：标示属性的装饰器
class A:
    def __init__(self):
        pass
    @property
    def foo(self):
        print('1111111111')
a=A()
print(a.foo)   # 访问属性，不需要加()执行foo
 
classmethod：标示方法为类方法的装饰器
class B(object):
    def __init__(self):
        pass
 
    @classmethod
    def foo(cls):
        print(cls)
         
print(B.foo()) # 类对象调用类方法
# <class '__main__.B'>
b=B()
print(b.foo()) # 类实例对象调用类方法
# <class '__main__.B'>
 
staticmethod：标示方法为静态方法的装饰器
class C(object):
    def __init__(self):
        pass
    @staticmethod
    def f1():
        print('hahahha')
         
print(C.f1())  # 类调用
c=C()
print(c.f1())  # 类实例对象调用
```

