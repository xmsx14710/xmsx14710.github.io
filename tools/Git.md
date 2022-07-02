# Git

## Git安装

## Git add & commit & reset & log & init


1.设置仓库（需要提前进入需要管理的项目根文件夹）


```
git init 
```


2.进入仓库添加或编写一个文件，把该文件进行版本控制


```
git add <文件名>
```


3.提交文件



```
git commit -m "提交或更改描述"
```



4.查看版本控制记录或文件更改记录


```
git log --pretty=oneline  
```


5.退回或恢复以前版本



```
git reset --hard <版本控制记录中的版本号>
```


6.查看命令记录


```
git reflog
```

1.Clone the repository

```
git clone https://github.com/username/username.github.io
```