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


* 实例

     >eg

      a = 5
      b = 2

      if(a == b):
          print("1、a等于b")
      else:
          print("1、a不等于b")

      if(a != b):
          print("2、a不等于b")
      else:
          print("2、a等于b")

      if(a < b):
          print("3、a小于b")
      else:
          print("3、a大于等于b")

      if(a > b):
          print("4、a大于b")
      else:
          print("4、a小于等于b")

      # 修改变量 a 和 b 的值
      a = 2
      b = 5
      if(a <= b):
          print("5、a小于等于b")
      else:
          print("5、a大于b")

      if(a >= b):
          print("6、a大于等于b")
      else:
          print("6、a小于b")


     >以上实例输出结果：

      1、a不等于b
      2、a不等于b
      3、a大于等于b
      4、a大于b
      5、a小于等于b
      6、a小于b

### 四、Python赋值运算符

  >以下假设变量a为10，变量b为20：

  <table>
     <tr>
        <td>运算符</td>
        <td>描述</td>
        <td>实例</td>
     </tr>
     <tr>
        <td>=</td>
        <td>简单的赋值运算符</td>
        <td>c = a + b 将 a + b 的运算结果赋值为 c</td>
     </tr>
     <tr>
        <td>+=</td>
        <td>加法赋值运算符</td>
        <td>c += a 等效于 c = c + a</td>
     </tr>
     <tr>
        <td>-=</td>
        <td>减法赋值运算符</td>
        <td>c -= a 等效于 c = c - a</td>
     </tr>
     <tr>
        <td>*=</td>
        <td>乘法赋值运算符</td>
        <td>c *= a 等效于 c = c * a</td>
     </tr>
     <tr>
        <td>/=</td>
        <td>除法赋值运算符</td>
        <td>c /= a 等效于 c = c / a</td>
     </tr>
     <tr>
        <td>%=</td>
        <td>取模赋值运算符</td>
        <td>c %= a 等效于 c = c % a</td>
     </tr>
     <tr>
        <td>**=</td>
        <td>幂赋值运算符</td>
        <td>c **= a 等效于 c = c ** a</td>
     </tr>
     <tr>
        <td>//=</td>
        <td>取整除赋值运算符</td>
        <td>c //= a 等效于 c = c // a</td>
     </tr>
  </table>

### 五、Python位运算符

* 按位运算符是把数字看作二进制来进行计算的。Python中的按位运算法则如下：
* 下表中变量 a 为 60，b 为 13二进制格式如下：

      a = 0011 1100
      b = 0000 1101
      -----------------
      a&b = 0000 1100
      a|b = 0011 1101
      a^b = 0011 0001
      ~a  = 1100 0011

* Python位运算符

    <table>
       <tr>
          <td>运算符</td>
          <td>描述</td>
          <td>实例</td>
       </tr>
       <tr>
          <td>&</td>
          <td>按位与运算符：参与运算的两个值,如果两个相应位都为1,则该位的结果为1,否则为0</td>
          <td>(a & b) 输出结果 12 ，二进制解释： 0000 1100</td>
       </tr>
       <tr>
          <td>|</td>
          <td>按位或运算符：只要对应的二个二进位有一个为1时，结果位就为1。</td>
          <td>(a | b) 输出结果 61 ，二进制解释： 0011 1101</td>
       </tr>
       <tr>
          <td>^</td>
          <td>按位异或运算符：当两对应的二进位相异时，结果为1</td>
          <td>(a ^ b) 输出结果 49 ，二进制解释： 0011 0001</td>
       </tr>
       <tr>
          <td>~</td>
          <td>按位取反运算符：对数据的每个二进制位取反,即把1变为0,把0变为1。~x 类似于 -x-1</td>
          <td>(~a ) 输出结果 -61 ，二进制解释： 1100 0011， 在一个有符号二进制数的补码形式。</td>
       </tr>
       <tr>
          <td><<</td>
          <td>左移动运算符：运算数的各二进位全部左移若干位，由"<<"右边的数指定移动的位数，高位丢弃，低位补0。</td>
          <td>a << 2 输出结果 240 ，二进制解释： 1111 0000</td>
       </tr>
       <tr>
          <td>>></td>
          <td>右移动运算符：把">>"左边的运算数的各二进位全部右移若干位，">>"右边的数指定移动的位数</td>
          <td>a >> 2 输出结果 15 ，二进制解释： 0000 1111</td>
       </tr>
    </table>
























