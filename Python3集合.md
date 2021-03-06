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
	 
* 类似列表推导式，同样集合支持集合推导式(Set comprehension):

     >eg:
     
	  a = {x for x in 'abracadabra'  if x not in 'abc'}
      print(a)

     >以上实例输出结果：
	 
	  {'d', 'r'}
	 
### 二、添加元素

* 语法格式如下：

	  s.add( x )

* 将元素 x 添加到集合 s 中，如果元素已存在，则不进行任何操作。

     >eg:
     
      thisSet = set(("hello","world","sunny"))
      print(thisSet)

      thisSet.add("good")
      print(thisSet)

     >以上实例输出结果：
	 
      {'sunny', 'world', 'hello'}
      {'good', 'sunny', 'world', 'hello'}
	 
* 还有一个方法，也可以添加元素，且参数可以是列表，元组，字典等，语法格式如下：

      s.update( x )

     * x 可以有多个，用逗号分开。

          >eg:
     
	       thisSet = set(("hello","world","sunny"))
	       print(thisSet)

	       thisSet.update({1,8})
	       print(thisSet)

	       thisSet.update([1,4],[5,6])
	       print(thisSet)

          >以上实例输出结果：
	 
           {'sunny', 'hello', 'world'}
           {'sunny', 1, 'hello', 8, 'world'}
           {'sunny', 1, 'hello', 4, 5, 6, 8, 'world'}
	 
### 三、移除元素

* 语法格式如下：

      s.remove( x )

     * 将元素 x 从集合 s 中移除，如果元素不存在，则会发生错误。

          >eg:
     
           thisSet = set(("hello","world","sunny"))
           print(thisSet)

           thisSet.remove("world")
           print(thisSet)

           thisSet.remove("aaa")
           print(thisSet)

          >以上实例输出结果：
	 
           {'hello', 'sunny', 'world'}
           Traceback (most recent call last):
           {'hello', 'sunny'}
             File "D:/studyCodes/pycharm/untitled/test.py", line 7, in <module>
               thisSet.remove("aaa")
           KeyError: 'aaa'
	 
* 此外还有一个方法也是移除集合中的元素，且如果元素不存在，不会发生错误。格式如下所示：

      s.discard( x )

     >eg:

      thisSet = set(("hello","world","sunny"))
      print(thisSet)

      thisSet.discard("world")
      print(thisSet)

      thisSet.discard("aaa")
      print(thisSet)

     >以上实例输出结果：

      {'sunny', 'world', 'hello'}
      {'sunny', 'hello'}
      {'sunny', 'hello'}

* 也可以设置随机删除集合中的一个元素，语法格式如下：

      s.pop() 

	 * 多次执行测试结果都不一样。
	
 	* 然而在交互模式，pop 是删除集合的第一个元素（排序后的集合的第一个元素）。 
     
     >eg:

	       thisSet = set(("hello","world","sunny"))
	       print(thisSet)

	       x = thisSet.pop()
	       print(x)
	       print(thisSet)

	 >以上实例输出结果：

	       {'hello', 'sunny', 'world'}
	       hello
	       {'sunny', 'world'}
	 

### 四、计算集合元素个数

* 语法格式如下：

      len(s)

     >eg:

      thisSet = set(("hello","world","sunny"))

      x = len(thisSet)
      print(x)

     >以上实例输出结果：

      3

### 五、清空集合

* 语法格式如下：

      s.clear()

     >eg:

      thisSet = set(("hello","world","sunny"))

      thisSet.clear()
      print(thisSet)

     >以上实例输出结果：

      set()

### 六、判断元素是否在集合中存在

* 语法格式如下：

      x in s

     * 判断元素 s 是否在集合 x 中存在，存在返回 True，不存在返回 False。

          >eg:

           thisSet = set(("hello","world","sunny"))

           a = "hello" in thisSet
           b = "aaa" in thisSet

           print(a)
           print(b)

          >以上实例输出结果：

           True
           False

### 七、集合内置方法完整列表

<table>
   <tr>
      <td>方法</td>
      <td>描述</td>
   </tr>
   <tr>
      <td>add()</td>
      <td>为集合添加元素</td>
   </tr>
   <tr>
      <td>clear()</td>
      <td>移除集合中的所有元素</td>
   </tr>
   <tr>
      <td>copy()</td>
      <td>拷贝一个集合</td>
   </tr>
   <tr>
      <td>difference()</td>
      <td>返回多个集合的差集</td>
   </tr>
   <tr>
      <td>difference_update()</td>
      <td>移除集合中的元素，该元素在指定的集合也存在。</td>
   </tr>
   <tr>
      <td>discard()</td>
      <td>删除集合中指定的元素</td>
   </tr>
   <tr>
      <td>intersection()</td>
      <td>返回集合的交集</td>
   </tr>
   <tr>
      <td>intersection_update()</td>
      <td>删除集合中的元素，该元素在指定的集合中不存在。</td>
   </tr>
   <tr>
      <td>isdisjoint()</td>
      <td>判断两个集合是否包含相同的元素，如果没有返回 True，否则返回 False。</td>
   </tr>
   <tr>
      <td>issubset()</td>
      <td>判断指定集合是否为该方法参数集合的子集。</td>
   </tr>
   <tr>
      <td>issuperset()</td>
      <td>判断该方法的参数集合是否为指定集合的子集</td>
   </tr>
   <tr>
      <td>pop()</td>
      <td>随机移除元素</td>
   </tr>
   <tr>
      <td>remove()</td>
      <td>移除指定元素</td>
   </tr>
   <tr>
      <td>symmetric_difference()</td>
      <td>返回两个集合中不重复的元素集合。</td>
   </tr>
   <tr>
      <td>symmetric_difference_update()</td>
      <td>移除当前集合中在另外一个指定集合相同的元素，并将另外一个指定集合中不同的元素插入到当前集合中。</td>
   </tr>
   <tr>
      <td>union()</td>
      <td>返回两个集合的并集</td>
   </tr>
   <tr>
      <td>update()</td>
      <td>给集合添加元素</td>
   </tr>
</table>











































































