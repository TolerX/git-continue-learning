# git-continue-learning
>continue learning some commands about git

# 撤销一次提交
>撤销一次提交可以用这种方式但是，但是得确保你提交了以后没有没有再次提交
 git reset --hard HEAD~1 //仅还原一次提交
 git push --force //像坦克一样，把其他的提交都给弄掉


#撤销中间的提交
> 如果推送到远程了，其他人也提交了，那么这时候我们就不能按照上面的方法了，我们需要用如下命令
  git rebase -i 2a9442^ //2a9442就是想删除的远程提交
  我们会看到有好几个pick出来的，把最上面的直接删除就好了
  pick 2a9442 //删除这行
  pick ds98dhj278
  ...
  然后git push -f //像推土机一样强制push到远程


