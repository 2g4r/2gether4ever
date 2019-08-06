**module.exports:{msg:msg}**  模块入口  
**require('./b').msg**  模块出口  
**webpack a.js dundle.js** 将a.js打包为dundle.js  
**webpack.config.js中**  
```
module.exports= {
	entry:'./a',//入口文件
	output:{
		filename:" ",//出口文件  
		path:_dingame//当前文件目录
	}
}
```  