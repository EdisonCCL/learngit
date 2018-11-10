Git is a distributed version contral systerm.
Git is a free software distributed under GPL.
ccl is a writer.

#新建本地库
git init
git add filename
git commit -m 'description'
git remote add origin 
git push -u origin master
git push origin master
#当对远程库进行了在线修改 因为本地库与远程库不一致 没更新 所以需要先拉下来 再上传
#这条指令的意思是把远程库中的更新合并到本地库中，
#–rebase的作用是取消掉本地库中刚刚的commit，并把他们接到更新后的版本库之中。
git pull --rebase origin master