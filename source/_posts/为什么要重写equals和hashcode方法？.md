---
title: 为什么要重写equals和hashcode方法？
tags: Java
categories: 总结
---

#### Object的equals方法
    public boolean equals(Object obj) {
        return (this == obj);
    }
    
#### equals()与‘==’的区别
1.‘==’比较对象的地址
2.equals()比较的是对象的内容
3.如果不对equals()进行重新，实际还是进行对象地址的比较

### equals()的重写规则
* 自反性：对于任何非null的引用值x，x.equals(x)应返回true。
* 对称性：对于任何非null的引用值x与y，当且仅当：y.equals(x)返回true时，x.equals(y)才返回true。
* 传递性：对于任何非null的引用值x、y与z，如果y.equals(x)返回true，y.equals(z)返回true，那么x.equals(z)也应返回true。
* 一致性：对于任何非null的引用值x与y，假设对象上equals比较中的信息没有被修改，则多次调用x.equals(y)始终返回true或者始终返回false。
* 对于任何非空引用值x，x.equal(null)应返回false。
