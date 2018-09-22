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

### 十、同一行显示多条语句

* Python可以在同一行中使用多条语句，语句之间使用分号( `;` )分割，以下是一个简单的实例：
    
    >eg:
    
    * test.py
    
          import sys; x = 'sunnyandgood'; sys.stdout.write(x + '\n')

        >执行以上代码，输出结果为：

          sunnyandgood

    * 使用交互式命令行执行，输出结果为：

          >>> import sys; x = 'sunnyandgood'; sys.stdout.write(x + '\n')
          sunnyandgood
          13
          
      * 此处的 13 表示字符数。

### 十一、多个语句构成代码组

* 缩进相同的一组语句构成一个代码块，我们称之代码组。
* 像`if`、`while`、`def`和`class`这样的复合语句，首行以关键字开始，以冒号(` : `)结束，该行之后的一行或多行代码构成代码组。
* 我们将首行及后面的代码组称为一个子句(clause)。

      flag = 2
      if (flag == 1):
          print("beauty==1")
      elif (flag == 2):
          print("beauty==2")
      else          :
          print("beauty!=1  && beauty!=2")

### 十二、Print 输出

* print 默认输出是换行的，如果要实现不换行需要在变量末尾加上 `end=" "`：

      print("hello")
      print("world")

      print("-----------------")
      
      print()

      print("hello ",end=" ")
      print("world",end=" ")

     >执行以上代码，输出结果为：

      hello
      world
      -----------------

      hello  world 

### 十三、`import` 与 `from...import`

* 在 python 用 `import` 或者 `from...import` 来导入相应的模块。

* 将整个模块(somemodule)导入，格式为： `import somemodule`

* 从某个模块中导入某个函数,格式为： `from somemodule import somefunction`

* 从某个模块中导入多个函数,格式为： `from somemodule import firstfunc, secondfunc, thirdfunc`

* 将某个模块中的全部函数导入，格式为： `from somemodule import *`

    >eg:
    
    * 导入 sys 模块

          import sys
          print("--------Python import mode-----------")
          print("命令行参数为:")
          for i in sys.argv:
              print(i)
          print("\n python 路径为",sys.path)


         >执行以上代码，输出结果为：

          --------Python import mode-----------
          命令行参数为:
          D:/studyCodes/pycharm/untitled/test.py

          python 路径为 ['D:\\studyCodes\\pycharm\\untitled', 'D:\\studyCodes\\pycharm\\untitled', 'C:\\Users\\sunny\\AppData\\Local\\Programs\\Python\\Python37\\python37.zip', 'C:\\Users\\sunny\\AppData\\Local\\Programs\\Python\\Python37\\DLLs', 'C:\\Users\\sunny\\AppData\\Local\\Programs\\Python\\Python37\\lib', 'C:\\Users\\sunny\\AppData\\Local\\Programs\\Python\\Python37', 'C:\\Users\\sunny\\AppData\\Local\\Programs\\Python\\Python37\\lib\\site-packages']

    * 导入 sys 模块的 argv,path 成员

          from sys import argv,path  #  导入特定的成员
          print("-------python from import-------")
          print("argv:",argv)
          print("path:",path)# 因为已经导入path成员，所以此处引用时不需要加sys.path

         >执行以上代码，输出结果为：


          -------python from import-------
          argv: ['D:/studyCodes/pycharm/untitled/test.py']
          path: ['D:\\studyCodes\\pycharm\\untitled', 'D:\\studyCodes\\pycharm\\untitled', 'C:\\Users\\sunny\\AppData\\Local\\Programs\\Python\\Python37\\python37.zip', 'C:\\Users\\sunny\\AppData\\Local\\Programs\\Python\\Python37\\DLLs', 'C:\\Users\\sunny\\AppData\\Local\\Programs\\Python\\Python37\\lib', 'C:\\Users\\sunny\\AppData\\Local\\Programs\\Python\\Python37', 'C:\\Users\\sunny\\AppData\\Local\\Programs\\Python\\Python37\\lib\\site-packages']


### 十四、命令行参数

* 很多程序可以执行一些操作来查看一些基本信息，Python可以使用-h参数查看各参数帮助信息：


      $ python -h
      usage: C:\Users\sunny\AppData\Local\Programs\Python\Python37\python.exe [option] ... 
                                  [-c cmd | -m mod | file | -] [arg] ...
      Options and arguments (and corresponding environment variables):
      -b     : issue warnings about str(bytes_instance), str(bytearray_instance)
               and comparing bytes/bytearray with str. (-bb: issue errors)
      -B     : don't write .pyc files on import; also PYTHONDONTWRITEBYTECODE=x
      -c cmd : program passed in as string (terminates option list)
      -d     : debug output from parser; also PYTHONDEBUG=x
      -E     : ignore PYTHON* environment variables (such as PYTHONPATH)
      -h     : print this help message and exit (also --help)
      -i     : inspect interactively after running script; forces a prompt even
               if stdin does not appear to be a terminal; also PYTHONINSPECT=x
      -I     : isolate Python from the user's environment (implies -E and -s)
      -m mod : run library module as a script (terminates option list)
      -O     : optimize generated bytecode slightly; also PYTHONOPTIMIZE=x
      -OO    : remove doc-strings in addition to the -O optimizations
      -q     : don't print version and copyright messages on interactive startup
      -s     : don't add user site directory to sys.path; also PYTHONNOUSERSITE
      -S     : don't imply 'import site' on initialization
      -u     : force the stdout and stderr streams to be unbuffered;
               this option has no effect on stdin; also PYTHONUNBUFFERED=x
      -v     : verbose (trace import statements); also PYTHONVERBOSE=x
               can be supplied multiple times to increase verbosity
      -V     : print the Python version number and exit (also --version)
               when given twice, print more information about the build
      -W arg : warning control; arg is action:message:category:module:lineno
               also PYTHONWARNINGS=arg
      -x     : skip first line of source, allowing use of non-Unix forms of #!cmd
      -X opt : set implementation-specific option
      file   : program read from script file
      -      : program read from stdin (default; interactive mode if a tty)
      arg ...: arguments passed to program in sys.argv[1:]

      Other environment variables:
      PYTHONSTARTUP: file executed on interactive startup (no default)
      PYTHONPATH   : ';'-separated list of directories prefixed to the
                     default module search path.  The result is sys.path.
      PYTHONHOME   : alternate <prefix> directory (or <prefix>;<exec_prefix>).
                     The default module search path uses <prefix>\lib.
      PYTHONCASEOK : ignore case in 'import' statements (Windows).
      PYTHONIOENCODING: Encoding[:errors] used for stdin/stdout/stderr.
      PYTHONFAULTHANDLER: dump the Python traceback on fatal errors.
      PYTHONHASHSEED: if this variable is set to 'random', a random value is used
         to seed the hashes of str, bytes and datetime objects.  It can also be
         set to an integer in the range [0,4294967295] to get hash values with a
         predictable seed.
      PYTHONMALLOC: set the Python memory allocators and/or install debug hooks
         on Python memory allocators. Use PYTHONMALLOC=debug to install debug
         hooks.
      PYTHONCOERCECLOCALE: if this variable is set to 0, it disables the locale
         coercion behavior. Use PYTHONCOERCECLOCALE=warn to request display of
         locale coercion and locale compatibility warnings on stderr.



















