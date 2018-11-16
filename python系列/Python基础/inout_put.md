# 输出与输入

## 输出
  在python中，可以使用**print函数**向屏幕终端输出内容，以下是print函数用法       
  
  * **普通输出**
  ```python
	# 在python2中，可以不带括号的输出内容，也可以带括号，python2.7为了兼容python3
    print "hello word"
	pirnt("hello word")
	
    # 但在python3中输出，必须要带括号，否则会报语法错误
	print("hello,python ")
    # 同时在python中，还以传入end参数的值，默认值是'\n',在python2中不可以传入
	print("hello word", end=",")
  ```

  * **格式化输出**
   在程序中，看到了%这样的操作符，这就是Python中格式化输出。
   ```python
	age = 18
    print("年龄是%d" % age)
   
	# 输入2个以上变量的值，需要使用()括起来
	name = "张三"
    age = 20
	print("姓名是%s,年龄是%d" %(name,age))
    
    #浮点数默认保留6位小数，但可以指定保留几位小数
    >>> a = 3.14356
	>>> print('%0.2f' % a)
	3.14
	>>> a = 3.14656
	>>> print('%0.2f' % a)  # 会四舍五入
	3.15
   ```


  * **常用的格式化输出符号**  
   下面是完整的，与％符号使用      

| 格式符号 | 转换 | 
| :------: | :------: | 
|%c	|字符| 
|%s	|通过str() 字符串转换来格式化| 
|%i	|有符号十进制整数| 
|%d	|有符号十进制整数| 
|%u	|无符号十进制整数| 
|%o	|八进制整数| 
|%x	|十六进制整数（小写字母）| 
|%X	|十六进制整数（大写字母）| 
|%e	|科学计数法（小写'e'）| 
|%E	|科学计数法（大写“E”）| 
|%f	|浮点数| 
|%g	|％f和％e 的简写| 
|%G	|％f和％E的简写| 





# 输入  
在python中，可以使用**raw_input函数**(python2中使用) 、**input函数**(python3中使用) 向接收键盘的输入      

* **raw_input()用法**  
```python
# raw_input从键盘接收的内容都当作字符串类型赋值给左边的passwrod变量
password = raw_input("请输入密码:")
print '您刚刚输入的密码是:', password
```
**注意:**
 * raw_input()的小括号中放入的是"提示信息"，用来在获取数据之前给用户的一个简单提示
 * raw_input()在从键盘获取了数据以后，会存放到等号右边的变量中
 * raw_input()会把用户输入的任何值都作为字符串来对待



* **python3中的input()用法**
 * 在python3中，input()函数与raw_input()功能用法一样。
 * 在python3中，没有raw_input()函数，只有input()


* **特别指出，在python2中也有一个input()函数，但和raw_input功能不一样**
  ```python
    # 接收的值是个表达式，如果表达式的值式int，则就直接作为int值赋给等号左边变量
	>>> a = input() 
	123
	>>> type(a)
	<type 'int'>
    # 输入abc，会认为是一个变量，而不是一个字符串，如果需要输入字符串，使用引号
	>>> a = input()
	abc
	Traceback (most recent call last):
	  File "<stdin>", line 1, in <module>
	  File "<string>", line 1, in <module>
	NameError: name 'abc' is not defined
	>>> a = input()
	"abc"
	>>> type(a)
	<type 'str'>
	>>> a = input()
	1+3
	>>> a
	4
	>>> a = input()
	"abc"+"def"
	>>> a
	'abcdef'
	>>> value = 100
	>>> a = input()
	value
	>>> a
	100
  ```
**注意：** input()接受表达式输入，并把表达式的结果赋值给等号左边的变量

