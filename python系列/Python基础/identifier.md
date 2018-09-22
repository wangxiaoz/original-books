# 标识符和关键字
## 标识符
* **什么是标志符**   
开发人员在程序中自定义的名称，一般用来标识变量，函数名，类名等。

* **标识符的命名规则**
	* 标识符由字母、下划线和数字组成，且数字不能开头  
	* python中的标识符是区分大小写的                     
	
	示例：    
	
	```python
	# num 就是一个标识符，起的一个名称而已
	num = 10
	
	# 1_a是b合法的标识符，不能以数字开头
	1_a = 100
	```                      

* **标识符命名方式**
	* 驼峰命名法
		* 小驼峰式命名法（lower camel case）： 第一个单词以小写字母开始；第二个单词的首字母大写，例如：myName、aDog 
		* 大驼峰式命名法（upper camel case）： 每一个单字的首字母都采用大写字母，例如：FirstName、LastName
	* 下划线命名法
	  用下划线“_”来连接所有的单词，比如send_buf. **这是在python中推荐的方式**，因为这种方式遵循了PEP8规则.


## 关键字
* **什么是关键字**
> python一些具有特殊功能的标识符，被python程序已经所使用了，这就是所谓的关键字。如if 、else等
> 这些关键字是python已经使用的了，所以不允许开发者自己定义和关键字相同的名字的标识符



* **查看关键字**                       
使用 `import keyword`  `keyword.kwlist` 可以查看已被python程序所使用的关键字      
        
   ![关键字](/images/keyword.png)

	```python
	and     as      assert     break     class      continue    def     del
	elif    else    except     exec      finally    for         from    global
	if      in      import     is        lambda     not         or      pass
	print   raise   return     try       while      with        yield          
	```
 

