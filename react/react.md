# React.js 环境配置（快速版）
编辑器：vscode

### 1.下载并安装 node.js
http://nodejs.cn/download/  
下载安装包后，一直点下去就可以了

### 2.查看电脑是否安装成功以及安装的版本信息  
1. windows：win+R 输入cmd 打开命令提示符
mac：打开终端
2. 分别输入代码
    ```
    npm -v
    node -v
    ```
    若均输出版本信息，则代表安装成功

### 3.安装**create-react-app**生成器
在命令提示符或者终端中输入
```
npm install -g create-react-app
```
等待安装完成

### 4.若上步安装出错则尝试以下方法，否则跳过
报错：  
```
rollbackFailedOptional: verb npm-session ....
```
解决方法：  
1、**更改npm源**  
命令提示符输入  
```
npm config set registry https://registry.npm.taobao.org
```
验证
```
npm config get registry
```
2、如若不行 查看更多操作
https://www.jianshu.com/p/c5acae8549bd

配置完成后，重复第3步操作

### 5.新建项目
```
create-react-app my-app
```
注意：记得先处理好路径

### 6.运行程序
```
//进入到my-app文件夹
cd my-app
//运行
npm start

```
### 7.安装谷歌调试插件
在**VSCode** 扩展中 搜索 **Debugger for Chrome** 安装
然后打开刚才新建的项目 按**F5**运行  此时会弹出选择运行环境  选择**Chrome**  会生成配置文件**launch.json**
修改**launch.json**文件中的配置
把
```  
"url": "http://localhost:3003"   
```
中的端口号改为 npm start 以后输出的端口号
``` 
Compiled successfully!

You can now view my-app in the browser.

Local:            http://localhost:3000/
```
保存即可，再次按**F5**可启动调试
### 8.React Devtools 调试工具安装
下载地址：
https://github.com/facebook/react-devtools  

下载，并解压文件夹

### 9.打开命令行或是终端 
进入解压好的文件夹，
`` 

``