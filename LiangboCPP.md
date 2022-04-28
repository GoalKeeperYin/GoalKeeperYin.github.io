## Company1 c++面试
 
struct 和 class 的区别 
1 struct 和 class 的访问权限不同 其他一样
2 struct 通常被用作 数据union

c++内存布局 堆和栈谁比较大 生命周期

RAII smartpointer unqiue_ptr 用move进行 shared_ptr内部的计数在哪个区域 weak_ptr解决了什么问题 shared_ptr 在c++标准库里线程安全吗

mutex 和 atomic 的区别 以及 开销上的区别 c++ mutex 怎么实现的？？？

三种锁 spin 读写 互斥 

tempplate CRTP是什么？？？

虚函数是怎么实现的 能不能重载 纯虚类为什么不能实例化

声明顺序 和 构造顺序 要考虑到依赖关系

static_thread_local 是什么？？？

tcp/ip 的划分有多少层 三次握手细节 为什么不是两次 为什么不是4次 四次握手细节

I/O多路复用

STL有哪些容器 增删改查复杂度

hashtable rehash

vector 扩容 用的是移动 怎么返回vector 不调用 拷贝构造

inplace_back push_back是什么

clear以后 capacity 还是原来的 曾经用的是swap去改 现在用的方法 shrinktofit()


vector 自从有了移动后 就不会拷贝了 没有移动的时候 写函数都是传引用或是指针

construtor 和 destructor 为什么一个不能是virtual 一个是virtual


一道leetcode reverselist

编码习惯 一般不用nullptr == 
草案 翻导论
两本书 c++并发编程实战 c++tempplates 必须都是第二版
去论坛上回答别人的问题

