## C++ unordered_map
### 1 std::unorded_map的定义
`unordered_map`是一个将`key`和`value`关联起来的容器，它可以高效的根据单个`key`值查找对应的`value`。`unordered_map`查询单个`key`的时候效率比`map`高，但要查询某一范围内的`key`时效率更低。可以使用[ ]操作符来访问`key`对应的`value`。
* 所在头文件：`<unordered_map>`
* `std::unordered_map`类模板：
```C++
template<class Key,                                 // unordered_map::key_type
         class T,                                   // unordered_map::mapped_type
         class Hash = hash<Key>,                    // unordered_map::hasher
         class Pred = equal_to<Key>,                // unordered_map::key_equal
         class Alloc = allocator<pair<const key, T>>// unordered_map::allocator_type
         > class unordered_map;
```
### 2 特性
* 关联性：`std::unordered_map`是一个关联容器，其中的元素根据`key`来引用，而不是根据索引来引用。
* 无序性：在内部，`std::unordered_map`中的元素不会根据其`key`或映射值按任何顺序排序，而是根据其哈希值组织到桶中，以允许通过`key`直接快速访问各个元素（常量的平均时间复杂度）。
* 唯一性：`std::unordered_map`中的元素的`key`是唯一的。`key`和`value`的数据类型可以不同。
### 3 基本函数实现
#### 3.1 构造函数
#### 3.2 成员函数
* `unordered_map:: count(const Key& keyval)`：查找与指定`key`匹配的元素数