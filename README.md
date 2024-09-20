<p align="center">
    <h1 align="center">Scoop Bucket</h1>
</p>
<p align="center">
### SCOOP介绍

Scoop**是一款适用于Windows平台的命令行软件（包）管理工具**。 简单来说，就是可以通过命令行工具（PowerShell、CMD等）实现软件（包）的安装管理等需求，通过简单的一行代码实现软件的下载、安装、卸载、更新等操作。

Scoop bucket **就是一个软件仓库**,提供windows渗透测试环境工具进行快捷安装、管理和自动更新。
### 软件自动更新

这个仓库已经添加 github ci 自动化，每隔几个小时会自动更新所有软件到最新版本

使用者可以自行在系统中加个定时任务，这样就能自动更新 scoop 软件了，当然也可以手工更新

### scoop基础使用

官网安装说明书： [ScoopInstaller](https://github.com/ScoopInstaller)

1. 先决条件

   - [PowerShell](https://aka.ms/powershell)最新版本或[Windows PowerShell 5.1](https://aka.ms/wmf5download)

2. PowerShell执行策略：

   ```
   Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
   ```

3. 下载安装脚本,在Powershell中执行以下命令

   ```
   irm get.scoop.sh -outfile 'install.ps1'
   ```

4. 管理员执行安装脚本

   ```
   .\install.ps1 -RunAsAdmin -ScoopDir 'D:\Base' -ScoopGlobalDir 'D:\Global' -NoProxy
   ```

   其中`-RunAsAdmin`是使用管理员角色执行脚本，`-ScoopDir`指定scoop安装目录，软件默认安装在此。 `-ScoopGlobalDir`指定全局程序安装到自定义目录。
    ### 安装该软件仓库中的软件
确保你已经有 Scoop 环境后，执行以下命令订阅本软件仓库：
   ```powershell
   scoop bucket add ar https://github.com/tongtong-bob/303
   ```
   执行以下命令安装本仓库中的软件：
   ```powershell
   scoop install ar/<软件名> -g
   ```

## 现有适配软件
| 软件                            | 描述                                                         | 官网地址                                                     |
| :------------------------------ | :----------------------------------------------------------- | :----------------------------------------------------------- |
| scoop install Advanced-SQL-Cheatsheet -g | A cheat sheet that contains advanced queries for SQL Injection of all types..(Scoop bucket by arch3rpro) | <https://github.com/kleiton0x00/Advanced-SQL-Injection-Cheatsheet> |
| scoop install oneforall -g | OneForAll是一款功能强大的子域收集工具 | <https://github.com/shmilylty/OneForAll> |
| scoop install yakit -g | 交互式应用安全测试平台 - Cyber Security ALL-IN-ONE Platform. | <https://www.yaklang.io> |
| scoop install kscan -g | Kscan是一款纯go开发的全方位扫描器，具备端口扫描、协议检测、指纹识别，暴力破解等功能。支持协议1200+，协议指纹10000+，应用指纹2000+，暴力破解协议10余种。 | <https://github.com/lcvvvv/kscan> |
| scoop install gogo -g | 面向红队的, 高度可控可拓展的自动化引擎(Scoop bucket for Cybersecurity by whoopscs) | <https://github.com/chainreactors/gogo> |
| scoop install fscan -g | 一款内网综合扫描工具，方便一键自动化、全方位漏扫扫描。 | <https://github.com/shadow1ng/fscan> |
| scoop install afrog -g | afrog 是一款性能卓越、快速稳定、PoC 可定制化的漏洞扫描工具 - A tool for finding vulnerabilities. | <https://github.com/zan8in/afrog> |
| scoop install goby -g | 新一代网络安全技术，通过为目标建立完整的资产数据库，实现快速的安全应急 | <https://gobysec.net/> |
| scoop install antsword -g | 中国蚁剑是一款跨平台的开源网站管理工具. | <https://github.com/AntSwordProject/AntSword-Loader> |
| scoop install godzilla -g | 哥斯拉 | <https://github.com/BeichenDream/Godzilla> |
| scoop install fuzzDicts -g | Web Pentesting Fuzz 字典,一个就够了. | <https://github.com/TheKingOfDuck/fuzzDicts> |
