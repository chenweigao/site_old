---
layout: page
title: C语言实训上机指导(4)
---

![cguide]({{ site.url }}/assets/cguide.png)

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

  {% highlight c++ %}
   polynomial a, b;
   a[0] = 13;
   a.insert({{1, 5}, {2, 9}}); //c++11

   b[1] = 10;
   b[2] = 20;
   b.insert(std::pair<int, int>(3, 30));
   {% endhighlight %}

   多项式计算如下: 
$$
   y_1=13x^0 + 5x^1 +9x^2 \\
   y_2=10x^1 + 20x^2 + 30x^3\\
   y_1+y_2 = 13x^0 +15x^1 +29x^2 +30x^3
$$

   # 2. 目标文件

   目标文件是什么？**编译器编译源代码后生成的文件**。

   可执行文件分为两种：PE(Windows)，ELF(Linux)，目标文件.obj(Windows)和.o(Linux)跟可执行文件的结构基本相同。

   ```shell
   file xxx.o
   gcc -c SimpleSection.c
   objdump -h SimpleSection.o
   readelf -h SimpleSection.o
   ```

   