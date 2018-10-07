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































