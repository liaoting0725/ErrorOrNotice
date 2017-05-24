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

## URL XXX refers to a file, not a directory
### svn单独checkout某个文件，而不是文件夹，如果使用普通的svn co path命令，会出现上面的提示
### 解决办法，将此文件上级文件夹如何同步到本地，而后使用svn up命令。比如SVN文件路径是：https://path1/path2/path3/file.xlsx,使用命令'svn co --depth=empty  https://path1/path2/path3 path3_new',path3_new为创建的本地文件夹名称，而后'cd path3_new','svn up file.xlsx'可以将此文件单独co到本地


