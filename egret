# egret引擎链接matchvs出现的问题
1.egret创建的项目中没有添加socket模块，导致使用matchvs登录时出现问题`egret.WebSocket is not a construtor`  
解决方法：  
在egret中添加socket模块，具体操作：

在配置文件 egretProperties.json 中添加
```
{
      "name": "socket"
}
```
然后执行 `egret build -e` 命令，在项目所在目录内执行一次引擎编译
