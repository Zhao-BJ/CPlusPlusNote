## C++ Vector 容器
### 1 什么是Vector？

向量(Vector)是一个封装了动态大小数组的顺序容器(Sequence Container)。跟任意其它类型容器一样，它能够存放各种类型的对象。可以简单的认为，向量是一个可以存放任意类型的动态数组。

### 2 容器特性  
#### 2.1 顺序序列
顺序容器中的元素按照严格的线性顺序排列。可以通过元素在序列中的位置访问对应的元素。
#### 2.2 动态数组
支持对序列中的任意元素进行快速直接访问，甚至可以通过指针算术进行该操作。提供了在序列末尾相对快速的添加/删除元素的操作。
#### 2.3 能够感知内存分配器(Allocator-aware)
容器使用一个内存分配器对象来动态地处理它的存储需求。
### 3基本函数实现
#### 3.1 构造函数
* vector(): 创建一个空vector
* vector(int nSize): 创建一个vector，元素个数为nSize
* vector(int nSize, const t& t): 创建一个vector，元素个数为nSize，且均值为t
* vector(const vector&): 复制构造函数
* vector(begin, end): 复制[begin, end]区间内另一个数组的元素到vector中