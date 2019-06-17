####Welcome to use JavaScript
##js的**set**和**map**
#### map：  
一组键值对的结构，具有极快的查找速度  
+ 初始化map  
1. 一个二维数组  
`var m = new Map([['a','x'],['b','y'],['c','z']])`  
`{"a"=>"x","b"=>"y","c"=>"z"}`  
2. 直接初始化一个空map  
`var m = new Map()//空map`  
+ 直接根据key查找相应的value  
`m.get('a')`  
`"x"`  
+ 添加新的key-value  
`m.set('d','0')`  
`{"a"=>"x","b"=>"y","c"=>"z","d"=>"0"}`  
+ 判断是否存在key，存在返回true，不存在返回false  
`m.has('a')` `true`  
`m.has('w')` `false`  
+ 删除key  
`m.delete('a')` `true`  

####set：  
与map类似，也是一组key的集合，但是不存储value。因为key不能重复，所以key中没有重复的key  
+ 创建一个set  
1. 提供一个数组  
`var s = new Set([1,2,3])`  `{1,2,3}`  
2. 创建一个空set  
`var s = new Set()`  
+ set中重复元素自动过滤  
`var ss = new Set([1,1,2,2,3,3,4])` `{1,2,3,4}`  
+ add添加新的key，可以重复添加，但是不会有结果  
`s.add(5)` `{1,2,3,5}`    
+ delete删除元素   
`s.delete(2)` `true`


#### js创建七天的数组  
```
[... Array ( 7 ). keys ()]. map ( days => new Date ( Date . now () - 86400000 * days ));  
 //创建过去七天的数组，  
如果把加号换成减号，表示创建未来七天的数组
```

####获得一个随机字符串  
```
Math . random (). toString ( 36 ). substring ( 2 );//获得一个随机字符串（11位）
```

####获取屏幕高度  
`document.body.clientheight` 可操作的高度  
`screen.availHeight` 可获得的高度  ，会减去屏幕高度中导航的高度
`screen.height` 得到整个屏幕，包括导航栏的高度
`window.innerHeight` 整个屏幕，减去屏幕高度中的导航和工具栏的高度  

#### Math方法  
* `Math.random()`   
	随机小数（0-1）  
* `Math.floor(Math.random() * 10)`   
	0-9的随机整数  
* `Math.round(x)`    
	四舍五入  
* `Math.ceil(x)`   
	向上取整  
* `Math.floor(x)`   
	向下取整  
* `Math.pow(x,y)`   
	x的y次方
* `Math.sqrt(x)`  
	x开方  
* `Math.abs(x)`  
	x的绝对值  
* `Math.min(a,b,c,...,n)`和`Math.max(a,b,c,...,n)`   
	查找数列中的最小值和最大值  
	
#### localStrong 本地存储  

* `localStorage.setItem('key',value)`  
	向本地存储添加key的value  
* `localStorage.getItem('key')`  
	得到本地存储中key的value值
* `localStorage.key(n)`  
	返回存在在本地存储中第n条数据的key  
* `localStorage.removeItem('key')`  
	删除指定的key  
* `localStorage.clear()`  
	删除所有本地存储  
* `JSON.stringify()`  
	将JSON数据转为字符串  
* `JSON.parse()`  
	将字符串转换为JSON数据输出  