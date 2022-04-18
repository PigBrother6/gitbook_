### git 常用命令

```markdown
1. git init 初始化（生成.git文件）
2. git status 查看文件状态（红色表示未被加进缓存区或已被修改，绿色代表已进入缓存）
3. git add '文件名' or git add . （.代表当前目录的所有文件）  将文件加载进缓存区
4. git commit -m '自拟版本信息'  将文件从缓冲区加载进版本库

## 版本回滚
### 回滚到之前版本
5. git log 查看版本信息
6. git reset --hard 版本号  回滚到之前版本

### 回滚到之后版本
7. git reflog 查看所有版本信息
8. git reset --hard 版本号  回滚到之后版本

```



- ##### 查看分支

```
git branch
```

- ###### 创建分支

```
git branch 分支名称
```

- 切换分支

```
git checkout 分支名称
```

- 分支合并

```
git merge 要合并的分支
注意：切换分支再合并
```

- 删除分支

````
git branch -d 分支名称
````



