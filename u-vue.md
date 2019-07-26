## 创建VUE  
`<div id="ul_schcode"></div>`  
```
var schcode = new Vue({
	el:'#ul_schcode',//“,”逗号必写，el指这个vue操作的组件名，可以是id，也可以是class
})
```  
需要绑定元素的时候  
`<div id="ul_schcode">{{name}}</div>`  
```
var schcode = new Vue({
	el:'#ul_schcode',//“,”逗号必写，el指这个vue操作的组件名，可以是id，也可以是class
	data:{
		name:'sss'
	}
})
```    
操作dom  
`<div id="ul_schcode" v-on:click:"fun()">{{name}}</div>`  
```
var schcode = new Vue({
	el:'#ul_schcode',//“,”逗号必写，el指这个vue操作的组件名，可以是id，也可以是class
	data:{
		name:'sss'
	},
	methods:{
		fun:function(){
			
		}
	}
})
```  
## 操作

#### `v-model`  
绑定数据，  
*注意：所有元素均需要在vue中定义*  
`<input type = "text" v-model = "name"/>`
```
<span>{{name}}</span>
```  
#### `v-show`  
v-show=“false”的时候隐藏，为true的时候显示  
```
<p v-show="show">显示</p>
```  

```
data:{
	show:true,(当show的值为false的时候隐藏)
}
``` 
#### `v-if`  
可与v-else或v-elseif连用  
```
<p v-if="show">显示</p>
<p v-else="!show">隐藏</p>
```  

```
data:{
	show:true,(当show的值为true的时候第一行显示，为false的时候第二行显示)
}
``` 
#### `v-for`  
循环  
```
<ul>
<li v-for = "n in name.length">{{name[n-1]}}</li>//n从1开始
</ul>

data:{
	name:['1','2','3'],
}
```  

```
<ul>
<li v-for = "n in names">{{n.name}}</li>//n从1开始
</ul>

data:{
	names:[
		{name:1},
		{name:2},
		{name:3}
		],
}
```  
#### `v-on`  
事件监听，一般有v-on:click,v-on:keyup.enter(识别键入字符)    
```
<td v-show=status[b-1] v-on:click="layerAlert(b_count[b-1])">分配</td>  

<div v-on:keyup.enter="uplogin()"></div>
```   

```
methods:{
	layerAlert:function(index){
		xxx
	},
	uplogin:function(){
		
	}
}
```  
#### `v-bind`  
*v-bind:xx ≈ $().attr("xx")*
```
<p v-bind:class="{onc:isclick}"></p>
```  

```
data: {
			isclick: true,//表示当isclick的值为true的时候，p增加一个叫onc的class
		},
```  

```
<input v-bind:id="grd_msg" v-bind:clsmsg="grd_msg" v-bind:value="grd" />
```  

```
效果为  
<input id = "grd_msg" clsmsg = "grd_msg" value = "grd" />
```  
 