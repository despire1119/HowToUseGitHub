## gitlab 开发对接小tip

- 目前前端代码的交付方式已由SVN切换为git，开发人员需要下载并安装一个git工具才能获取到前端项目代码。
- <a href="http://10.24.10.51/Git-1.9.4.exe" target="_blank">[点击下载Git]</a>, 一次安装永久有效。
- 下载安装后，在本地要存放前端代码的目录下，右击执行git bash，
- 然后输入以下命令即可检出项目代码仓库：git clone 项目仓库地址,其中只用到build目录下的文件,其他文件不用管.
- 修改对比查看，可直接在浏览器打开仓库地址，然后左侧点Commits菜单
- 注：新项目检出命令：git clone [项目仓库地址]；已有项目更新命令直接执行：git pull

----

## gitlab苏宁易购前端代码托管平台使用须知(前端人员)

### 1.平台地址：http://fed.cnsuning.com
  - 用户名: 姓名拼音，初始密码为：工号，登入后在个人工作台可以修改用户名和密码，还可以添加个人rsa_pub公钥
  - 查看所有仓库地址：`http://fed.cnsuning.com/explore/projects`
  - 新建仓库点点击右上角+
  - 项目首页找到：+add project member 可添加项目成员，权限为：`developer`

### 2.提交代码需安装git客户端，
  - 命令行客户端下载地址：`http://10.24.10.51/Git-1.9.4.exe`
  - GUI式客户端建议`sourceTree`或`TortoiseGit`，请自行下载。

### 3.使用平台提交代码需设置本地git账户为平台标识用户
依次在git命令行模式执行以下语句（后两句修改成个人信息）

    git config --global --unset user.name
    git config --global --unset user.email
    git config --global --add user.name "中文姓名"
    git config --global --add user.email "工号八位数@cnsuning.com"

### 4.本地操作
- 建议新建一个根目录级别的目录叫 gitlab，来放来自gitlab平台的所有项目（仓库）。

### 5.平台提供了一个可随意clone commit 并 push的一个仓库为
- clone地址：http://fed.cnsuning.com:9000/qinyuguo/public-test.git
- 预览地址：http://fed.cnsuning.com/qinyuguo/public-test

### 6.推荐git别名设置
    git config --global alias.st status
    git config --global alias.co checkout
    git config --global alias.ci commit
    git config --global alias.br branch
    git config --global alias.last 'log -1'
    git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"

### 7.对git命令不熟悉的，建议尽快恶补
    教程地址：http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/