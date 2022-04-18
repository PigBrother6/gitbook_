# git原理

- ### 三个概念 blob tree commit 

  三者都是.git的object

  ```
  blob 存储文件数据 
  
  tree 存储文件名，指向上一个tree的指针，指向blob的指针等
  
  commit存储committer，commit的描述信息，指向tree的指针，指向parental commit的指针等
  ```

- #### 什么时候生成这三个object

  git add . 的时候会生成blob

  git commit -- m 的时候生成 tree 和 commit对象

- #### SHA1值是关键

  当有100个文件，文件内容完全一样时，blob只记录一份，tree里存储的SHA1值不变。

  SHA1值，哈希值。数据不变，一定不变；数据改变，SHA1值一定改变。

- #### commit对象的重点理解

  commit存储的快照是两个指针：一个指向parental commit；另一个指向当前的tree

------

- ### branch

  ##### refs三件套：HEAD branch Tag

  ##### refs与commit紧密相关

  ##### merge时commit是怎么移动的

  ```
  1. fast-forword
  由于dev是比mater走得更前，所以git commit的时候commit的SHA1值就是当前dev分支的SHA1值
  2. no-fast-forword
  无论有没有冲突，dev和mater都在引出分支时有了改变，所以merge时commit会生成新的SHA1值
  
  ```

------

- ### 其他知识

  - 三个区与remote仓库的理解
  - 本电脑github与本地的联系怎么创建
  - git pull 与git fetch + merge 的区别
  - merge时为什么会有conflict
  - merge与rebase的区别
  - commit移动的图（要记得）