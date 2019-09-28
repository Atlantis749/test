### git 安装
下载地址：https://git-scm.com/downloads

一直点下一步，安装完成点击鼠标右键菜单栏，点击git bush here,输入git --version命令查看版本号 安装完成。
### git 介绍

# 结构：
 工作库 暂存区 本地库 
## 代码托管中心的任务：维护远程库
# 局域网环境下
 GitLab
# 外网环境下
 GitHub
 码云

 ### Git命令行操作
1.本地仓库初始化
    命令： git init
2.设置签名
    用户名：随意
    Elmail 地址：随意（区分不同开发人员身份）
    git config user.name xxx
    git config user.email xxx         (项目级别)
    cat .git/config（查看用户）
    git config --globaluser.name xxx
    git config user.email xxx         (系统级别 通常使用) 
    cat ~/.gitconfig（查看用户）

3.提交本地仓库
    git status 查看工作区状态
    git add xxx 放置暂存区
    git rm --cached xxx 移出暂存区
    git commit xxx -m '本次提交说明'   提交保留区 
4.前进后退
    基于索引值操作【推荐】
        git reset --hard [局部索引值]
        例如 git reset --hard 6aace91
    使用^符号：只能往后不能往前
        git reset --hard HEAD^
        注：一个^表示后退一步 n个表示后退n步
    使用~符号： 只能后退不能前进
        git reset --hard HEAD~n
        注: 表示后退n步
5.reset命令的三个参数对比
    --soft参数
        仅仅在本地库移动HEAD指针
    --mixed参数
        在本地库移动HEAD指针
        重置暂存区
    --hard
        在本地库移动HEAD指正
        重置暂存区
        重置工作区
6.删除文件并找回
    前提： 删除前，文件存在时的状态提交到本地库
    操作： git reset --hard[指针位置]
        删除操作已经提交到本地库：指针位置指向历史记录
        删除操作尚未提交到本地仓库：指针位置使用HEAD
7.比较文件差异
    git diff[文件名]
        将工作区中的文件和暂存区进行比较
    git diff[本地库中历史版本][文件名]
        将工作区的文件和本地库历史记录比较
    不带文件名比较多个文件
### 使用GitHub托管项目
    1.查看地址别名 git remote -v
        https//github.com/xxx(fetch) 拉取地址
        https//github.com/xxx(push) 上传地址
    2.设置地址别名 git remote add origin https//github.com/xxx
    3.推送 git push origin master
    4.克隆远程库 git clone https://github/xxx
        4.1 完整的把远程库下载到本地
        4.2 创建origin远程地址别名
        4.3 初始化本地库
### 拉取
    pull = fetch+merge
    git fetch[远程库地址别名][远程库分支名]
    git merge[远程库地址别名/远程库远程库分支名]
### 
         

