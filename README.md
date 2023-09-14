# Diudiu

视频地址：https://www.imooc.com/learn/1278
git常用命令
git init //初始化
git add . //提交到缓存区 .代表整个项目 .可以替换项目文件
git commit -m 第一次提交 //提交命令 -m后面提交的时候备注
git status   //查看当前项目的状态
git log  //查看提交记录、commit的ID
git log --author='梁一帆' //查询梁一帆的提交记录
git rm  demo3.html //删除demo3.html项目文件
git mv home.html demo3.html //项目文件重命名 第一个名字是改动之前的，第二个是改动之后的
git mv demo2.html home/home.html //把demo2文件移到home文件夹并重命名
git mv  demo2.html home//把demo2文件移到home文件
git log -p demo.html //查看文件的前后变化 
git diff //找到项目文件的内容和上一次版本的不同
git checkout -- demo.html //回滚上一次版本
git reset HEAD demo.html //项目文件add到了缓存区，实现文件追踪回滚
git reset --hard HEAD^ //把整个项目回滚，一个^号代表回滚到上一个版本，两个^号回滚两个版本
git reset --hard 47123 //把整个项目回滚，47123代表commit的ID，这样就回滚到那次提交的版本
git checkout 47123 -- demo.html//把指定文件回滚到指定版本
git push orgin master //把文件推送到运程仓库 master默认的分支
git tag v1.0  //把一个版本创建一个独特的标签
git tag v2.0 47123 //给指定的commit的ID 创建一个独特的标签
git tag -d v2.0 //把v2.0的标签给删除
git push oragin v1.0 //把标签推送到运程仓库
如何配置git用户名和邮箱
git config --global user.name '梁一帆' //配置用户名
git config --global user.email 'liangyifan1016@163.com'//配置邮件
git config --global --list //查看配置的用户名和邮件
创建、切换、删除分支时的操作
git branch dev //创建分支  创建好了一个dev的分支
git branch //查看分支 master默认的分支
git checkout dev //切换分支 切换到dev的分支
git branch -d dev //删除分支 注意：不能删除当前所在的分支
git checkout -b test //创建分支并切换到test这个分支
git branch -D test //强制删除分支，如果你在当前分支提交了记录，用小写字母d删除不了
git push origin liangyifan-扩能总装安灯设备状态接口 //把分支提交运程仓库 分支名：liangyifan-扩能总装安灯设备状态接口
如何正确的合并分支
git merge dev //把dev分支向默认分支合并
如何解决合并分支的时候起冲突
git merge --abort //忽略其他分支的代码，保留当前的代码
不同人想要查看版本路线如何进行操作
git log --oneline //简单的看所有人的提交记录
git log --oneline --graph //查看版本路线
不同人想要删除不想要的分支如何操作
git push origin --delete summer //summer是分支名字，删除不要的分支 
不同人修改了不同的文件如何处理
git push //把文件推送到运程仓库
git branch -av //查看运程的仓库
git merge origin/test //test是分支名，命令执行之后按I输入备注,然后ESC输入:wp 回车 然后再次重新推送运程仓库即可
不同人修改了相同的文件如何处理
git fetch //从远端拉取分支
从远端拉取分支 提交代码，再次推送运程仓库，这样就实现了不同人修改了相同的文件， 
