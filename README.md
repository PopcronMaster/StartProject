# StartProject
初入职场不比紧张，git不熟？从这里开始。

此篇从场景触发，带你应对入门难题。



##### 1.老大把你加入了组织，丢了个地址给你，让你先把代码拉下来，怎么做？

![1567212156217](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1567212156217.png)

点击地址，进入到你要拉的项目目录，找到右边绿色的**Clone or download**，点击复制地址

在自己电脑磁盘合适位置右键选择**Git Bash Here**

![1567212798190](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1567212798190.png)

在黑框中输入命令 **git clone** ,右键粘贴刚刚复制的内容

![1567213019961](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1567213019961.png)

回车后，就会自动拉取到远端仓库的主分支的代码，任务完成



##### 2.老大让你建一个自己的分支，以后你就在你的分支开发，怎么做

进入到本地项目目录，右键**Git Bash Here**，先查看分支

```
# 查看本地分支
git branch

# 查看本地和远端分支
git branch -a
```

![1567213523658](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1567213523658.png)

现在开始，新建分支

```
# 切换分支，若不存在就新建 
git checkout -b  分支名
```

![1567213741832](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1567213741832.png)

可以看到已经在本地新建了一个**master-dev-testing**的分支了，并切换到这个分支了，但你细心点就会发现红色的远端分支并没有testing分支，那么别人是看不到这个分支的，那么怎么让远端和自己本地分支同步呢，推送上去就可以了

```
git push origin 分支名
```

![1567214164866](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1567214164866.png)



##### 3.你写了代码，现在需要提交，然后推送到远端，怎么做

```
# 查看当前状态,包括本地工作区情况，当前所在分支，本地仓库与远端仓库进度说明等
git status

# 一定要先切换到自己的开发分支
git checkout master-dev-testing

# 将本地修改保存，提交到本地仓库，并添加说明
git add .
git commit -m '修改说明'
```

这样只是在本地保存了，接着是推送到远端

```
git push origin master-dev-testing
```

这样就是一次代码修改过程了



##### 4.当多个人一起开发时，可能需要合并代码，怎么做？