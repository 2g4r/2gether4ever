@[toc]
#### === 和 ==的区别  
使用“`==`”，等号两边类型不同时，JS会把它们转为同一类型比较。
使用“`===`”时，不会进行类型转换，两边类型不同，一定不相等。

`false`,`''`,`""`都 `= 0`

`null ~！= 0`

`NAN`不等于任何值，包括它自己。  
判断`NAN`用`isNaN(NaN)` ,值为`true`  

####  字符串操作  
* `Str.charAt(index)` 返回字符串index位置的元素
* `Str.charCodeAt(index)` 返回字符串index位置的元素的编码
* `Str.fromCharCode(numX,…,numX)` ，numX是字符编码，str将会是由numX拼成的字符串 ，numX的个数>1  

* `Str.toUpperCase()`字符串大写  
* `Str.toLowerCase()`字符串小写  

* `Str.sub()` 字符下标  
* `Str.sup()` 字符上角标  
* `Str.strike()` 字符变为删除线  

* `Str.trim()`删除字符串前后的空格  

* `Str.replace()`字符串替换，可用于字符串内容的判断  

	**Str.replace(oldstr,newstr)**  
	+ `oldstr`：必需，用于被替换的字符串  
	+ `newstr`：必需，用于替换oldstr的字符串，可以是字符串、正则或函数  

* `Str.split(str)` 把字符串分割成数组     
* `Str1.content(Str2)`连接两个字符串  
* `Str.indexOf(值)`  检索字符串中是否存在某元素，存在返回元素的第一次出现的位置，不存在返回`-1`  
* `Str.slice(start，end)` 返回字符串从start（包括start）开始到end（不包括end）为止的所有字符 。  
	+ 如果start是负数则表示从字符串尾部开始start长度的字符串
* `Str.Substr(start，length)` 返回字符串从start（包括start）开始的length长度的字符  
	+ 如果start是负数表示从末尾第一位开始的start长度的字符串  
* `Str.SubString(start，stop)`，  返回字符串从start（包括start）开始到stop-1为止的所有字符  
	+ start=stop返回空串  
	+ start stop均不能为负  

#### 数组操作
* `Array.join(str)` 把数组用str连接成一个字符串  
* `Array.pop()` 删除并返回数组中的最后一个元素  
* `Array.slice(元素位置)`  从数组中返回选定的元素  
* `Array.splice()` 删除元素并向数组中添加新元素   
	**Array.splice(index,howmany,item1,…,itemX)**  
	+ 从index的位置开始删除howmany个元素，并从item中添加元素  
	+ index为负：从数组结尾处规定元素（倒着看数组位置）   
	+ howmany=0：不删除项目  
* `Array.push()` 在数组末尾添加并返回新的长度  
* `Array.unshift()` 在数组开头添加并返回新的长度  
