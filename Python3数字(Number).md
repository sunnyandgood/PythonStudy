# Python3 数字(Number)

### 一、Python 数字数据类型

* Python 数字数据类型用于存储数值。
* 数据类型是不允许改变的,这就意味着如果改变数字数据类型的值，将重新分配内存空间。
* 以下实例在变量赋值时 Number 对象将被创建：

      var1 = 1
      var2 = 10

* 也可以使用del语句删除一些数字对象的引用。 

     >del语句的语法是：
     
      del var1[,var2[,var3[....,varN]]]]

* 可以通过使用del语句删除单个或多个对象的引用，例如：

      del var
      del var_a, var_b

### 二、Python 支持三种不同的数值类型：

* 整型(int)：通常被称为是整型或整数，是正或负整数，不带小数点。Python3 整型是没有限制大小的，可以当作 Long 类型使用，所以 Python3 没有 Python2 的 Long 类型。

* 浮点型(float)：浮点型由整数部分与小数部分组成，浮点型也可以使用科学计数法表示（2.5e2 = 2.5 x 10² = 250）

* 复数(complex)：复数由**实数部分**和**虚数部分**构成，可以用 `a + bj` ,或者`complex(a,b)`表示， 复数的实部a和虚部b都是浮点型。

-----------------

可以使用十六进制和八进制来代表整数：

    >>> number = 0xA0F # 十六进制
    >>> number
    2575

    >>> number=0o37 # 八进制
    >>> number
    31

----------------

  <table>
     <tr>
        <td>int</td>
        <td>float</td>
        <td>complex</td>
     </tr>
     <tr>
        <td>10</td>
        <td>0</td>
        <td>3.14j</td>
     </tr>
     <tr>
        <td>100</td>
        <td>15.2</td>
        <td>45.j</td>
     </tr>
     <tr>
        <td>-786</td>
        <td>-21.9</td>
        <td>9.322e-36j</td>
     </tr>
     <tr>
        <td>80</td>
        <td>32.3+e18</td>
        <td>.876j</td>
     </tr>
     <tr>
        <td>-490</td>
        <td>-90</td>
        <td>-.6545+0J</td>
     </tr>
     <tr>
        <td>-0x260</td>
        <td>-3.25E+101</td>
        <td>3e+26J</td>
     </tr>
     <tr>
        <td>0x69</td>
        <td>70.2-E12</td>
        <td>4.53e-7j</td>
     </tr>
  </table>































































