git add .
git commit -m "说明文档"
git reset --hard HEAD^ 
git status //查看状态
git checkout -- test.txt //还原版本
git diff HEAD -- readme.txt //查看区别
git log //版本id
git reflog //操作id
git reset --hard ID
git rm test.txt //删除
git remote add origin ssh地址 //绑定github仓库
git push -u origin master //上传代码 git master github main
git remote -v
