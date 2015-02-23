generator(生成器）的好处是：
占用CPU、内存资源小，速度快

1,generator只能用一次
2,含有yield的函数是generator；
3,在python2.x中，xrange()是generator，range()是list（列表)
4,例如:x=(a for a in range(10)),x是generator




yield

含有yield的函数是generator（生成器），当执行此函数时，执行到yield时，返回一个值，继续执行。直到所有值生成。
如果用generator.next()(或者next(generator()))的方法，当遇到yield时，返回一个值，然后函数挂起。再执行generator.next()，函数从前一次挂起的位置继续执行，直到抛出错误，此时需要generator.close()结束函数。


下面这个generator的例子中，用next(gensquares(11))的结果是一直是0，原因是gensquares(11)调用一次他就重新生成一次，所以永远都是第一次。这时需要将这个生成器对象赋值给一个变量g，用next(g)来调用生成器。
>>> def gensquares(n):
...     i=0
...     while i<= n:
...             yield i*i
...             i += 1
... 
>>> gensquares
<function gensquares at 0x7f46db422b18>
>>> gensquares(11)
<generator object gensquares at 0x7f46db410aa0>
>>> next(gensquares(11))
0
>>> next(gensquares(11))
0
>>> g=gensquares(11)
>>> next(g)
0
>>> next(g)
1
>>> next(g)
4
>>> 

