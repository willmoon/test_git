------------------Git Tips-------------

1.git config --list :查看config信息

2.git add . :把所有刚刚修改过或新增的档案一次Add到stage状态

3.git commit -m "" :提交stage中内容，保存“”中德commit 信息
  git commit --amend -m "" :可修改上次提交的消息

4.git log :查看commit记录
   git log -p ：可以看到更详细的内容
 

5.配置.gitignore文件可以忽略某些内容.
建议在repository的初始阶段就配置.gitignore文件
否则当你想忽略那些你已经track的内容时，再修改.gitignore时，
git 不会忽略.此时你得通过命令先把相应要过滤的目录
的缓存删除。具体如下：
git rm --cached <文件名> 删除文件的缓存
git rm --cached -r <目录名> 删除目录下的所有文件的缓存
 

6.一般的过滤条件：
 bin/：过滤所有bin文件夹
 obj/：过滤所有的obj文件夹
 *.log：过滤所有的.log文件
 ！important.log：取反不会过滤此log文件
 
 具体可参考：
 
 http://www.cnblogs.com/wugang/archive/2013/05/23/3094748.html
 
 http://www.zoneself.org/2012/11/16/content_2003.html

7. 在bash 中输入 git --all &可以让gitk在后台执行，可以直观查看各branch的关系
   git branch ：列出所有的branch，带*的为当前branch
   git branch branchname :新建名为branchname的branch
   git checkout branchname :切换到名为branchname的分支
   
8. git reset 可以把已stage的文件、已提交的commit或是已合并的branch进行取消操作
   git reset HEAD <file> ：取消加入stage的file
   git reset --hard HEAD^ ：放弃修改回到上一次commit的位置
   git reset --hard HEAD~2:则是再上一个，依次类推
   git reset --soft HEAD^:会把这次修改加入stage
   git reset HEAD^ :会保留修改不会加入stage
   加上hard 会把修改删除
   
   关于 branch 、git reset 、git merge 和 git rebase,和发生conflict时操作可参考：

   http://blog.gogojimmy.net/2012/01/21/how-to-use-git-2-basic-usage-and-worflow/

   http://blog.csdn.net/jackystudio/article/details/12271811
   
 9.git push 和git pull参考：
 
 http://blog.csdn.net/jackystudio/article/details/12309531
 


 
 以上主要来自于：
 
 http://blog.csdn.net/column/details/jacky-git.html?&page=2
 
 http://blog.gogojimmy.net/2012/02/29/git-scenario/

 感谢。 
   
   
