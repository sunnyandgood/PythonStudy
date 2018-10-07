# Python3 集合 

### 一、Python3 集合 

* 集合（set）是一个无序的不重复元素序列。
* 可以使用大括号 { } 或者 set() 函数创建集合，注意：创建一个空集合必须用 set() 而不是 { }，因为 { } 是用来创建一个空字典。 
* 创建格式：

      parame = {value01,value02,...}
      或者
      set(value)
      
* 实例

     >eg:
     
      frulit = {'apple','orange','apple','pear','orange','banana'}

      print(frulit)
      print('orange' in frulit)
      print('tea' in frulit)

      # 两个集合间的运算。
      a = set('abracadabra')
      b = set('alacazam')

      print(a)
      print(b)

      print(a - b)
      print(a | b)
      print(a & b)
      print(a ^ b)

     >以上实例输出结果：
	 
	  {'apple', 'orange', 'banana', 'pear'}
      True
      False
      {'b', 'c', 'a', 'd', 'r'}
      {'z', 'c', 'a', 'm', 'l'}
      {'b', 'd', 'r'}
      {'b', 'z', 'c', 'a', 'l', 'm', 'd', 'r'}
      {'c', 'a'}
      {'b', 'm', 'd', 'z', 'r', 'l'}
	 











































































































