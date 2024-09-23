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
   scoop bucket add 303 https://github.com/tongtong-bob/303
   ```
   执行以下命令安装本仓库中的软件：
   ```powershell
   scoop install 303/<软件名> -g
   ```

## 现有适配软件
| 软件                            | 描述                                                         | 官网地址                                                     |
| :------------------------------ | :----------------------------------------------------------- | :----------------------------------------------------------- |
| scoop install ToolsFx -g | 基于kotlin+tornadoFx的跨平台密码学工具箱.包含编解码,编码转换,加解密, 哈希,MAC,签名,大数运算,压缩,二维码功能,ctf等实用功能,支持插件 | <https://github.com/Leon406/ToolsFx> |
| scoop install AlliN -g | A flexible scanner. | <https://github.com/P1-Team/AlliN> |
| scoop install Advanced-SQL-Cheatsheet -g | A cheat sheet that contains advanced queries for SQL Injection of all types.. | <https://github.com/kleiton0x00/Advanced-SQL-Injection-Cheatsheet> |
| scoop install yakit -g | 交互式应用安全测试平台 - Cyber Security ALL-IN-ONE Platform. | <https://www.yaklang.io> |
| scoop install goby -g | 新一代网络安全技术，通过为目标建立完整的资产数据库，实现快速的安全应急 | <https://gobysec.net/> |
| scoop install kscan -g | Kscan是一款纯go开发的全方位扫描器，具备端口扫描、协议检测、指纹识别，暴力破解等功能。支持协议1200+，协议指纹10000+，应用指纹2000+，暴力破解协议10余种。 | <https://github.com/lcvvvv/kscan> |
| scoop install gogo -g | 面向红队的, 高度可控可拓展的自动化引擎 | <https://github.com/chainreactors/gogo> |
| scoop install fscan -g | 一款内网综合扫描工具，方便一键自动化、全方位漏扫扫描。 | <https://github.com/shadow1ng/fscan> |
| scoop install afrog -g | afrog 是一款性能卓越、快速稳定、PoC 可定制化的漏洞扫描工具 - A tool for finding vulnerabilities. | <https://github.com/zan8in/afrog> |
| scoop install Pillager -g | Pillager是一个适用于后渗透期间的信息收集工具，可以收集目标机器上敏感信息，方便下一步渗透工作的进行。 | <https://github.com/qwqdanchun/Pillager> |
| scoop install antsword -g | 中国蚁剑是一款跨平台的开源网站管理工具. | <https://github.com/AntSwordProject/AntSword-Loader> |
| scoop install godzilla -g | 哥斯拉 | <https://github.com/BeichenDream/Godzilla> |
| scoop install CDK -g | CDK是一款为容器环境定制的渗透测试工具，在已攻陷的容器内部提供零依赖的常用命令及PoC/EXP。集成Docker/K8s场景特有的 逃逸、横向移动、持久化利用方式，插件化管理。 | <https://github.com/cdk-team/CDK> |
| scoop install AsyncRAT -g | Open-Source Remote Administration Tool For Windows C# (RAT). | <https://github.com/NYAN-x-CAT/AsyncRAT-C-Sharp> |
| scoop install NacosExploitGUI -g | Nacos漏洞利用工具GUI | <https://github.com/charonlight/NacosExploitGUI> |
| scoop install woodpecker -g | 高危漏洞精准检测与深度利用框架 | <https://github.com/woodpecker-framework/woodpecker-framework-release> |
| scoop install RuoYiExploitGUI -g | RuoYi漏洞利用工具GUI | <https://github.com/charonlight/RuoYiExploitGUI> |
| scoop install xxl-jobExploitGUI -g | xxl-job漏洞利用工具GUI | <https://github.com/charonlight/xxl-jobExploitGUI> |
| scoop install JenkinsExploitGUI -g | Jenkins漏洞利用工具GUI | <https://github.com/charonlight/JenkinsExploitGUI> |
| scoop install SpringExploitGUI -g | Spring漏洞利用工具GUI | <https://github.com/charonlight/SpringExploitGUI> |
| scoop install nuclei -g | Fast and customizable vulnerability scanner based on simple YAML based DSL | <https://nuclei.projectdiscovery.io> |
| scoop install struts2vulsscantools -g | 1、点击“检测漏洞”，会自动检测该URL是否存在S2-001、S2-005、S2-009、S2-013、S2-016、S2-019、S2-020/021、S2-032、S2-037、DevMode、S2-045/046、S2-052、S2-048、S2-053、S2-057、S2-061、S2相关log4j2十余种漏洞。  2、“批量验证”，（为防止批量geshell，此功能已经删除，并不再开发）。  3、S2-020、S2-021仅提供漏洞扫描功能，因漏洞利用exp很大几率造成网站访问异常，本程序暂不提供。  4、对于需要登录的页面，请勾选“设置全局Cookie值”，并填好相应的Cookie，程序每次发包都会带上Cookie。  5、作者对不同的struts2漏洞测试语句做了大量修改，执行 | <https://github.com/abc123info/Struts2VulsScanTools> |
| scoop install HostCollisionGUI -g | HostCollision漏洞利用工具GUI | <https://github.com/charonlight/HostCollisionGUI> |
| scoop install pocsuite3 -g | pocsuite3 is an open-sourced remote vulnerability testing framework developed by the Knownsec 404 Team. | <https://github.com/knownsec/pocsuite3/> |
| scoop install quark -g | 夸克网盘 | <https://pan.quark.cn/> |
| scoop install everything-alpha -g | Locate files and folders by name instantly. | <https://www.voidtools.com> |
| scoop install proxifier -g | Allows network applications that do not support working through proxy servers to operate through a SOCKS or HTTPS proxy and chains. | <https://www.proxifier.com> |
| scoop install python-beta -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install spacedrive -g | Spacedrive is an open source cross-platform file explorer, powered by a virtual distributed filesystem written in Rust | <https://github.com/spacedriveapp/spacedrive> |
| scoop install FlowUs -g | null | <https://flowus.cn/download> |
| scoop install wemeet -g | tencent meeting | <https://meeting.tencent.com/index.html> |
| scoop install python-alpha -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install wub -g | wub 彻底关闭Win10自动更新工具(Windows Update Blocker)  | <https://www.sordum.org/downloads/?st-windows-update-blocker> |
| scoop install axure9 -g | Prototypes, Specifications, and Diagrams in One Tool | <https://www.axure.com/> |
| scoop install emeditor -g | EmEditor is a fast, lightweight, yet extensible, easy-to-use text editor for Windows. | <https://www.emeditor.com/> |
| scoop install maye -g | 一个简洁小巧的快速启动工具 | <https://github.com/25H/Maya> |
| scoop install wireshark3 -g | A network protocol analyzer that lets you see what’s happening on your network at a microscopic level. | <https://www.wireshark.org/> |
| scoop install picgo -g | 图片上传和管理工具  | <https://picgo.github.io/PicGo-Doc/> |
| scoop install python311 -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install clash-windows -g | A Windows/macOS GUI based on Clash | <https://github.com/Fndroid/clash_for_windows_pkg> |
| scoop install gda -g | the fastest and most powerful android decompiler(native tool working without Java VM) for the APK, DEX, ODEX, OAT, JAR, AAR, and CLASS file. which supports malicious behavior detection, privacy leaking detection, vulnerability detection, path solving, packer identification, variable tracking, deobfuscation, python&java scripts, device memory extraction, data decryption, and encryption, etc | <https://twitter.com/charles_gan1> |
| scoop install everything-beta -g | Locate files and folders by name instantly. | <https://www.voidtools.com> |
| scoop install python -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install confuserex-cli -g | An open-source, free protector for .NET applications | <https://mkaring.github.io/ConfuserEx/> |
| scoop install wps-ai -g | WPS AI是由金山办公发布的具备大语言模型能力的人工智能应用，为用户提供智能文档写作、阅读理解和问答、智能人机交互的能力。作为WPS办公套件的重要组成部分，WPS AI将与WPS其他产品无缝衔接，让用户在办公、写作、文档处理等方面实现更高效、更智能的体验。 | <https://ai.wps.cn> |
| scoop install caesium -g | Caesium is an image compression software that helps you store, send and share digital pictures, supporting JPG, PNG and WebP formats. | <https://github.com/Lymphatus/caesium-image-compressor/> |
| scoop install python27 -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install easy-context-menu -g | Easy Context Menu (ECM) lets you add a variety of useful commands and tweaks to the Desktop, My Computer, Drives, File and Folder right-click context menus. This enables you to access the most used Windows components quickly and easily. Simply check the box next to the items you wish to add. Once added, just right click and the select the component shortcut to launch it. Easy Context Menu is both portable and freeware. | <https://www.sordum.org/7615/> |
| scoop install python36 -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install ddns-go -g | 简单好用的DDNS。自动更新域名解析到公网IP(支持阿里云、腾讯云dnspod、Cloudflare、华为云、百度云、porkbun) | <https://github.com/jeessy2/ddns-go> |
| scoop install gowitness -g | gowitness - a golang, web screenshot utility using Chrome Headless | <https://github.com/sensepost/gowitness> |
| scoop install extremedumper -g | .NET Assembly Dumper | <https://github.com/wwh1004/ExtremeDumper> |
| scoop install python-pre -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install newfiletime -g | NewFileTime is a Windows tool that provides you easy access to correct or manipulate any of the timestamps for any file and folder on Windows! | <http://www.softwareok.com/?seite=Microsoft/NewFileTime> |
| scoop install MonitorOff -g | MonitorOff (Screen Turns Off) | <https://www.sordum.org/downloads/?st-sordum-monitor-off> |
| scoop install siyuan -g | SiYuan is a local-first personal knowledge management system, support fine-grained block-level reference and Markdown instant-render editing. | <https://github.com/siyuan-note/siyuan> |
| scoop install 7zip -g | A multi-format file archiver with high compression ratios | <https://www.7-zip.org/> |
| scoop install notepad-- -g | 一个支持windows/linux/mac的文本编辑器，目标是要替换notepad++，来自中国。 | <https://github.com/cxasm/notepad--> |
| scoop install pwsh-beta -g | Cross-platform automation and configuration tool/framework, known as Powershell Core, that works well with existing tools and is optimized for dealing with structured data. (beta channel) | <https://github.com/PowerShell/PowerShell> |
| scoop install finalshell -g | 国产软件FinalShell SSH工具,服务器管理,远程桌面加速软件,支持Windows,macOS,Linux | <https://www.hostbuf.com/t/988.html> |
| scoop install zlib -g | Massively spiffy yet delicately unobtrusive compression library. Unencumbered by patents. | <http://www.zlib.net/> |
| scoop install everything-powertoys -g | This plugin adds Everything search results to PowerToys Run. | <https://github.com/lin-ycv/EverythingPowerToys> |
| scoop install filezilla -g | a free, open source, cross-platform FTP software that is offered both as a client and a server. It offers support for FTP, FTPS (it's the FTP over SSL/TLS) and SFTP (SSH file transfer protocol) | <https://filezilla-project.org> |
| scoop install pixpin -g | 功能强大使用简单的截图/贴图工具-snipaste替代品，支持长截图. | <https://pixpinapp.com/> |
| scoop install windows-terminal-preview -g | The new Windows Terminal, and the original Windows console host - all in the same place! (Preview version) | <https://github.com/microsoft/terminal> |
| scoop install sublime-text -g | A sophisticated text editor for code, markup and prose | <https://www.sublimetext.com> |
| scoop install python310 -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install vim -g | A highly configurable text editor | <https://www.vim.org> |
| scoop install everything -g | Locate files and folders by name instantly. | <https://www.voidtools.com> |
| scoop install fab -g | Firewall App Blocker (Fab) 易于使用的Windows防火墙工具  | <https://www.sordum.org/downloads/?firewall-app-blocker> |
| scoop install notepadplusplus -g | A free source code editor and Notepad replacement that supports several languages. | <https://notepad-plus-plus.org> |
| scoop install he3 -g | A Free, Modern Toolbox, Built for Developers | <https://he3.app> |
| scoop install treesize -g | TreeSize纯净版是一款功能强大的磁盘空间管理软件，为用户提供了功能强大的磁盘空间管理功能，帮助更好的管理内存空间，为文件管理提供了帮助。软件已经进行了整体优化，去除了各种无用的功能和界面，满足用户的各种软件纯净版使用需求  | <https://www.jam-software.com/treesize> |
| scoop install python35 -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install python39 -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install everything-beta-np -g | Locate files and folders by name instantly. | <https://www.voidtools.com> |
| scoop install windynamicdesktop -g | Port of macOS Mojave Dynamic Desktop feature to Windows 10 | <https://github.com/t1m0thyj/WinDynamicDesktop> |
| scoop install cpuz-cn -g | System information software | <https://www.cpuid.com/softwares/cpu-z.html> |
| scoop install edx -g | 一款高性能的可扩展编辑器 | <https://www.ed-x.cc/index.html> |
| scoop install git-repo-clean -g | 对Git仓库大文件进行扫描、清理，并重写提交历史的Git拓展工具。 | <https://gitee.com/oschina/git-repo-clean> |
| scoop install rubick -g | Electron based open source toolbox, free integration of rich plug-ins. 基于 electron 的开源工具箱，自由集成丰富插件。 | <https://rubickcenter.github.io/rubick/> |
| scoop install crawlergo -g | A powerful browser crawler for web vulnerability scanners | <https://github.com/Qianlitp/crawlergo> |
| scoop install windterm -g | SSH/Sftp/Shell/Telnet/Serial client | <https://kingtoolbox.github.io/> |
| scoop install pwsh -g | Cross-platform automation and configuration tool/framework, known as Powershell Core, that works well with existing tools and is optimized for dealing with structured data. | <https://github.com/PowerShell/PowerShell> |
| scoop install FluentSearch -g | null | <https://www.fluentsearch.net/> |
| scoop install innounpacker -g | null | <https://www.rathlev-home.de/index-e.html?tools/prog-e.html#unpack> |
| scoop install fastgithub -g | github加速神器，解决github打不开、用户头像无法加载、releases无法上传下载、git-clone、git-pull、git-push失败等问题.  | <https://github.com/dotnetcore/FastGithub> |
| scoop install confuserex-gui -g | An open-source, free protector for .NET applications | <https://mkaring.github.io/ConfuserEx/> |
| scoop install dev-sidecar -g |   开发者边车，github打不开，github加速，git clone加速，git release下载加速，stackoverflow加速 . | <https://github.com/docmirror/dev-sidecar> |
| scoop install xunlei -g | 迅雷11 v11.2.2.1716 绿色精简版v2 | <https://www.ghxi.com/thunder11green.html> |
| scoop install igdm -g | Desktop application for Instagram DMs | <https://github.com/igdmapps/igdm/> |
| scoop install everything-lite -g | Locate files and folders by name instantly. (lite version, does not contain IPC and ETP/FTP/HTTP servers) | <https://www.voidtools.com> |
| scoop install wireshark3.6 -g | A network protocol analyzer that lets you see what’s happening on your network at a microscopic level. | <https://www.wireshark.org/> |
| scoop install wireshark -g | A network protocol analyzer that lets you see what’s happening on your network at a microscopic level. | <https://www.wireshark.org/> |
| scoop install curl-impersonate -g | A special build of curl for Windows that can impersonate Chrome | <https://github.com/depler/curl-impersonate-win> |
| scoop install git -g | Distributed version control system | <https://gitforwindows.org> |
| scoop install todesk -g | ToDesk Windows客户端.  | <https://www.todesk.com/> |
| scoop install another-redis-desktop-manager -g |  更快、更好、更稳定的Redis桌面(GUI)管理客户端，兼容Windows、Mac、Linux，性能出众，轻松加载海量键值. | <https://github.com/qishibo/AnotherRedisDesktopManager> |
| scoop install w3cschool -g | w3cschool离线版，包含HTML,CSS,Javascript,jQuery,C,PHP,Java,Python,Sql,Mysql等编程语言和开源技术的在线教程及使用手册 | <https://www.w3cschool.cn> |
| scoop install notepadplusplus-np -g | Text and source code editor | <https://notepad-plus-plus.org/> |
| scoop install windows-terminal -g | The new Windows Terminal, and the original Windows console host - all in the same place! | <https://github.com/microsoft/terminal> |
| scoop install uTools -g | 新一代效率工具平台. | <https://u.tools/> |
| scoop install verycapture -g | 支持长截图，矩形截图，延时截图，任意区域截图，gif录制，录屏，ocr翻译等功能 | <https://verycapture.com/cn/download.html> |
| scoop install mobaxterm -g | MobaXterm 简体中文汉化版 | <https://github.com/RipplePiam/MobaXterm-Chinese-Simplified.> |
| scoop install Maye-lite -g | 更轻更简洁的快速启动工具，功能单一化，专注于文件的快速启动 | <https://t.arae.cc/p/25804.html> |
| scoop install notify -g | Notify is a Go-based assistance package that enables you to stream the output of several tools (or read from a file) and publish it to a variety of supported platforms | <https://projectdiscovery.io> |
| scoop install cudatext-cn -g | Cross-platform text and code editor | <https://sourceforge.net/projects/cudatext> |
| scoop install python38 -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install transfer -g | 集合多个API的大文件传输工具 | <https://github.com/Mikubill/transfer> |
| scoop install everything-cli -g | Command line interface to Everything. | <https://www.voidtools.com/support/everything/command_line_interface/> |
| scoop install imfile -g | A full-featured download manager. | <https://imfile.io/> |
| scoop install vscode-insiders -g | Visual Studio Code is a lightweight but powerful source code editor (Insiders, Portable Edition). | <https://code.visualstudio.com/> |
| scoop install sublime-merge -g | A Git client with snappy UI, three-way merge tool, side-by-side diffs, syntax highlighting, and more. | <https://www.sublimemerge.com/> |
| scoop install vscode -g | Lightweight but powerful source code editor | <https://code.visualstudio.com/> |
| scoop install python37 -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install baidudisk -g | baidu net disk client | <http://pan.baidu.com/> |
| scoop install everything-np -g | Locate files and folders by name instantly. | <https://www.voidtools.com> |
| scoop install python-rc -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install python312 -g | A programming language that lets you work quickly and integrate systems more effectively. | <https://www.python.org/> |
| scoop install telegram-downloader -g | A cli utility for downloading files from Telegram, backing up your Telegram data, uploading files to Telegram, and recovering your Telegram data. | <https://github.com/iyear/tdl> |
| scoop install telegram -g | A messaging app with a focus on speed and security | <https://telegram.org> |
| scoop install aliyun -g | Manage and use Alibaba Cloud resources. | <https://github.com/aliyun/aliyun-cli> |
| scoop install fuzzDicts -g | Web Pentesting Fuzz 字典,一个就够了. | <https://github.com/TheKingOfDuck/fuzzDicts> |
| scoop install oneforall -g | OneForAll是一款功能强大的子域收集工具 | <https://github.com/shmilylty/OneForAll> |
| scoop install subfinder -g | Subfinder is a subdomain discovery tool that discovers valid subdomains for websites. Designed as a passive framework to be useful for bug bounties and safe for penetration testing | <https://projectdiscovery.io> |
| scoop install whatweb -g | whatweb 增强版 8000+插件（提供windows可执行文件）. | <https://github.com/winezer0/whatweb-plus> |
| scoop install observerward -g | Cross platform community web fingerprint identification tool | <https://0x727.github.io/ObserverWard/> |
| scoop install EHole_magic -g | EHole(棱洞)魔改。可对路径进行指纹识别；支持识别出来的重点资产进行漏洞检测(支持从hunter和fofa中提取资产)支持对ftp服务识别及爆破 | <https://github.com/lemonlove7/EHole_magic> |
| scoop install ehole -g | EHole(棱洞)3.0 重构版-红队重点攻击系统指纹探测工具。 | <https://github.com/EdgeSecurityTeam/EHole> |
| scoop install ENScan_GO -g | 一款基于各大企业信息API的工具，解决在遇到的各种针对国内企业信息收集难题。一键收集控股公司ICP备案、APP、小程序、微信公众号等信息聚合导出。 | <https://github.com/wgpsec/ENScan_GO> |
| scoop install ToolsFx -g | 基于kotlin+tornadoFx的跨平台密码学工具箱.包含编解码,编码转换,加解密, 哈希,MAC,签名,大数运算,压缩,二维码功能,ctf等实用功能,支持插件 | <https://github.com/Leon406/ToolsFx> |
| scoop install AlliN -g | A flexible scanner. | <https://github.com/P1-Team/AlliN> |
| scoop install txportmap -g | Port Scanner & Banner Identify From TianXiang | <https://github.com/4dogs-cn/TXPortMap> |
| scoop install ServerScan -g | ServerScan一款使用Golang开发的高并发网络扫描、服务探测工具。 | <https://github.com/Adminisme/ServerScan> |
| scoop install naabu -g | projectdiscovery/naabu: A fast port scanner written in go with a focus on reliability and simplicity. Designed to be used in combination with other tools for attack surface discovery in bug bounties and pentests | <https://github.com/projectdiscovery/naabu/> |
| scoop install dirxk -g | 一款集成了多种老牌工具字典的轻量级目录扫描器，包括御剑后台扫描字典，test404网站备份，web破壳扫描器，御剑1.5扫描字典，御剑专业版字典，wwwscan字典，dirscan字典，dirsafe字典，swebscan. | <https://github.com/xk11z/dirxk> |
| scoop install katana -g | A next-generation crawling and spidering framework. | <https://github.com/projectdiscovery/katana> |
| scoop install feroxbuster -g | 一个用 Rust 编写的快速，简单，递归的内容发现工具。A fast, simple, recursive content discovery tool written in Rust. | <https://github.com/epi052/feroxbuster> |
| scoop install dirmap -g | An advanced web directory & file scanning tool that will be more powerful than DirBuster, Dirsearch, cansina, and Yu Jian. | <https://github.com/H4ckForJob/dirmap> |
| scoop install dirsearch_bypass403 -g | 信息收集中时可使用它进行目录枚举，目录进行指纹识别，枚举出来的403状态目录可尝试进行绕过。 | <https://github.com/lemonlove7/dirsearch_bypass403> |
| scoop install gobuster -g | A tool to brute-force URIs, DNS subdomains or Virtual Host names | <https://github.com/OJ/gobuster> |
| scoop install ffuf -g | Fast web fuzzer written in Go | <https://github.com/ffuf/ffuf> |
| scoop install dirsearch -g | Web path scanner. | <https://github.com/maurosoria/dirsearch> |
| scoop install urlfinder -g | 一款快速、全面、易用的页面信息提取工具，可快速发现和提取页面中的JS、URL和敏感信息。 | <https://github.com/pingc0y/URLFinder> |
