# SVN遇见的问题    

## warning: empty strings as pathspecs will be made invalid in upcoming release
### svn提交代码时，文件夹内有本地.git仓库和.gitattribute文件，出现上面的报错
### 文件夹内删除.git文件夹'rm -rf .git'，删除.gitattribute文件'rm .gitattribute'，而后'svn del (相关文件/文件夹)'

## svn: E200009: is not under version control
### 'svn st'输出 '? .'，ci显示'is not under version control',无版本控制权限
### bash输入'svn add .'，将文件夹'.'内全部文件加入svn控制中，而后'svn st'查看状态


## svn: E200009: '项目名/图片文件夹名/btn@2x.png': a peg revision is not allowed here
### 在使用「svn status|grep ! |awk '{print $2}'|xargs svn del」批量删除svn文件时，出现上面的错误，而且图片的数量较多
### 对于少量的图片文件，使用'svn resolved 项目名/图片文件夹名/btn@2x.png@'，svn resolved path/ resource @，对于我上面遇到的问题，在这里直接使用'svn del path/'则更为方便

