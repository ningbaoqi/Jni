### JNI概述
image1

+ JNI是Java Native Interface的缩写，含义为Java本地调用；承载Java世界的虚拟机是用native语言写的，而虚拟机又运行在具体的平台上，所以虚拟机本身无法做到平台无关，然而，有了Jni技术后就可以对Java层屏蔽不同操作系统平台之间的差异，这样就实现了Java本身的平台无关特性；从Java到C/C++建立的是函数间的关联，而从C/C++到Java，必须先得到Java对象的引用，才能调用该对象的方法；无论是从Java到C/C++还是从C/C++到Java，中间都没有跨线程调用，两者在一个线程中运行，但是在各自打印的log中，线程Id的值是不同的，这只是两者所使用的线程Id表示方法不同而已，Java层的线程Id是一个从1开始的整数，C/C++使用的则是一个与线程相关的数据结构的指针值，两者不能比较；
