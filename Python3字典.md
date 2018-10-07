# Python3 字典

### 一、Python3 字典

* 字典是另一种可变容器模型，且可存储任意类型对象。
* 字典的每个键值(key=>value)对用冒号(:)分割，每个对之间用逗号(,)分割，整个字典包括在花括号({})中 ,格式如下所示： 

      d = {key1 : value1, key2 : value2 }

* 键必须是唯一的，但值则不必。
* 值可以取任何数据类型，但键必须是不可变的，如字符串，数字或元组。
* 一个简单的字典实例：

      dict = {'Alice': '2341', 'Beth': '9102', 'Cecil': '3258'}

* 也可如此创建字典：

      dict1 = { 'abc': 456 };
      dict2 = { 'abc': 123, 98.6: 37 };

### 二、访问字典里的值

* 把相应的键放入到方括号中，如下实例:

     >eg:
     
      dict = {'Name':'zhangsan','age':20,'class':'first'}

      print("dict['Name']:",dict['Name'])
      print("dict['age']:",dict['age'])
      print("dict['class']:",dict['class'])

     >以上实例输出结果：

      dict['Name']: zhangsan
      dict['age']: 20
      dict['class']: first

* 如果用字典里没有的键访问数据，会输出错误如下：

     >eg:
     
      dict = {'Name':'zhangsan','age':20,'class':'first'}

      print("dict['aaa']",dict['aaa'])

     >以上实例输出结果：

      Traceback (most recent call last):
        File "D:/studyCodes/pycharm/untitled/test.py", line 3, in <module>
          print("dict['aaa']",dict['aaa'])
      KeyError: 'aaa'


### 三、修改字典

* 向字典添加新内容的方法是增加新的键/值对，修改或删除已有键/值对如下实例:

     >eg:
     
      dict = {'name':'zhangsan','age':'21','class':'first'}

      print(dict)

      dict['age'] = 18
      dict['school'] = 'NUC'

      print(dict)

     >以上实例输出结果：

      {'name': 'zhangsan', 'age': '21', 'class': 'first'}
      {'name': 'zhangsan', 'age': 18, 'class': 'first', 'school': 'NUC'}

### 四、删除字典元素

* 能删单一的元素也能清空字典，清空只需一项操作。
* 显示删除一个字典用del命令，如下实例：

     >eg:
     
      dict = {'name':'zhangsan','age':'21','class':'first'}

      del dict['class'] #删除键'class'
      print(dict)

      dict.clear()      #清空字典
      print(dict)

      del dict          #删除字典
      print(dict['name'])

     >以上实例输出结果：

      Traceback (most recent call last):
      {'name': 'zhangsan', 'age': '21'}
        File "D:/studyCodes/pycharm/untitled/test.py", line 10, in <module>
      {}
          print(dict['name'])
      TypeError: 'type' object is not subscriptable

### 五、字典键的特性

* 字典值可以是任何的 python 对象，既可以是标准的对象，也可以是用户定义的，但键不行。
* 两个重要的点需要记住：
      
     * 1）不允许同一个键出现两次。创建时如果同一个键被赋值两次，后一个值会被记住，如下实例：

          >eg:

           dict = {'name':'zhangsan','age':'21','class':'first','name':'菜鸡'}

           print(dict['name'])

          >以上实例输出结果：

           菜鸡

     * 2）键必须不可变，所以可以用数字，字符串或元组充当，而用列表就不行，如下实例：

          >eg:

           dict = {['name']:'zhangsan','age':'21','class':'first'}

           print("dict['name']",dict['name'])

          >以上实例输出结果：

           Traceback (most recent call last):
             File "D:/studyCodes/pycharm/untitled/test.py", line 1, in <module>
               dict = {['name']:'zhangsan','age':'21','class':'first'}
           TypeError: unhashable type: 'list'

### 六、字典内置函数

<table>
   <tr>
      <td>序号</td>
      <td>函数及描述</td>
      <td>实例</td>
   </tr>
   <tr>
      <th rowspan="3">1</th>
      <td>len(dict)</td>
      <td> >>> dict = {'Name': 'Runoob', 'Age': 7, 'Class': 'First'}</td>
   </tr>
   <tr>
      <th rowspan="2">计算字典元素个数，即键的总数。</th>
      <td> >>> len(dict)</td>
   </tr>
   <tr>
      <td>3</td>
   </tr>
   <tr>
      <th rowspan="3">2</th>
      <td>str(dict)</td>
      <td> >>> dict = {'Name': 'Runoob', 'Age': 7, 'Class': 'First'}</td>
   </tr>
   <tr>
      <th rowspan="2">输出字典，以可打印的字符串表示。</th>
      <td>>>> str(dict)</td>
   </tr>
   <tr>
      <td>"{'Name': 'Runoob', 'Class': 'First', 'Age': 7}"</td>
   </tr>
   <tr>
      <th rowspan="3">3</th>
      <td>type(variable)</td>
      <td> >>> dict = {'Name': 'Runoob', 'Age': 7, 'Class': 'First'}</td>
   </tr>
   <tr>
      <th rowspan="2">返回输入的变量类型，如果变量是字典就返回字典类型。</th>
      <td> >>> type(dict)</td>
   </tr>
   <tr>
      <td> < class 'dict' > </td>
   </tr>
</table>

### 七、字典内置方法

<table>
   <tr>
      <td>序号</td>
      <td>函数</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>1</td>
      <td>radiansdict.clear()</td>
      <td>删除字典内所有元素</td>
   </tr>
   <tr>
      <td>2</td>
      <td>radiansdict.copy()</td>
      <td>返回一个字典的浅复制</td>
   </tr>
   <tr>
      <td>3</td>
      <td>radiansdict.fromkeys()</td>
      <td>创建一个新字典，以序列seq中元素做字典的键，val为字典所有键对应的初始值</td>
   </tr>
   <tr>
      <td>4</td>
      <td>radiansdict.get(key, default=None)</td>
      <td>返回指定键的值，如果值不在字典中返回default值</td>
   </tr>
   <tr>
      <td>5</td>
      <td>key in dict</td>
      <td>如果键在字典dict里返回true，否则返回false</td>
   </tr>
   <tr>
      <td>6</td>
      <td>radiansdict.items()</td>
      <td>以列表返回可遍历的(键, 值) 元组数组</td>
   </tr>
   <tr>
      <td>7</td>
      <td>radiansdict.keys()</td>
      <td>返回一个迭代器，可以使用 list() 来转换为列表</td>
   </tr>
   <tr>
      <td>8</td>
      <td>radiansdict.setdefault(key, default=None)</td>
      <td>和get()类似, 但如果键不存在于字典中，将会添加键并将值设为default</td>
   </tr>
   <tr>
      <td>9</td>
      <td>radiansdict.update(dict2)</td>
      <td>把字典dict2的键/值对更新到dict里</td>
   </tr>
   <tr>
      <td>10</td>
      <td>radiansdict.values()</td>
      <td>返回一个迭代器，可以使用 list() 来转换为列表</td>
   </tr>
   <tr>
      <td>11</td>
      <td>pop(key[,default])</td>
      <td>删除字典给定键 key 所对应的值，返回值为被删除的值。key值必须给出。 否则，返回default值。</td>
   </tr>
   <tr>
      <td>12</td>
      <td>popitem()</td>
      <td>随机返回并删除字典中的一对键和值(一般删除末尾对)。</td>
   </tr>
</table>



























