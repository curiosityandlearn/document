generator(生成器）的好处是：
占用CPU、内存资源小，速度快

1,含有yield的函数是generator；
2，在python2.x中，xrange()是generator，range()是list（列表)
3，例如:x=(a for a in range(10)),x是generator




yield

含有yield的函数是generator（生成器），当执行此函数时，执行到yield时，返回一个值，继续执行。直到所有值生成。
如果用generator.next()的方法，当遇到yield时，返回一个值，然后函数挂起。再执行generator.next()，函数从前一次挂起的位置继续执行，直到抛出错误，此时需要generator.close()结束函数。

