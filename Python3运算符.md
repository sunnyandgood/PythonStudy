# Python3运算符

### 一、什么是运算符？

Python语言支持以下类型的运算符:
* 算术运算符
* 比较（关系）运算符
* 赋值运算符
* 逻辑运算符
* 位运算符
* 成员运算符
* 身份运算符
* 运算符优先级

### 二、Python算术运算符

  >以下假设变量a为10，变量b为21：

  <table>
     <tr>
        <td>运算符</td>
        <td>描述</td>
        <td>实例</td>
     </tr>
     <tr>
        <td>+</td>
        <td>加 - 两个对象相加</td>
        <td>a + b 输出结果 31</td>
     </tr>
     <tr>
        <td>-</td>
        <td>减 - 得到负数或是一个数减去另一个数</td>
        <td>a - b 输出结果 -11</td>
     </tr>
     <tr>
        <td>*</td>
        <td>乘 - 两个数相乘或是返回一个被重复若干次的字符串</td>
        <td>a * b 输出结果 210</td>
     </tr>
     <tr>
        <td>/</td>
        <td>除 - x 除以 y</td>
        <td>b / a 输出结果 2.1</td>
     </tr>
     <tr>
        <td>%</td>
        <td>取模 - 返回除法的余数</td>
        <td>b % a 输出结果 1</td>
     </tr>
     <tr>
        <td>**</td>
        <td>幂 - 返回x的y次幂</td>
        <td>a**b 为10的21次方</td>
     </tr>
     <tr>
        <td>//</td>
        <td>取整除 - 返回商的整数部分</td>
        <td>9//2 输出结果 4 , 9.0//2.0 输出结果 4.0</td>
     </tr>
  </table>

* 实例

     >eg

      a = 5
      b = 2
      c = 0

      c = a + b
      print("1、c = a + b  的值为:",c)

      c = a - b
      print("2、c = a - b  的值为:",c)

      c = a * b
      print("3、c = a * b  的值为:",c)

      c = a / b
      print("4、c = a / b  的值为:",c)

      c = a % b
      print("5、c = a % b  的值为:",c)

      c = a ** b
      print("6、c = a ** b 的值为:",c)

      c = a // b
      print("7、c = a // b 的值为:",c)


     >以上实例输出结果：

      1、c = a + b  的值为: 7
      2、c = a - b  的值为: 3
      3、c = a * b  的值为: 10
      4、c = a / b  的值为: 2.5
      5、c = a % b  的值为: 1
      6、c = a ** b 的值为: 25
      7、c = a // b 的值为: 2

### 三、Python比较运算符

   >以下假设变量a为10，变量b为20：

  <table>
     <tr>
        <td>运算符</td>
        <td>描述</td>
        <td>实例</td>
     </tr>
     <tr>
        <td>==</td>
        <td>等于 - 比较对象是否相等</td>
        <td>(a == b) 返回 False。</td>
     </tr>
     <tr>
        <td>!=</td>
        <td>不等于 - 比较两个对象是否不相等</td>
        <td>(a != b) 返回 True。</td>
     </tr>
     <tr>
        <td>></td>
        <td>大于 - 返回x是否大于y</td>
        <td>(a > b) 返回 False。</td>
     </tr>
     <tr>
        <td><</td>
        <td>小于 - 返回x是否小于y。所有比较运算符返回1表示真，返回0表示假。这分别与特殊的变量True和False等价。注意，这些变量名的大写。</td>
        <td>(a < b) 返回 True。</td>
     </tr>
     <tr>
        <td>>=</td>
        <td>大于等于 - 返回x是否大于等于y。</td>
        <td>(a >= b) 返回 False。</td>
     </tr>
     <tr>
        <td><=</td>
        <td>小于等于 - 返回x是否小于等于y。</td>
        <td>(a <= b) 返回 True。</td>
     </tr>
  </table>






































