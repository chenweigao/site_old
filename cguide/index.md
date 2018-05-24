---
layout: page
title: C语言实训上机指导(4)
---

# 1. 多项式相加

实现方法：

1. 链表
2. map

```c++
map<int, int> polynomial;
```

定义如上所示的map

```c++
polynomial merge(polynomial a, polynomial b){
    polynomial result;
    for (auto i:a){
        result[i.first]=i.second;
    }

    for (auto i:b){
        result[i.first]=result[i.first]+i.second;
    }

    return result;
}
```

编写函数实现。[参考源码:GitHub](https://github.com/chenweigao/_code/blob/master/Test_C%2B%2B/polynomial.cpp)

## Map

1. map能自动建立**key - value**的对应， key和value可以是任意类型。

2. 使用map需要添加头文件`#inlcude<map>`

3. 为了使用方便，使用模板类进行类型定义：`typedef std::map<int, int> polynomial; `

4. 可以使用`insert()`方法添加数据(单个插入使用`std::pair`)，也可以使用数组方法插入数据

5. 使用`auto`关键字遍历容器是一种很好的方法

   | key（指数） | value（基数） |
   | :---------: | :-----------: |
   |      0      |      13       |
   |      1      |       5       |
   |      2      |       9       |

   

