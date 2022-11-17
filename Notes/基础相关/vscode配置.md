## vscode中文设置
  * ctrl+shift+p
  * 搜索 configure display language
  * 选择中文即可
## vscode配置Git
  * 安装好Git(安装步骤:https://github.com/liu53dui/Notes/blob/master/Notes/%E5%9F%BA%E7%A1%80%E7%9B%B8%E5%85%B3/git%E5%85%A8%E5%AE%B6%E6%A1%B6.md)
  * 可以在桌面右键git bash here输入git -v查看是否安装好，进行基础的用户名还有邮箱的设置(上面的笔记里也有)，可以使用 git config --list进行查看
  * 新添加sshkey进GitHub账号(保姆教程：https://zhuanlan.zhihu.com/p/576368060)
  * 进入vscode，点击设置->输入shell window->setting.json
  ```
  {
    "workbench.colorTheme": "Default Dark+",
    "terminal.integrated.profiles.windows": {

        "PowerShell": {
            "source": "PowerShell",
            "icon": "terminal-powershell"
        },
        "Command Prompt": {
            "path": [
                "${env:windir}\\Sysnative\\cmd.exe",
                "${env:windir}\\System32\\cmd.exe"
            ],
            "args": [],
            "icon": "terminal-cmd"
        },
        "Git Bash": {
            // "source": "Git Bash"
            "path":"D:\\Git\\bin\\bash.exe"//git的安装路径
        }
    },
    "terminal.integrated.defaultProfile.windows":"Git Bash"
  }
  ```
  为了使用左侧的第三个快捷git操作我们需要配置git的打开路径
  ```
  设置->输入git.path->把上面一样的git启动的地址配置进去就好，重启之后就可以是用左侧的快捷操作
  ```
  * vscode与仓库链接
    这里我专门用了一个文件夹来放git上的代码，在文件中使用git bash来进行一个init的操作 git init(当前建立的为git的代码库) 这时候如果没有仓库的话可以新建一个远程仓库，如果有仓库的话直接使用 git clone [仓库地址]