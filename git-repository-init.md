# git本地仓库初始化以及gitbub远程仓库连接   

 
* 下载安装包安装 
* 配置用户名与邮箱
```
git config --global user.name **
git config --global user.email *@qq.com
// 查看配置是否成功
git cofig --list
```
* 生成公钥私钥
```
ssh-keygen -t rsa -C "*@qq.com"
// 默认公钥私钥保存位置 C:\Users\Administrator\.ssh
```
* github 配置公钥并建立远程仓库(远程仓库名-- remote-test)

* 初始化本地仓库建立提交内容
```
git init
git add .
git commit -m "提交备注"
```
* 关联本地与远程仓库并提交修改
```
// 建立本地仓库与远程仓库关联
git remote add origin git@github.com:penghuolong/remote-test.git
// 如果远程仓库已经存在，删除远程仓库
git remote rm origin
// 建立本地分支的远程追踪分支关系
git branch --set-upstream-to=origin/master master
// 查看本地与远程分支关联
git branch -vv
// 更新本地与远程差异
git pull --rebase
// 提交代码
git push -u origin master
```





