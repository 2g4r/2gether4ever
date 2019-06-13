###Welcome to use JavaScript
##js的**set**和**map**
### map：  
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

###set：  
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


### js创建七天的数组  
```
[... Array ( 7 ). keys ()]. map ( days => new Date ( Date . now () - 86400000 * days ));  
 //创建过去七天的数组，  
如果把加号换成减号，表示创建未来七天的数组
```
###获得一个随机字符串  
```
Math . random (). toString ( 36 ). substring ( 2 );//获得一个随机字符串（11位）
```

