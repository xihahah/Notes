# ssh公钥

附上[官方说明](https://git-scm.com/book/zh/v2/服务器上的-Git-生成-SSH-公钥)

1. 查看是否已存在ssh公钥
```
//进入 ~/.ssh 文件夹  如果没有 则进入失败
cd ~/.ssh

//列出该文件夹内的文件
ls
```
2. 查看ssh公钥  
```
进入C:\Users\ASUS\.ssh
记事本打开 id_rsa.pub
```

3. 生成ssh公钥
```
ssh-keygen
```