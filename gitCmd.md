1、初始化本地仓库
git init

2、将文件添加到暂存区
git add 文件名

3、查看暂存区状态
git status/git status 文件名 

4、将文件提交到git本地库
git commit -m '本地库文件记录名称'
（文件提交到本地库之前一定要先提交到暂存区，否则操作无效）

5、查看提交本地库操作日志
git log

6、更直观看版本
git log -行数 --pretty=oneline

7、撤销暂存区文件
git reset HEAD / git reset HEAD 暂存区文件名

8、输出工作区内容
cat 文件名



时光穿梭机
1、回退一个版本
git reset --hard HEAD^

2、回退两个版本
git reset --hard HEAD^^

3、回退多个版本
git reset --hard HEAD~回退数（number）

4、前进到某个版本
git reset --hard 版本唯一标识符
（ git log后第一行commit：加密字符 就是版本唯一标识符 ）
（版本标识不用全部输完，只要保证唯一性就行，不与其他版本标识重复即可）

5、查看历史操作记录（版本标识，执行操作，版本名称）
git reflog

6、恢复已提交本地库 但在工作区删除的文件
git checkout 被删除的文件名

7、永久删除本地仓库里的文件（不会更新版本，无法回退）
git rm 文件名

8、查看本地仓库文件目录
git ls-files


1、远程仓库文件克隆到本地
git clone https地址

2、将本地仓库连接到远程仓库
git remote add 远程仓库别名 远程仓库地址

3、将本地库追加到到远程仓库里
git push -u 远程仓库别名 master(远程仓库分支名)

公钥

1、创建公钥 
ssh-keygen -t rsa -C "w2262281625@163.com"
（创建完，找到相应目录，复制公钥到github/gitee，添加公钥）例：'/c/Users/86182/.ssh'

2、秘钥检查测试连接
ssh -T git@github.com



