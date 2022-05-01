## Company1 c++面试
 
struct 和 class 的区别 
1 struct 和 class 的访问权限不同 其他一样
2 struct 通常被用作 数据union

c++内存布局 堆和栈谁比较大 生命周期

RAII smartpointer unqiue_ptr 用move进行 shared_ptr内部的计数在哪个区域 weak_ptr解决了什么问题 shared_ptr 在c++标准库里线程安全吗 count是安全的 读写要加锁

上下文切换

c++ 同步原语有哪些

mutex 和 atomic 的区别 以及 开销上的区别 c++ mutex 怎么实现的？？？

三种锁 spin 读写 互斥 
现象：

（1）单线程无锁速度最快，但应用场合受限；

（2）多线程无锁速度第二快，但结果不对，未保护临界代码段；

（3）多线程原子锁第三快，且结果正确；

（4）多线程互斥量较慢，慢与原子锁近10倍，结果正确；

（5）多线程自旋锁最慢，慢与原子锁30倍，结果正确。

结论：原子锁速度最快，互斥量和自旋锁都用保护多线程共享资源。

       自旋锁是一种非阻塞锁，也就是说，如果某线程需要获取自旋锁，但该锁已经被其他线程占用时，该线程不会被挂起，而是在不断的消耗CPU的时间，不停的试图获取自旋锁。
       互斥量是阻塞锁，当某线程无法获取互斥量时，该线程会被直接挂起，该线程不再消耗CPU时间，当其他线程释放互斥量后，操作系统会激活那个被挂起的线程，让其投入运行。

       在多处理器环境中对持有锁时间较短的程序来说使用自旋锁代替一般的互斥锁往往能提高程序的性能，但是本代码无该效果。


tempplate CRTP是什么？？？

虚函数是怎么实现的 能不能重载 纯虚类为什么不能实例化

声明顺序 和 构造顺序 要考虑到依赖关系

static_thread_local 是什么？？？

tcp/ip 的划分有多少层 三次握手细节 为什么不是两次 为什么不是4次 四次握手细节

I/O多路复用

STL有哪些容器 增删改查复杂度

hashtable rehash

vector 扩容 用的是移动 怎么返回vector 不调用 拷贝构造

emplace_back 帮助调用了构造函数 push_back是什么

vector 自从有了移动后 就不会拷贝了 没有移动的时候 写函数都是传引用或是指针

construtor 和 destructor 为什么一个不能是virtual 一个是virtual

一道leetcode reverselist
clear以后 capacity 还是原来的 曾经用的是swap去改 现在用的方法 shrinktofit()
编码习惯 一般不用nullptr == 
草案 翻导论
两本书 c++并发编程实战 c++tempplates 必须都是第二版
去论坛上回答别人的问题

https://blog.51cto.com/quantfabric/2588193





mingleng 一

为什么要设置昨仓今仓
写的结构是什么
tcp udp 区别
http了解吗
polymorphism 怎么实现的
内存分布
64寻址的最大寻址空间
lambda细节 和函数指针的区别

mingleng 二
交易进程crash掉了 怎么恢复

防止 exception 在程序退出前 catch一下 但是crash不会  如何恢复交易信号 持仓

记log 怎么让他不影响 系统性能

不影响 critical path 如何log 记录时间
提供一个线程 专门在计数寄存器上++ 怎么确认时间颗粒 不能用cpu 频率 可能不准

verilog 怎么handle 时钟 pos_edge 那么 在linux下在用户态高精度时钟 有什么接口去拿cpu时间戳

uint64_t rdtsc(){
    unsigned int lo,hi;
    __asm__ __volatile__ ("rdtsc" : "=a" (lo), "=d" (hi));
    return ((uint64_t)hi << 32) | lo;
}
有没有写过dll
一道prime计算 start开始 第count个 prime


为什么要 noexcept
docker了解吗 ubuntu的docker可以放到centos吗

c++ 书 cppcon blog
性能调优 redhat centos的说明书
找一些commnuity 哪些公司的人会做性能 公司的人是不是会让他去在网络上share 


