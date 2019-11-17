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
#### 在matchvs 中注册用户时，返回的用户头像在线地址，使用的时候出现跨域问题
[参考：Egret 白鹭跨域问题](https://blog.csdn.net/rickshaozhiheng/article/details/79611712)  
解决方法：  
1.  在`.Wing/launch.json`中给 chrome的配置加上 --disable-web-security 也就会忽略跨域的安全行问题(在同样基于VSCode的LayaAir中也有用)  
问题是，这个仅在egret wing中调试时有用，出了这个编辑器就没啥用了
``` 
"runtimeArgs": [
	"--allow-file-access-from-files",
	"--allow-file-access-frome-files",
	"--disable-web-security"
]
```
2. 我的游戏是用canvas渲染的，直接在`index.html`中将默认的`webgl`改为`canvas`  暂时解决了问题  


#### 把游戏发布后，发现生成的`index.html`中的`webgl`并没有被修改
解决方法：  
再手动修改一次

#### 发布后的游戏，上传到github，使用github.io来访问页面，出现跨域问题，大致是https请求不能发送到ws那边？要用wss之类的  
解决方法：  
把matchSDK 中的`IsWss`的值改为`true`就可以了，但是生成后仍然没有被修改，依然手动修改一次  
基本没问题了，可以使用github page 多端登录 并加入房间
