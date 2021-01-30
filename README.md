```
】项目文件中新建.gitignore:

】git init:

】git add . (提交所有代码)    或      git add demo.html（提交指定代码）
：提交代码至暂存区
】git commit -m 测试上传代码
：提交代码至 git 仓库
】git status
：查看项目当前状态
】git log
：提交记录
    git log --author=''(查看指定修改人)

】配置用户名和邮箱：
git config --global user.name 'YSF'
git config --global user.email '1917689528@qq.com'
git config --global --list （查看已配置项）

】删除文件：
手动删除 -> git add .
命令行：git rm demo3.html

】重命名文件：
手动：新建 new.html -> 删除 old.html ->git add .
命令行：git rm new.html old.html

】移动文件到其他位置：
git mv demo.html home
git mv demo.html home/home.html  (移动并重命名)

】文件有变化时查看文件前后文件
git log --pretty=oneline home/home.html    获取到 id
git show id
git log -p home/home.html   查看具体修改内容

】操作失误情况下一键还原：
只提交到了暂存区
git checkout -- home/home.html  （撤回到上一次提交状态）
提交至暂存区，git 仓库（需要撤销追踪）
git reset HEAD home/home.html
git checkout -- home/home.html 

】回到项目上一版本或指定版本
git reset --hard "HEAD^"  （window系统原因，加了引号）
git reset --hard 指定版本id (id前几位即可)

】将某一文件回退到指定版本
git checkout 指定版本id -- version.html

】修改内容后修改至远程仓库
git push origin master

】为每个版本创建一个独特标签，做所有版本标签管理

】切换、删除分支
git branch  dev 创建分支 dev
git branch 查看所有分支
git checkout test 切换到 test 分支
git branch -d dev 删除 dev 分支
git branch -D test 强制删除 test 分支

】合并分支
git checkout master  切换至 master 分支
git merge dev  合并 dev 分支至 master

】解决合并分支时的冲突
git merge -abort  忽略其他分支内容，保留原分支代码
手动删除：

```