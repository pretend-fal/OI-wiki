#排列组合

---

##排列组合简介

排列组合是组合数学中的一种。排列就是指从给定个数的元素中取出指定个数的元素进行排序；组合则是指从给定个数的元素中仅仅取出指定个数的元素，不考虑排序。排列组合的中心问题是研究给定要求的排列和组合可能出现的情况总数。 排列组合与古典概率论关系密切。

在高中初等数学中，排列组合多是利用列表、枚举等方法解题。

---

##排列组合公式及定义


###排列的定义

从$n$个不同元素中，任取$m$($m≤n$,$m$与$n$均为自然数,下同）个元素按照一定的顺序排成一列，叫做从$n$个不同元素中取出$m$个元素的一个排列；从$n$个不同元素中取出$m$($m≤n$）个元素的所有排列的个数，叫做从$n$个不同元素中取出$m$个元素的排列数，用符号 $A_n^m$ 表示。

###排列的计算公式

$$A_n^m = n(n-1)(n-2)......(n-m+1) = \frac{n!}{(n - m)!}$$

**$n$!代表$n$的阶乘，即6! = 1 × 2 × 3 × 4 × 5 × 6.**

###组合的定义

从n个不同元素中，任取m(m≤n）个元素并成一组，叫做从n个不同元素中取出m个元素的一个组合；从n个不同元素中取出m(m≤n）个元素的所有组合的个数，叫做从n个不同元素中取出m个元素的组合数。用符号 $C_n^m$ 表示。

###组合的计算公式

$$\binom{n}{m} = n(n-1)(n-2)......(n-m+1) = \frac{n!}{(n - m)!}$$

##排列组合的分类

###排列

**全排列**:<br>
$n$个人全部来排队，队长为$n$。第一个位置可以选$n$个，第二位置可以选$n-1$个，以此类推得：

$$A_n^n = n(n-1)(n-2)......3 × 2 × 1 = n!$$

**部分排列**:<br>
$n$个人选$m$个来排队($m<=n$)。第一个位置可以选$n$个，第二位置可以选$n-1$个，以此类推，第$m$个（最后一个）可以选($n-m+1$)个，得：

$$A_n^m = n(n-1)(n-2)......(n-m+1) = \frac{n!}{(n - m)!}$$

###组合

$n$个人$m$($m<=n$)个出来，不排队，不在乎顺序$C_n^m$。如果在乎排列那么就是$A_n^m$，如果不在乎那么就要除掉重复，那么重复了多少？同样选出的来的$m$个人，他们还要“全排”得$A_n^m$，所以得：

$$\binom{n}{m} * m! = A_n,m$$

$$\binom{n}{m} = \frac{A_n^m}{m!} = \frac{n!}{(n-m)! * m!}$$

####组合数的性质

$$\binom{n}{m} = \binom{n}{n-m}$$

$$\binom{n}{m} = \binom{n-1}{m} + \binom{n-1}{m-1}$$

如果编程实现，以上两个公式有没有帮助？

###圆排列

n个人全部来围成一圈为$Q_n^n$，其中已经排好的一圈，从不同位置断开，又变成不同的队列。<br>
所以：

$$Q_n^n * n = A_n^n → Q_n = \frac{A_n^n}{n} = (n-1)!$$

**由此可知：部分圆排**

$$Q_n^r = \frac{A_n^r}{r} = \frac{n!}{r * (n-r)!}$$
