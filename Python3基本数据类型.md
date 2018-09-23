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

* 加号 `+` 是列表连接运算符，星号 `*` 是重复操作。如下实例： 

    >eg:

      list = ['qwe',123,3.56,'sunny',88.9]
      lists = ['sunny',789]

      print(list)
      print(list[0])
      print(list[1:3])
      print(list[2:])
      print(lists * 2)
      print(list + lists)

    >执行以上程序会输出如下结果：

      ['qwe', 123, 3.56, 'sunny', 88.9]
      qwe
      [123, 3.56]
      [3.56, 'sunny', 88.9]
      ['sunny', 789, 'sunny', 789]
      ['qwe', 123, 3.56, 'sunny', 88.9, 'sunny', 789]

* 与Python字符串不一样的是，列表中的元素是可以改变的：

    >eg:

      list = [1,2,3,4,5,6]
      list[0] = 9
      list[2:5] = [19,18,17]
      print(list)

      list[2:5] = []
      print(list)

    >执行以上程序会输出如下结果：

      [9, 2, 19, 18, 17, 6]
      [9, 2, 6]

* List内置了有很多方法，例如append()、pop()等等。
* 注意：
   * 1、List写在方括号之间，元素用逗号隔开。
   * 2、和字符串一样，list可以被索引和切片。
   * 3、List可以使用+操作符进行拼接。
   * 4、List中的元素是可以改变的。


### 八、Tuple（元组）

* 元组（tuple）与列表类似，不同之处在于元组的元素不能修改。元组写在小括号 () 里，元素之间用逗号隔开。 
* 元组中的元素类型也可以不相同： 

    >eg:

      tuple = ( 'abcd', 786 , 2.23, 'sunny', 70.2  )
      tuples = (123, 'sunny')

      print (tuple)             # 输出完整元组
      print (tuple[0])          # 输出元组的第一个元素
      print (tuple[1:3])        # 输出从第二个元素开始到第三个元素
      print (tuple[2:])         # 输出从第三个元素开始的所有元素
      print (tuples * 2)        # 输出两次元组
      print (tuple + tuples)    # 连接元组

    >执行以上程序会输出如下结果：

      ('abcd', 786, 2.23, 'sunny', 70.2)
      abcd
      (786, 2.23)
      (2.23, 'sunny', 70.2)
      (123, 'sunny', 123, 'sunny')
      ('abcd', 786, 2.23, 'sunny', 70.2, 123, 'sunny')

* 元组与字符串类似，可以被索引且下标索引从0开始，-1 为从末尾开始的位置。也可以进行截取（如上）。
* 可以把字符串看作一种特殊的元组。 
* tuple的元素**不可改变**，但它可以包含可变的对象，比如list列表。 
* 构造包含 0 个或 1 个元素的元组比较特殊，所以有一些额外的语法规则： 

      tup1 = ()    # 空元组
      tup2 = (20,) # 一个元素，需要在元素后添加逗号

* string、list和tuple都属于sequence（序列）。
* 注意：
     * 1、与字符串一样，元组的元素不能修改。
     * 2、元组也可以被索引和切片，方法一样。
     * 3、注意构造包含0或1个元素的元组的特殊语法规则。
     * 4、元组也可以使用+操作符进行拼接。

### 九、Set（集合）

* 集合（set）是由一个或数个形态各异的大小整体组成的，构成集合的事物或对象称作元素或是成员。
* 基本功能是进行成员关系测试和删除重复元素。
* 可以使用大括号 { } 或者 set() 函数创建集合，注意：创建一个空集合必须用 set() 而不是 { }，因为 { } 是用来创建一个空字典。 
* 创建格式：

      parame = {value01,value02,...}
      或者
      set(value)

* 实例

    >eg:

      student = {'Kitty','Juery','Tom','Rose','Jack','Jim'}

      print(student)

      # 成员测试
      if 'Kitty' in student:
      print("kitty in Set")
      else:
      print("kitty not in Set")

      # set可以进行集合运算
      set1 = set('qwertyuiop')
      set2 = set('qweasdgiop')

      print(set1)

      print(set1 - set2) # set1和set2的差集
      print(set1 | set2) # set1和set2的并集
      print(set1 & set2) # set1和set2的交集
      print(set1 ^ set2) # set1和set2中不同时存在的元素

    >执行以上程序会输出如下结果：

      {'Rose', 'Tom', 'Juery', 'Jack', 'Jim', 'Kitty'}
      kitty in Set
      {'i', 'u', 'p', 'e', 'y', 'r', 't', 'q', 'o', 'w'}
      {'t', 'u', 'r', 'y'}
      {'i', 'a', 'p', 'e', 'g', 'q', 'o', 'u', 's', 'd', 'y', 'r', 't', 'w'}
      {'i', 'p', 'e', 'q', 'o', 'w'}
      {'s', 'a', 'u', 'd', 'g', 'y', 'r', 't'}

### 十、Dictionary（字典）

* 字典（dictionary）是Python中另一个非常有用的内置数据类型。
* 列表是有序的对象集合，字典是无序的对象集合。两者之间的区别在于：字典当中的元素是通过键来存取的，而不是通过偏移存取。
* 字典是一种映射类型，字典用"`{ }`"标识，它是一个无序的**键(key) : 值(value)对集合**。
* 键(key)必须使用**不可变类型**。
* 在同一个字典中，键(key)必须是唯一的。 
* 实例

    >eg:

      dict = {}
      dict['qwe'] = 123
      dict[2] = 'qwe'

      dicts = {'name':'sunny','code':88,'site':'NUC'}

      print(dict['qwe'])    # 输出键为 'qwe' 的值
      print(dict[2])        # 输出键为 2 的值
      print(dicts)          # 输出完整的字典
      print(dicts.keys())   # 输出所有键
      print(dicts.values()) # 输出所有值

    >执行以上程序会输出如下结果：

      123
      qwe
      {'name': 'sunny', 'code': 88, 'site': 'NUC'}
      dict_keys(['name', 'code', 'site'])
      dict_values(['sunny', 88, 'NUC'])

* 构造函数 `dict()` 可以直接从键值对序列中构建字典

    >eg:

      dict1 = dict([('sunny',1),('and1',2),('good',3)])
      dict2 = {x: x**2 for x in (2, 4, 6)}
      dict3 = dict(sunny=1, and1=2, good=3)

      print(dict1)
      print(dict2)
      print(dict3)

    >执行以上程序会输出如下结果：

      {'sunny': 1, 'and1': 2, 'good': 3}
      {2: 4, 4: 16, 6: 36}
      {'sunny': 1, 'and1': 2, 'good': 3}

* 字典类型也有一些内置的函数，例如clear()、keys()、values()等。
* 注意：
     * 1、字典是一种映射类型，它的元素是键值对。
     * 2、字典的关键字必须为不可变类型，且不能重复。
     * 3、创建空字典使用 { }。

### 十一、Python数据类型转换

* 有时候，我们需要对数据内置的类型进行转换，数据类型的转换，你只需要将数据类型作为函数名即可。
* 以下几个内置的函数可以执行数据类型之间的转换。这些函数返回一个新的对象，表示转换的值。

     <table>
        <tr>
           <td>函数</td>
           <td>描述</td>
        </tr>
        <tr>
           <td>int(x [,base])</td>
           <td>将x转换为一个整数</td>
        </tr>
        <tr>
           <td>float(x)</td>
           <td>将x转换到一个浮点数</td>
        </tr>
        <tr>
           <td>complex(real [,imag])</td>
           <td>创建一个复数</td>
        </tr>
        <tr>
           <td>str(x)</td>
           <td>将对象 x 转换为字符串</td>
        </tr>
        <tr>
           <td>repr(x)</td>
           <td>将对象 x 转换为表达式字符串</td>
        </tr>
        <tr>
           <td>eval(str)</td>
           <td>用来计算在字符串中的有效Python表达式,并返回一个对象</td>
        </tr>
        <tr>
           <td>tuple(s)</td>
           <td>将序列 s 转换为一个元组</td>
        </tr>
        <tr>
           <td>list(s)</td>
           <td>将序列 s 转换为一个列表</td>
        </tr>
        <tr>
           <td>set(s)</td>
           <td>转换为可变集合</td>
        </tr>
        <tr>
           <td>dict(d)</td>
           <td>创建一个字典。d 必须是一个序列 (key,value)元组。</td>
        </tr>
        <tr>
           <td>frozenset(s)</td>
           <td>转换为不可变集合</td>
        </tr>
        <tr>
           <td>chr(x)</td>
           <td>将一个整数转换为一个字符</td>
        </tr>
        <tr>
           <td>ord(x)</td>
           <td>将一个字符转换为它的整数值</td>
        </tr>
        <tr>
           <td>hex(x)</td>
           <td>将一个整数转换为一个十六进制字符串</td>
        </tr>
        <tr>
           <td>oct(x)</td>
           <td>将一个整数转换为一个八进制字符串</td>
        </tr>
     </table>












































