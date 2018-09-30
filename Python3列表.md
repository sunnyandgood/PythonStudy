# Python3 列表

### 一、Python3 列表

* 序列是Python中最基本的数据结构。序列中的每个元素都分配一个数字 - 它的位置，或索引，第一个索引是0，第二个索引是1，依此类推。
* Python有6个序列的内置类型，但最常见的是列表和元组。
* 序列都可以进行的操作包括索引，切片，加，乘，检查成员。
* 此外，Python已经内置确定序列的长度以及确定最大和最小的元素的方法。
* 列表是最常用的Python数据类型，它可以作为一个方括号内的逗号分隔值出现。
* 列表的数据项不需要具有相同的类型
* 创建一个列表，只要把逗号分隔的不同的数据项使用方括号括起来即可。如下所示：

      list1 = ['Google', 'Sunny', 1997, 2000];
      list2 = [1, 2, 3, 4, 5 ];
      list3 = ["a", "b", "c", "d"];

    * 与字符串的索引一样，列表索引从0开始。列表可以进行截取、组合等。

### 二、访问列表中的值

* 使用下标索引来访问列表中的值，同样你也可以使用方括号的形式截取字符，如下所示：

     >eg:
     
      list1 = ["hello","world","sunny",1997]
      list2 = [1,2,3,4,5,6,7,8,9]

      print("list1[0]",list1[0])
      print("list2[1:5]",list2[1:5])
     
     >以上实例输出结果：

      list1[0] = hello
      list2[1:5] = [2, 3, 4, 5]

### 三、更新列表

* 可以对列表的数据项进行**修改**或**更新**，也可以使用append()方法来**添加**列表项，如下所示： 
     
     >eg:
     
      list = ["hello","world","sunny",1997]
      print("list[2] =",list[2])

      list[2] = 'good'
      print("list[2] =",list[2])
     
     >以上实例输出结果：

      list[2] = sunny
      list[2] = good

### 四、删除列表元素

* 可以使用 `del 语句` 来删除列表的的元素，如下实例：
     
     >eg:
     
      list = ["hello","world","sunny",1997]
      print(list)

      del list[1]
      print(list)
     
     >以上实例输出结果：

      ['hello', 'world', 'sunny', 1997]
      ['hello', 'sunny', 1997]

### 五、Python列表脚本操作符

* 列表对 `+` 和 `*` 的操作符与字符串相似。`+` 号用于**组合列表**，`*` 号用于**重复列表**。

    <table>
       <tr>
          <td>Python 表达式</td>
          <td>结果</td>
          <td>描述</td>
       </tr>
       <tr>
          <td>len([1, 2, 3])</td>
          <td>3</td>
          <td>长度</td>
       </tr>
       <tr>
          <td>[1, 2, 3] + [4, 5, 6]</td>
          <td>[1, 2, 3, 4, 5, 6]</td>
          <td>组合</td>
       </tr>
       <tr>
          <td>['Hi!'] * 4</td>
          <td>['Hi!', 'Hi!', 'Hi!', 'Hi!']</td>
          <td>重复</td>
       </tr>
       <tr>
          <td>3 in [1, 2, 3]</td>
          <td>TRUE</td>
          <td>元素是否存在于列表中</td>
       </tr>
       <tr>
          <td>for x in [1, 2, 3]: print(x, end=" ")</td>
          <td>1 2 3</td>
          <td>迭代</td>
       </tr>
    </table>

### 六、Python列表截取与拼接

* Python的列表截取与字符串操作类型，如下所示：

      L=['Google', 'Tencent', 'Taobao']

     >操作：

    <table>
       <tr>
          <td>Python 表达式</td>
          <td>结果</td>
          <td>描述</td>
       </tr>
       <tr>
          <td>L[2]</td>
          <td>'Taobao'</td>
          <td>读取第三个元素</td>
       </tr>
       <tr>
          <td>L[-2]</td>
          <td>'Tencent'</td>
          <td>从右侧开始读取倒数第二个元素: count from the right</td>
       </tr>
       <tr>
          <td>L[1:]</td>
          <td>['Tencent', 'Taobao']</td>
          <td>输出从第二个元素开始后的所有元素</td>
       </tr>
    </table>

* 列表还支持拼接操作：

     >eg:

      squares = [1,2,3,4,5,6]
      print(squares)

      squares += [22,33,55,88]
      print(squares)

     >以上实例输出结果：

      [1, 2, 3, 4, 5, 6]
      [1, 2, 3, 4, 5, 6, 22, 33, 55, 88]

### 七、嵌套列表

* 使用嵌套列表即在列表里创建其它列表，例如：

     >eg:

      x = ['a','b','c']
      y = [1,2,3]
      z = [x,y]

      print(z)
      print(z[0])
      print(z[0][1])

     >以上实例输出结果：

      [['a', 'b', 'c'], [1, 2, 3]]
      ['a', 'b', 'c']
      b

### 八、Python列表函数

   <table>
       <tr>
          <td>序号</td>
          <td>函数</td>
          <td>描述</td>
       </tr>
       <tr>
          <td>1</td>
          <td>len(list)</td>
          <td>列表元素个数</td>
       </tr>
       <tr>
          <td>2</td>
          <td>max(list)</td>
          <td>返回列表元素最大值</td>
       </tr>
       <tr>
          <td>3</td>
          <td>min(list)</td>
          <td>返回列表元素最小值</td>
       </tr>
       <tr>
          <td>4</td>
          <td>list(seq)</td>
          <td>将元组转换为列表</td>
       </tr>
    </table>

### 九、Python列表方法

  <table>
     <tr>
        <td>序号</td>
        <td>方法</td>
        <td>描述</td>
     </tr>
     <tr>
        <td>1</td>
        <td>list.append(obj)</td>
        <td>在列表末尾添加新的对象</td>
     </tr>
     <tr>
        <td>2</td>
        <td>list.count(obj)</td>
        <td>统计某个元素在列表中出现的次数</td>
     </tr>
     <tr>
        <td>3</td>
        <td>list.extend(seq)</td>
        <td>在列表末尾一次性追加另一个序列中的多个值（用新列表扩展原来的列表）</td>
     </tr>
     <tr>
        <td>4</td>
        <td>list.index(obj)</td>
        <td>从列表中找出某个值第一个匹配项的索引位置</td>
     </tr>
     <tr>
        <td>5</td>
        <td>list.insert(index, obj)</td>
        <td>将对象插入列表</td>
     </tr>
     <tr>
        <td>6</td>
        <td>list.pop([index=-1]])</td>
        <td>移除列表中的一个元素（默认最后一个元素），并且返回该元素的值</td>
     </tr>
     <tr>
        <td>7</td>
        <td>list.remove(obj)</td>
        <td>移除列表中某个值的第一个匹配项</td>
     </tr>
     <tr>
        <td>8</td>
        <td>list.reverse()</td>
        <td>反向列表中元素</td>
     </tr>
     <tr>
        <td>9</td>
        <td>list.sort(cmp=None, key=None, reverse=False)</td>
        <td>对原列表进行排序</td>
     </tr>
     <tr>
        <td>10</td>
        <td>list.clear()</td>
        <td>清空列表</td>
     </tr>
     <tr>
        <td>11</td>
        <td>list.copy()</td>
        <td>复制列表</td>
     </tr>
  </table>






















