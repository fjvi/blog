# 🔖 Windows でのパッケージ管理は Scoop

什么是 Scoop？它是一个在 Windows 上运行的软件包管理器。 它可以在 cmd 或 Powershell 中使用

Windows 上的软件包管理器包括
- [winget](https://learn.microsoft.com/ja-jp/windows/package-manager/winget/)   
- [chocolatey](https://chocolatey.org/) 
- [Scoop](https://scoop.sh/)

区别：使用 winget，除使用命令安装的软件包外，其他软件包也会被置于管理之下，
但使用 scoop，只有使用 scoop 安装的软件包才能被管理（这与 chocolaty 类似）。

使用管理工具的好处，例如：
安装 Windows 版 Git 时，需要下载并运行安装程序，然后点击 “下一步 ”按钮
使用 Scoop 时，只需使用 scoop install git 命令即可。 卸载时，也同样可以用命令完成。


# 🔖 安装scoop
https://scoop.sh/
Quickstart に従って、Powershell でコマンドを実行するだけ
```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```


# 🔖 使用方法
安装：
```
scoop install {package_name}
```
卸载：
```
scoop uninstall {package_name}
```


他のオプションは以下の通り。

```
>scoop -h
Usage: scoop <command> [<args>]

Available commands are listed below.

Type 'scoop help <command>' to get more help for a specific command.

Command    Summary
-------    -------
alias      Manage scoop aliases
bucket     Manage Scoop buckets
cache      Show or clear the download cache
cat        Show content of specified manifest.
checkup    Check for potential problems
cleanup    Cleanup apps by removing old versions
config     Get or set configuration values
create     Create a custom app manifest
depends    List dependencies for an app, in the order they'll be installed
download   Download apps in the cache folder and verify hashes
export     Exports installed apps, buckets (and optionally configs) in JSON format
help       Show help for a command
hold       Hold an app to disable updates
home       Opens the app homepage
import     Imports apps, buckets and configs from a Scoopfile in JSON format
info       Display information about an app
install    Install apps
list       List installed apps
prefix     Returns the path to the specified app
reset      Reset an app to resolve conflicts
search     Search available apps
shim       Manipulate Scoop shims
status     Show status and check for new app versions
unhold     Unhold an app to enable updates
uninstall  Uninstall an app
update     Update apps, or Scoop itself
virustotal Look for app's hash or url on virustotal.com
which      Locate a shim/executable (similar to 'which' on Linux)
```