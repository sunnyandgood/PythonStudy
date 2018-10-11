# Python3 变量

### 一、局部变量和全局变量

* 函数体内的变量叫局部变量；函数体外的变量叫全局变量

* 代码1. 局部变量作用域覆盖全局变量

      def p_num():
          num=5
          print(num)

      num = 10
      p_num()
      print(num)

      # 结果为 5 10

* 代码2. 函数内有局部变量定义，解释器不使用全局变量，局部变量的定义晚于被引用，报错

      def p_num():
          print(num)
          num=5
          print(num)

      num = 10
      p_num()
      print(num)

      # 结果出错

* 代码3. 函数内部可以直接访问全局变量

      def p_num():
          print(num)

      num = 10
      p_num()
      print(num)

      # 结果为 10 10

* 代码4. 函数内修改全局变量,使用global关键字

      def p_num():
          global num
          print(num)
          num = 8
          print(num)

      num = 10
      p_num()
      print(num)

      # 结果为 10 8 8

### 二、特殊变量


* `_xxx`：    `from module import *`无法导入     

* `__xxx__`：  系统定义的变量     

* `__xxx`：   类的本地变量



















