# Windows でのパッケージ管理は Scoop


最近、Windows 上で Powershell を使ってちょっとした開発を行った際に、Powershell のコマンド分からん…! となっていたんですが、Scoop というパッケージマネージャーを使って Linux 系のコマンドだったりパッケージをインストールすることで開発しやすくなりました。その内容を記事にしてみます。

Scoop とは？
Windows で動くパッケージマネージャー。コマンドプロンプトや Powershell で使用できる。
Windows でのパッケージマネージャーといえば、
[winget](https://learn.microsoft.com/ja-jp/windows/package-manager/winget/) や 
[chocolatey](https://chocolatey.org/) が有名ですが、
Scoop はよりデベロッパーフレンドリーなんだとか。
また、winget だとコマンドでインストールしたもの以外も管理下に置かれますが、scoop だと scoop でインストールしたもののみを管理できます (この点は、chocolaty と同様かもしれません)。


例えば、Git for Windows をインストールする場合、インストーラーをダウンロードして実行して Next ボタンをポチポチして… みたいな形ですが、Scoop だと scoop install git コマンドで一発。アンインストールする際も同様にコマンドだけで完結できます。


# インストール方法
上記リンク先の、Quickstart に従って、Powershell でコマンドを実行するだけ。それだけ。

# 使い方
上でもちょっと書きましたが、何かインストールする際には以下コマンド。

```
scoop install {package_name}
```

アンインストールは以下。

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