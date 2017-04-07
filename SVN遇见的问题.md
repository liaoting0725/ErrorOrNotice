# SVN遇见的问题    

## warning: empty strings as pathspecs will be made invalid in upcoming release
### svn提交代码时，文件夹内有本地.git仓库和.gitattribute文件，出现上面的报错
### 文件夹内删除.git文件夹'rm -rf .git'，删除.gitattribute文件'rm .gitattribute'，而后'svn del (相关文件/文件夹)'

## svn: E200009: is not under version control
### 'svn st'输出 '? .'，ci显示'is not under version control',无版本控制权限
### bash输入'svn add .'，将文件夹'.'内全部文件加入svn控制中，而后'svn st'查看状态


