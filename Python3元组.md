# Python3 元组

### 一、Python 的元组与列表

* Python 的元组与列表类似，不同之处在于元组的元素不能修改。

* 元组使用小括号，列表使用方括号。

* 元组创建很简单，只需要在括号中添加元素，并使用逗号隔开即可。

     >eg:
     
      tup1 = ('hello','world',99,88)
      tup2 = (1,2,3,4,5,6)
      tup3 = "a","b","c","d"

      print(type(tup1))
      print(type(tup2))
      print(type(tup3))

     >以上实例输出结果：

      <class 'tuple'>
      <class 'tuple'>
      <class 'tuple'>

### 二、创建空元组

    tup1 = ()

### 三、元组中只包含一个元素时，需要在元素后面添加逗号，否则括号会被当作运算符使用：

* 元组与字符串类似，下标索引从0开始，可以进行截取，组合等。


     >eg:
     
      tup1 = (88)
      print(type(tup1))   # 不加逗号，类型为整型

      tup2 = (88,)
      print(type(tup2))   # 加上逗号，类型为元组

     >以上实例输出结果：

      <class 'int'>
      <class 'tuple'>

### 四、访问元组

* 元组可以使用下标索引来访问元组中的值，如下实例:

     >eg:
     
      tup1 = ('hello','world',88,99)
      tup2 = (1,2,3,4,5,6,7,8)

      print("tup1[0] =",tup1[0])
      print("tup2[1:5] =",tup2[1:5])

     >以上实例输出结果：

      tup1[0] = hello
      tup2[1:5] = (2, 3, 4, 5)

### 五、修改元组

* 元组中的元素值是不允许修改的，但我们可以对元组进行连接组合，如下实例:

     >eg:
     
      tup1 = (12,3.14159)
      tup2 = ('hello','world')

      # 以下修改元组元素操作是非法的。
      #tup1[0] = 100

      # 创建一个新的元组
      tup3 = tup1 + tup2
      print(tup3)

     >以上实例输出结果：
     
      (12, 3.14159, 'hello', 'world')

### 六、删除元组

* 元组中的元素值是不允许删除的，但我们可以使用del语句来删除整个元组，如下实例:

     >eg:
     
      tup = ('hello','world',99,88)

      print(tup)

      del tup

      print("删除后的元组：")
      print(tup)

     >以上实例输出结果：

      Traceback (most recent call last):
      ('hello', 'world', 99, 88)
        File "D:/studyCodes/pycharm/untitled/test.py", line 8, in <module>
      删除后的元组：
          print(tup)
      NameError: name 'tup' is not defined
  
### 七、元组运算符

* 与字符串一样，元组之间可以使用 `+` 号和 `*` 号进行运算。这就意味着他们可以组合和复制，运算后会生成一个新的元组。  

     <table>
        <tr>
           <td>Python 表达式</td>
           <td>结果</td>
           <td>描述</td>
        </tr>
        <tr>
           <td>len((1, 2, 3))</td>
           <td>3</td>
           <td>计算元素个数</td>
        </tr>
        <tr>
           <td>(1, 2, 3) + (4, 5, 6)</td>
           <td>(1, 2, 3, 4, 5, 6)</td>
           <td>连接</td>
        </tr>
        <tr>
           <td>('Hi!',) * 4</td>
           <td>('Hi!', 'Hi!', 'Hi!', 'Hi!')</td>
           <td>复制</td>
        </tr>
        <tr>
           <td>3 in (1, 2, 3)</td>
           <td>TRUE</td>
           <td>元素是否存在</td>
        </tr>
        <tr>
           <td>for x in (1, 2, 3): print (x,)</td>
           <td>1 2 3</td>
           <td>迭代</td>
        </tr>
     </table>

### 八、元组索引，截取

* 因为元组也是一个序列，所以可以访问元组中的指定位置的元素，也可以截取索引中的一段元素，如下所示：

* 元组：

          L = ('Google', 'Taobao', 'sunny')

     <table>
        <tr>
           <td>Python 表达式</td>
           <td>结果</td>
           <td>描述</td>
        </tr>
        <tr>
           <td>L[2]</td>
           <td>'sunny'</td>
           <td>读取第三个元素</td>
        </tr>
        <tr>
           <td>L[-2]</td>
           <td>'Taobao'</td>
           <td>反向读取；读取倒数第二个元素</td>
        </tr>
        <tr>
           <td>L[1:]</td>
           <td>('Taobao', 'sunny')</td>
           <td>截取元素，从第二个开始后的所有元素。</td>
        </tr>
     </table>

### 九、元组内置函数


<table>
   <tr>
      <td>序号</td>
      <td>方法及描述</td>
      <td>实例</td>
   </tr>
   <tr>
      <th rowspan="4">1</th>
      <td>len(tuple)</td>
      <td> >>> tuple1 = ('Google', 'Runoob', 'Taobao')</td>
   </tr>
   <tr>
      <th rowspan="3">计算元组元素个数</th>
      <td> >>> len(tuple1)</td>
   </tr>
   <tr>
      <td>3</td>
   </tr>
   <tr>
      <td> >>> </td>
   </tr>
   <tr>
      <th rowspan="4">2</th>
      <td>max(tuple)</td>
      <td> >>> tuple2 = ('5', '4', '8')</td>
   </tr>
   <tr>
      <th rowspan="3">返回元组中元素最大值</th>
      <td>>>> max(tuple2)</td>
   </tr>
   <tr>
      <td>'8'</td>
   </tr>
   <tr>
      <td> >>> </td>
   </tr>
   <tr>
      <th rowspan="4">3</th>
      <td>min(tuple)</td>
      <td> >>> tuple2 = ('5', '4', '8')</td>
   </tr>
   <tr>
      <th rowspan="3">返回元组中元素最小值</th>
      <td>>>> min(tuple2)</td>
   </tr>
   <tr>
      <td>'4'</td>
   </tr>
   <tr>
      <td> >>> </td>
   </tr>
   <tr>
      <th rowspan="4">4</th>
      <td>tuple(seq)</td>
      <td> >>> list1= ['Google', 'Taobao', 'Runoob', 'Baidu']</td>
   </tr>
   <tr>
      <th rowspan="3">将列表转换为元组</th>
      <td>>>> tuple1=tuple(list1)</td>
   </tr>
   <tr>
      <td> >>> tuple1</td>
   </tr>
   <tr>
      <td>('Google', 'Taobao', 'Runoob', 'Baidu')</td>
   </tr>
</table>

































































