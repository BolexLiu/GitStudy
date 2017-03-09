# git笔记
Git is a version control system
git is free software

---

## 基本命令：
- git init 初始化目录
-  git add ｛文件名称｝ 放入git仓库的暂存区域
- git commit  -m {提交说明} 把文件提交到仓库
- git status 查看提交状态
- git diff 对比改动
- git log 查看提交日志 （--pretty=｛oneline｝ 只看概要）
- git 输入 git log --all 命令后出现<END>标记？按Q退出
 rm ｛文件命｝ 删除文件

---

## 工作区回滚至分支
- git reset --hard ｛版本号｝ 回滚到具体的版本号
- git reset --hard HEAD^ 回滚（^表示上一次 ^^前两次 HEAD~100 前100次）
- git reflog 可以再回滚出错后查看每一次的log 再用reset hard ｛版本号｝可以回滚到指定的版本

##工作区回滚至未修改前（丢去本次工作区的修改）

- git checkout -- file  工作区的修改全部撤销

##暂存区回滚到工作区
- git reset HEAD file 


## 比较
- git diff    #是工作区(work dict)和暂存区(stage)的比较
- git diff --cached    #是暂存区(stage)和分支(master)的比较
- git diff HEAD -- ｛文件名｝  #是工作区(work dict)和分支(master)的比较

##push
- git push -u origin master 将本地库push到远程origin上去 -u表示Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。 
- git push origin master 简化以后:将本地仓库中的代码push至origin

##分支
- git branch ｛分支名称｝ 创建分支
- git checkout ｛分支名称｝ 切换到该分支
- git checkout -b ｛分支名称｝ 创建一个分支并-b切换到该分支
- git branch 查看当前分支
- git merge ｛分支名称｝ 将当前的分支与｛｝中的分支合并
- git branch -d ｛分支名称｝ 删除一个分支
- git log --graph --pretty=oneline --abbrev-commit 擦