### 作者 [日]
**关键字**：
>版本管理、分支、合并、Fork、Issue、BUG管理、任务管理、Markdown、代码审查、社会化编程、Jenkins Github Flow、Git Flow、hub命令...

- 版本管理
  - [ ] 集中型——SVN
  - [x] 分散性——Git

### 分支的操作
<!-- 可以在互不影响前提下对多个功能进行开发 -->
- git branch
    <!-- 查看分支一览表 -->
    - git checkout -b feature-a
    <!-- 创建分支feature-a -->
    - git checkout master
    <!-- - 切换回master分支 -->
- git merge
    <!-- - 分支合并 -->
    - git checkout master
    <!-- - 切换回master分支 -->
    - git merge --no-ff feature-a
    <!-- - 创建合并提交 -->

### 查看日志
- git log
<!-- - 查看以当前状态为终点的历史日志 -->
- git log --graph
<!-- - 以图标形式查看分支 -->
- git reflog
<!-- - 查看当前仓库的操作日志 -->

### 更改提交的操作
- git reset
<!-- - 回溯历史版本,这里通过一个例子回溯到创建feature-a之前创建分支fix-b，再回溯到merge feature-a后的版本 -->

### 消除冲突
- git merge --no-ff fix-b
  - ![](../../source/img/2019-11-24-11-23-50.png)
  - 解决冲突
  - git add
  - git commit
- git commit --amend
- git rebase -i
  - HEAD~2,压缩最近2次提交
  - pick → fixup
- 推送至远程仓库
  - git remote add——添加远程仓库
  - git push
    - -u origin master,推送到master分支
    - -u origin feature-d，推送到master以外的分支
- 从远程仓库获取
  - git clone，获取远程仓库
  - git pull,获取最新的远程仓库分支
### 注意点
- 合并merge和回溯reset都需要回到master分支

### 参考资料
- Pro Git
- LearnGitBranching
- tryGit
- [Git常用指令总结 | Luozm's Blog](https://luozm.github.io/git)