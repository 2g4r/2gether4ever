**安装**  
1. tsc --init ,生成tsconfig.json，改“outDir”：“./js”  
2. 运行任务，监视tsconfig.json  

**ts中为了使编写的代码更规范，更有利于维护，增加了类型校验**  
写rs代码，必须指定类型  
`var flag:boolean = true`
+ 布尔类型 Boolean
+ 数字类型 number  
+ 字符串类型 string  
+ 数组类型 array  
  1. `var arr:number[] = [1,2]`  
  //数组中所有元素为数字类型  
  2. `var arr:Array<number> =[11,22,33]`  
+ 元组类型 tuple:属于数组的一种  
  `let arr:[number,string] = [111,'this is ts']`  
+ 枚举类型 enum  
```
enum Flag{success=1,error=2}  
let s:Flag=Flag.success//如果标识符没有赋值，其值为下标
```  
+ 任意类型 any  
 `var num:any = '111'`  
 任意类型的用处:ts无object，any可暂用  
+ undefined  
变量定义未赋值就是undefined  
+ null
+ void 表示没有任何类型，一般用于定义方法的时候方法没有返回值  
```
function run():void{
	console.log('run')
}
run()
```
*一般来讲，函数返回什么类型函数就是什么类型*  
+ never类型：是其他类型（包括null和undefined），代表从不会出现的值    
 *这意味着never的变量只能被never类型赋值*
 null只能赋值null，undefined同理