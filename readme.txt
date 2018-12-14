Git is a distributed version contral systerm.
Git is a free software distributed under GPL.
ccl is a writer.
#创建git用户
git config --global user.email '1******@***.com'
git config --global user.name '***'

#新建本地库
git init
#保存到本地库
git add filename
git commit -m 'description'
#第一次连远程库需要前两条语句 之后都第三条语句直接传
git remote add origin git@github.com:EdisonCCL/learngit.git
git push -u origin master
git push origin master
#当对远程库进行了在线修改 因为本地库与远程库不一致 没更新 所以需要先拉下来 再上传
#这条指令的意思是把远程库中的更新合并到本地库中，
#–rebase的作用是取消掉本地库中刚刚的commit，并把他们接到更新后的版本库之中。
git pull --rebase origin master

#提示：fatal: refusing to merge unrelated histories
git pull origin master --allow-unrelated-histories

#提示：fatel: git remote origin already exist
git remote rm origin
