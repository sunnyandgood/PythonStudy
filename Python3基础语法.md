# Python3基础语法

### 一、标识符

* 第一个字符必须是字母表中字母或下划线 _ 。
* 标识符的其他的部分由字母、数字和下划线组成。
* 标识符对大小写敏感。

### 二、python保留字

  保留字即关键字，我们不能把它们用作任何标识符名称。Python 的标准库提供了一个 keyword 模块，可以输出当前版本的所有关键字： 

    >>> import keyword
    >>> keyword.kwlist
    ['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 
     'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 
     'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']

### 三、注释

* Python中单行注释以 `#` 开头，实例如下： 

      print("Hello World！")
      # print(7+9)

  >执行以上代码，输出结果为：

      Hello World！

* 多行注释可以用多个 `#` 号，还有 `'''` 和 `"""`：

      # 第一个注释
      # 第二个注释

      # print(7+9)

      '''
      第三注释
      第四注释
      '''

      """
      第五注释
      第六注释
      """

      print("Hello World！")

  >执行以上代码，输出结果为：
  
      Hello World！

### 四、行与缩进

   python最具特色的就是使用缩进来表示代码块，不需要使用大括号 `{}` 。

* 缩进的空格数是可变的，但是同一个代码块的语句必须包含相同的缩进空格数。实例如下： 

      if True:
          print("hello")
          print("world")
      else:
          print("hello")
          print("python")


  >执行以上代码，输出结果为：
  
      hello
      world

* 以下代码最后一行语句缩进数的空格数不一致，会导致运行错误：

      if True:
          print("hello")
          print("world")
      else:
          print("hello")
         print("python")# 缩进不一致，会导致运行错误

### 五、多行语句

* Python 通常是一行写完一条语句，但如果语句很长，我们可以使用反斜杠(`\`)来实现多行语句，例如：

      total = 2 + \
              6 + \
              8
      print(total)

  >执行以上代码，输出结果为：
  
      16

* 在 `[]`, `{}`, 或 `()` 中的多行语句，不需要使用反斜杠(`\`)，例如：

      total = [2,3,4,6,
               8,9,1,5,
               10,]
      print(total)

  >执行以上代码，输出结果为：
  
      [2, 3, 4, 6, 8, 9, 1, 5, 10]

### 六、数字(Number)类型

python中数字有四种类型：整数、布尔型、浮点数和复数。

* int (整数), 如 1, 只有一种整数类型 int，表示为长整型，没有 python2 中的 Long。
* bool (布尔), 如 True。
* float (浮点数), 如 1.23、3E-2
* complex (复数), 如 1 + 2j、 1.1 + 2.2j

### 七、字符串(String)

* python中单引号和双引号使用完全相同。
* 使用三引号(`'''` 或 `"""`)可以指定一个多行字符串。
* 转义符 `\`
* 反斜杠可以用来转义，使用r可以让反斜杠不发生转义。。 如 `r"this is a line with \n"` 则 `\n` 会显示，并不是换行。
* 按字面意义级联字符串，如`"this "` `"is "` `"string"`会被自动转换为`this is string`。
* 字符串可以用 `+` 运算符连接在一起，用 `*` 运算符重复。
* Python 中的字符串有两种索引方式，从左往右以 0 开始，从右往左以 -1 开始。
* Python中的字符串不能改变。
* Python 没有单独的字符类型，一个字符就是长度为 1 的字符串。
* 字符串的截取的语法格式如下：`变量[头下标:尾下标]`

    >eg:
    
      word = '字符串'
      sentence = "这是一个句子。"
      paragraph = """这是一个段落，
      可以由多行组成"""

* 实例

      str = 'sunnyandgood'

      print(str)                 # 输出字符串
      print(str[0:-1])           # 输出第一个到倒数第二个的所有字符
      print(str[0])              # 输出字符串第一个字符
      print(str[2:5])            # 输出从第三个开始到第五个的字符
      print(str[2:])             # 输出从第三个开始的后的所有字符
      print(str * 2)             # 输出字符串两次
      print(str + '你好')        # 连接字符串

      print('------------------------------')

      print('hello\nsunnyandgood')      # 使用反斜杠(\)+n转义特殊字符
      print(r'hello\nsunnyandgood')     # 在字符串前面添加一个 r，表示原始字符串，不会发生转义

  >执行以上代码，输出结果为：

      sunnyandgood
      sunnyandgoo
      s
      nny
      nnyandgood
      sunnyandgoodsunnyandgood
      sunnyandgood你好
      ------------------------------
      hello
      sunnyandgood
      hello\nsunnyandgood

### 八、空行

* 函数之间或类的方法之间用空行分隔，表示一段新的代码的开始。类和函数入口之间也用一行空行分隔，以突出函数入口的开始。

* 空行与代码缩进不同，空行并不是Python语法的一部分。书写时不插入空行，Python解释器运行也不会出错。但是空行的作用在于分隔两段不同功能或含义的代码，便于日后代码的维护或重构。

* 记住：**空行也是程序代码的一部分**。

### 九、等待用户输入（执行下面的程序在按回车键后就会等待用户输入：）
    
    input("\n\n按下 enter 键后退出。")

* 以上代码中 ，"\n\n"在结果输出前会输出两个新的空行。一旦用户按下 enter 键时，程序将退出。




































