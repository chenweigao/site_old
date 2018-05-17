---
layout: post
title: Notes - An introduction to algorithmic competition
key: acm
tags:
  - Algorithm
comment: true
---

ACM, the world's largest educational and scientific computing society, delivers resources that advance computing as a science and a profession. ACM provides the computing field's premier Digital Library and serves its members and the computing profession with leading-edge publications, conferences, and career resources.
<!--more-->
## Loops and Recursive

### Define Struct
There are many ways to define *struct*, what we should do is that chose a best way to solve problem.

**Example 1**
{% highlight c %}
struct Point { double x, y; };
double dist(struct Point a, struct Point b){
    return hypot(a.x-b.x, a.y-b.y);
}
{% endhighlight %}

**Example2**

{% highlight c %}
typedef struct { double x, y; } Point;
double dist(Point a, Point b){
    return hypot(a.x-b.x, a.y-b.y);
}
{% endhighlight %}

As you can see from the comparison, **Example 2** is better, which use `typedef struct { define; }struct name; ` to define.

