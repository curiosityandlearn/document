
iterator:
迭代，指从一组数据中，可以一次取出一个数据。
1,generator是迭代器(含有yield的函数或者generator表达式)
2,用__iter__定义的函数是迭代器
3,用__getitem__定义的函数是迭代器
4,iter(object)是迭代器
5,迭代器是含有next()方法的对象
6,当迭代器从数组中取完数据，抛出StopIteration异常
7,string,list,dictionary 都是可迭代的。





