# AQS

## Unsafe
Unsafe提供的CAS功能，其中valueOffset可以理解为value在内存中的偏移量，对应了CAS三个操作数(V/A/B)中的V
Unsafe是用来帮助Java访问操作系统底层资源的类（如可以分配内存、释放内存），通过Unsafe，Java具有了底层操作能力，可以提升运行效率。
强大的底层资源操作能力也带来了安全隐患(类的名字Unsafe也在提醒我们这一点)，因此正常情况下用户无法使用。

## synchronized
是一个重量级的操作，不仅是因为加锁需要消耗额外的资源，还因为线程状态的切换会涉及操作系统核心态和用户态的转换。
不过随着JVM对锁进行的一系列优化(如自旋锁、轻量级锁、锁粗化等)，synchronized的性能表现已经越来越好。