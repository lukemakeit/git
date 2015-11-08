work space:是当前的文件夹，就是正在编辑的东西的文件夹；  
stage area:是指git add过的；  
reposity；是指git commit过的；
##windows  
在git bash中直接使用FC <file1> <file2>
###linux

使用 git diff   
git diff 还可以比较**提交的**两个版本的不同:git diff <ID1> <ID2>  
如果直接比较两个文件的话使用：git diff（现在比较的是work space 和 stage area中的所有文件）
git diff <file1> 就是比较work space 和 stage area中的文件file1；  
如果是比较stage area和reposity中的file1，使用:git diff --staged   

git log：查看历史提交记录  
git reset --hard <ID的前7位> 回到某个提交历史。  
![git_rest](git_reset.png)  
此时你再用vim去打开文件来看，全部都回到了以前你需要的版本。**（不过这种操作有一个问题，就是回去的时候会把你对所有文件的修改都倒回去）**  
这看起来我们是丢掉了我们第二次的提交，没有办法找回来了。但是 reflog 就是用来解决这个问题的。简单的说，它会记录所有HEAD的历史，也就是说当你做 reset，checkout等操作的时候，这些操作会被记录在reflog中。   
$git reflog  
![git_reset2](git_reset2.png)  
查看所有分支：git branch  
创建新分支：git branch <new_branch_name>  
切换到分支：git checkout <branch_name>
