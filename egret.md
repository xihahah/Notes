### egret引擎连接matchvs出现的问题
egret创建的项目中没有添加socket模块，导致使用matchvs登录时出现问题`egret.WebSocket is not a construtor`  
解决方法：  
在egret中添加socket模块，具体操作：

在配置文件 egretProperties.json 中添加
```
{
      "name": "socket"
}
```
然后执行 `egret build -e` 命令，在项目所在目录内执行一次引擎编译

### 跨域问题
在matchvs 中注册用户时，返回的用户头像在线地址，使用的时候出现跨域问题  
解决方法：  
在`.Wing/launch.json`中给 chrome的配置加上 --disable-web-security 也就会忽略跨域的安全行问题(在同样基于VSCode的LayaAir中也有用)
``` 
"runtimeArgs": [
	"--allow-file-access-from-files",
	"--allow-file-access-frome-files",
	"--disable-web-security"
]
```
[参考：Egret 白鹭跨域问题](https://blog.csdn.net/rickshaozhiheng/article/details/79611712)
