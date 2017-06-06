## 将本地代码上传到github上
1. 在本地文件夹内生成git仓库，
git init

2. 将所有文件加入仓库中
git add .

3. commit文件
git commit -m '提交目的'

4. 在github上面创建相应的项目/仓库，得到相应的提交地址，例如：https://github.com/liaoting0725/ErrorOrNotice

5. 在本地文件夹内clone远程
git clone https://github.com/liaoting0725/ErrorOrNotice

6. 在本地pull远程代码
git pull origin master
可能会出现'fatal: refusing to merge unrelated histories'
使用
git pull origin master --allow-unrelated-histories
解决上面的问题
7. 将代码推入github中
git push -u origin master 




