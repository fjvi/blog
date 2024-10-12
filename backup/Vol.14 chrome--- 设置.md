# Chrome URLs コマンドの一覧
Chromeの隠しコマンドの一覧をまとめました。

```
chrome://about
chrome://chrome-urls
```


### コマンドの一覧
```
chrome://about
chrome://accessibility
chrome://appcache-internals
chrome://apps
chrome://blob-internals
chrome://bluetooth-internals
chrome://bookmarks
chrome://chrome
chrome://chrome-urls
chrome://components
chrome://conflicts
chrome://crashes
chrome://credits
chrome://device-log
chrome://devices
chrome://dino
chrome://discards
chrome://download-internals
chrome://downloads
chrome://extensions
chrome://flags
chrome://flash
chrome://gcm-internals
chrome://gpu
chrome://help
chrome://histograms
chrome://history
chrome://indexeddb-internals
chrome://inspect
chrome://interstitials
chrome://interventions-internals
chrome://invalidations
chrome://local-state
chrome://media-engagement
chrome://media-internals
chrome://nacl
chrome://net-export
chrome://net-internals
chrome://network-error
chrome://network-errors
chrome://newtab
chrome://ntp-tiles-internals
chrome://omnibox
chrome://password-manager-internals
chrome://policy
chrome://predictors
chrome://print
chrome://quota-internals
chrome://safe-browsing
chrome://serviceworker-internals
chrome://settings
chrome://signin-internals
chrome://site-engagement
chrome://suggestions
chrome://supervised-user-internals
chrome://sync-internals
chrome://system
chrome://taskscheduler-internals
chrome://terms
chrome://thumbnails
chrome://tracing
chrome://translate-internals
chrome://usb-internals
chrome://user-actions
chrome://version
chrome://webrtc-internals
chrome://webrtc-logs
```

### 以下はデバッグ専用のコマンド

The following pages are for debugging purposes only. Because they crash or hang the renderer, they're not linked directly; you can type them into the address bar if you need them.

chrome://badcastcrash/
chrome://inducebrowsercrashforrealz/
chrome://crash/
chrome://crashdump/
chrome://kill/
chrome://hang/
chrome://shorthang/
chrome://gpuclean/
chrome://gpucrash/
chrome://gpuhang/
chrome://memory-exhaust/
chrome://ppapiflashcrash/
chrome://ppapiflashhang/
chrome://inducebrowserheapcorruption/
chrome://heapcorruptioncrash/
chrome://quit/
chrome://restart/
 

知っておくと便利なChromeコマンド
あまりに沢山あるので、知っておくと便利なコマンドだけまとめてみました。

設定画面
chrome://settings/

Chromeの設定画面が開けます。

普通にメニューから開いても良いのですが、アドレスを叩いた方が早い場面もありますので、覚えておくとよいでしょう。

ブックマーク管理画面
chrome://bookmarks/

Chromeのブックマーク管理画面に移動できます。

メニューから開いた時と何ら変わりません。

ダウンロード履歴画面
chrome://downloads/

ダウンロード履歴の画面が開けます。

「ファイルをダウンロードしたはずなんだけど、どこに保存されちゃった？」って時に便利です。

拡張機能管理画面
chrome://extensions/

Chromeにインストールしている拡張機能の管理画面です。

履歴一覧画面
chrome://history/

Chromeの閲覧履歴を一覧で見られる画面です。

閲覧履歴に関しては、普通にメニューからも開けるし、「Command + Y」でも開けます。

Googleアプリ画面
chrome://apps/

Chromeアプリの画面を開けます。

ブックマークバーの「アプリ」からでも飛べますが、知っておくと便利です。

Chromeのバージョン確認
chrome://version/

現在使用しているChromeについての情報が見られます。

Chromeのバージョンがいくつなのかを確認したい時に便利。

プラグイン管理画面
chrome://plugins/

Chromeにインストールされているプラグインが一覧で見られます。

 

「拡張機能」と「プラグイン」は、言葉としては似ていますが違うものです。

「拡張機能」は、使用するとブラウザに新しい機能を追加したり、お気に入りのサイトの機能です。

 

プラグインは、ブラウザで Flash や Windows Media ファイルなどの特定の種類のウェブ コンテンツを処理するのに役立つものになります。

メモリ消費状況
chrome://memory-redirect/

Google Chrome内の、何がどれだけメモリを消費しているかが分かります。

「最近Chromeが重いなぁ」と思ったら、ここを見ながらエクステンションを整理するとよいでしょう。

キャッシュ管理画面
chrome://cache

Chromeが現在抱えているキャッシュを一覧できます。

この画面からは何をどうこうできるわけではなく、ただ見ているだけ。

「キャッシュが多いな」と感じたら、設定画面からキャッシュを削除しましょう。

試験機能、隠し設定
chrome://flags/

まだ実際には実装されていない機能を、実験的に使えるようにできます。

ただ、あくまで試験的な機能。

注意書きにも

「随時変更、中断、提供中止されることがある」

「ブラウザによってすべてのデータが削除されたり、予期せぬ方法でセキュリティやプライバシーが侵害されたりする可能性がある」

とあります。

ウイルスチェック、セキュリティ対策
chrome://settings/cleanup

「パソコンのクリーンアップ」という画面が表示される。

そこで「検索」ボタンをクリックすると、不審なソフトウェアを検出することができる。

Chromeクリーンアップで用いられているウイルス発見システムは、セキュリティ関連では有名な、スロバキア企業「ESET」が開発したものです。

検出対象となるのはランサムウェアやトロイの木馬型ウイルスだけでなく、グーグルが「好ましくないソフトウェア」と判断したあらゆるソフトです。

恐竜ゲーム dino
chrome://dino

オフライン時にChromeで遊べる「恐竜ゲーム」です。