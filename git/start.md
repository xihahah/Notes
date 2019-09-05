# 上传项目到github仓库的简单步骤
1. github 新建一个仓库

2. 在本地的项目文件夹中，初始化
    ```
    git init
    ```

3. 关联远程仓库，在github仓库中复制http/ssh地址
    ```
    git remote add [自定仓库名] [http/ssh地址]
    git remote add origin git@github.com:xihahah/Notes.git
    ```

4. 项目中添加所有文件（也可只添加指定文件）
    ```
    git add .
    ```

5. 提交并填写提交信息
    ```
    git commit -m "初始提交"
    ```

6. 推送到远程仓库
    ```
    git push [自定的仓库名] [分支名]
    git push origin master
    ```

# github page的使用
1. 完成主支的推送后，新建一个 gh-pages 分支
    ```
    git checkout -b gh-pages
    ```

2. 把主支的代码推送一份到 gh-pages 分支（前面已经提交了）
    ```
    git push origin gh-pages
    ```

3. 访问地址 ``https://[github用户名].github.io/[仓库名]/[html名.html] ``即可查看  
默认访问的是index.html 可以只输``https://[github用户名].github.io/[仓库名] ``