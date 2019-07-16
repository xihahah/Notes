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