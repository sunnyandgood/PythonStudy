# Python3 基本数据类型

* Python 中的变量不需要声明。每个变量在使用前都必须赋值，变量赋值以后该变量才会被创建。

* 在 Python 中，变量就是变量，它没有类型，我们所说的"类型"是变量所指的内存中对象的类型。

* 等号（`=`）用来给变量赋值。

* 等号（`=`）运算符左边是一个变量名,等号（`=`）运算符右边是存储在变量中的值。

     >eg

      num = 100              #整形变量
      real = 18.9            #浮点变量
      name = "sunnyandgood"  #字符串
      print("num =",num,"；real =",real,"；name =",name)

     >执行以上程序会输出如下结果：

      num = 100 ；real = 18.9 ；name = sunnyandgood


### 一、多个变量赋值

* Python允许你同时为多个变量赋值。例如：

      a = b = c = 1

  * 以上实例，创建一个整型对象，值为 1，从后向前赋值，三个变量都指向同一个内存地址。 
* 也可以为多个对象指定多个变量。例如：

      a,b,c = 1,8,"sunnyandgood"

    * 以上实例，两个整型对象 1 和 8 的分配给变量 a 和 b，字符串对象 "sunnyandgood" 分配给变量 c。

### 二、标准数据类型

* Python3 中有六个标准的数据类型： 
     * Number（数字）
     * String（字符串）
     * List（列表）
     * Tuple（元组）
     * Set（集合）
     * Dictionary（字典）

* Python3 的六个标准数据类型中：
    * 不可变数据（3 个）：
        * Number（数字）、
        * String（字符串）、
        * Tuple（元组）；
    * 可变数据（3 个）：
        * List（列表）、
        * Dictionary（字典）、
        * Set（集合）。 

### 三、Number（数字）

* Python3 支持 int、float、bool、complex（复数）。 

* 在Python 3里，只有一种整数类型 int，表示为长整型，没有 python2 中的 Long。

* 像大多数语言一样，数值类型的赋值和计算都是很直观的。

* 内置的 type() 函数可以用来查询变量所指的对象类型。
    
     >eg:

      a,b,c,d = 1,True,"sunnyandgood",8+9j
      print(type(a))
      print(type(b))
      print(type(c))
      print(type(d))

     >执行以上程序会输出如下结果：

      <class 'int'>
      <class 'bool'>
      <class 'str'>
      <class 'complex'>

* 此外还可以用 isinstance 来判断：

     >eg:

      a,b,c,d = 1,True,"sunnyandgood",8+9j
      print(isinstance(a,int))
      print(isinstance(b,bool))
      print(isinstance(c,str))
      print(isinstance(d,complex))

     >执行以上程序会输出如下结果：

      True
      True
      True
      True

* isinstance 和 type 的区别：
    * type()不会认为子类是一种父类类型。
    * isinstance()会认为子类是一种父类类型。

     >eg:

      class TestA:
          pass
      class TestB(TestA):
          pass

      print(isinstance(TestA(),TestA))    #True
      print(type(TestA())==TestA)         #True
      print(isinstance(TestB(),TestA))    #True
      print(type(TestB())==TestA)         #False

     >执行以上程序会输出如下结果：

      True
      True
      True
      False

    * 注意：在 Python2 中是没有布尔型的，它用数字 0 表示 False，用 1 表示 True。到 Python3 中，把 True 和 False 定义成关键字了，但它们的值还是 1 和 0，它们可以和数字相加。

* 当指定一个值时，Number 对象就会被创建：

      num1 = 9
      num2 = 8

* 也可以使用del语句删除一些对象引用。

    * del语句的语法是：`del var1[,var2[,var3[....,varN]]]`
    * 可以通过使用del语句删除单个或多个对象。例如：

          del num1
          del num2,num3

### 四、数值运算

* 1、Python可以同时为多个变量赋值，如a, b = 1, 2。
* 2、一个变量可以通过赋值指向不同类型的对象。
* 3、数值的除法包含两个运算符：`/` 返回一个浮点数，`//` 返回一个整数。
* 4、在混合计算时，Python会把整型转换成为浮点数。 
* 5、Python还支持复数，复数由实数部分和虚数部分构成，可以用`a + bj`,或者`complex(a,b)`表示， 复数的实部a和虚部b都是浮点型

* 7、实例

      print(8 + 9)   # 加法 17
      print(8.0 - 5) # 减法 3.0
      print(8 * 9)   # 乘法 72
      print(3 / 6)   # 除法，得到一个浮点数 0.5
      print(3 // 6)  # 除法，得到一个整数   0
      print(8 % 3)   # 取余 2
      print(2 ** 5)  # 乘方 32

### 五、数值类型实例

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
        <td>3.23E+19</td>
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
        <td>7.02E-11</td>
        <td>4.53e-7j</td>
     </tr>
  </table>

### 六、String（字符串）

* Python中的字符串用单引号 ' 或双引号 " 括起来，同时使用反斜杠 `\` 转义特殊字符。
* 字符串的截取的语法格式如下：

      变量[头下标:尾下标]

    * 索引值以 0 为开始值，-1 为从末尾的开始位置。

    <div align="center"><img src="./img/字符串.png"/></div>

* 加号 + 是字符串的连接符， 星号 * 表示复制当前字符串，紧跟的数字为复制的次数。

    >eg:
    
      str = 'sunnyandgood'

      print(str)                 # 输出字符串
      print(str[0:-1])           # 输出第一个到倒数第二个的所有字符
      print(str[0])              # 输出字符串第一个字符
      print(str[2:5])            # 输出从第三个开始到第五个的字符
      print(str[2:])             # 输出从第三个开始的后的所有字符
      print(str * 2)             # 输出字符串两次
      print(str + ' hello')      # 连接字符串

    >执行以上程序会输出如下结果：

      sunnyandgood
      sunnyandgoo
      s
      nny
      nnyandgood
      sunnyandgoodsunnyandgood
      sunnyandgood hello

* Python 使用反斜杠(`\`)转义特殊字符，如果你不想让反斜杠发生转义，可以在字符串前面添加一个 `r`，表示原始字符串：

    >eg:

      str = 'sunnyandgood'

      print('hello\nsunnyandgood')      # 使用反斜杠(\)+n转义特殊字符
      print(r'hello\nsunnyandgood')     # 在字符串前面添加一个 r，表示原始字符串，不会发生转义

    >执行以上程序会输出如下结果：

      hello
      sunnyandgood
      hello\nsunnyandgood

     * 另外，反斜杠(`\`)可以作为续行符，表示下一行是上一行的延续。也可以使用 `"""..."""` 或者 `'''...'''` 跨越多行。 

* 注意，Python 没有单独的字符类型，一个字符就是长度为1的字符串。 


    >eg:

      str = 'Python'

      print(str[0],str[5])
      print(str[-1],str[-6])

    >执行以上程序会输出如下结果：

      P n
      n P

* 与 C 字符串不同的是，Python 字符串不能被改变。向一个索引位置赋值，比如 `word[0] = 'm'`会导致错误。
* 注意：
     * 1、反斜杠可以用来转义，使用r可以让反斜杠不发生转义。
     * 2、字符串可以用+运算符连接在一起，用*运算符重复。
     * 3、Python中的字符串有两种索引方式，从左往右以0开始，从右往左以-1开始。
     * 4、Python中的字符串不能改变。

### 七、List（列表）

* List（列表） 是 Python 中使用最频繁的数据类型。

* 列表可以完成大多数集合类的数据结构实现。列表中元素的类型可以不相同，它支持数字，字符串甚至可以包含列表（所谓嵌套）。

* 列表是写在方括号 [] 之间、用逗号分隔开的元素列表。

* 和字符串一样，列表同样可以被索引和截取，列表被截取后返回一个包含所需元素的新列表。 

* 列表截取的语法格式如下：

      变量[头下标:尾下标]

* 索引值以 0 为开始值，-1 为从末尾的开始位置。

    <div align="center"><img src="./img/list_slicing1.png"/></div>















