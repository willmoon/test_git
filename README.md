------------------Git Tips-------------
1.git config --list :查看config信息
2.git add . :把所有刚刚修改过或新增的档案一次Add到stage状态
3.git commit -m "" :提交stage中内容，保存“”中德commit 信息
4.git log :查看commit记录
   git log -p ：可以看到更详细的内容
 
5.配置.gitignore文件可以忽略某些内容.
建议在repository的初始阶段就配置.gitignore文件
否则当你想忽略那些你已经track的内容时，再修改.gitignore时，
git 不会忽略.此时你得通过命令先把相应要过滤的目录
的缓存删除。具体如下：
git rm --cached <文件名> 删除文件的缓存
git rm --cached -r <目录名> 删除目录下的所有文件的缓存
 
 