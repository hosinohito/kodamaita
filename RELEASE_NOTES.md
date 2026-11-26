# こだま板（仮）1.1.0

こだま板は、参加端末の保管ノード同士で投稿を受け渡す掲示板です。

**匿名ではありません。IPと投稿時間と投稿内容が紐づけられ、何があっても削除できません。**

責任をもって自由に投稿し、特定思想による弾圧を可能な限り排除するSNSです。通常のSNSはユーザーが増えるほど不安定になりますが、こだま板はユーザーのサーバー運用によってより安定したシステムになります。外部から投稿を受け付ける保管ノード（サーバー）を運用すると、自己紹介の公開と固定ハンドルネームの利用ができます。今後のリリースで、サーバー運用特典が追加されるかもしれません。

動作確認はwindows版とandroid版でのみ行っています。mac,linuxで不具合が出た場合、できるだけ詳細に症状を教えてもらうと対応できるかもしれません。
iOS版は偏った思想による検閲とショバ代のために存在しえません。

## 1.1.0の変更点

- 保存確認が0台の投稿は「送信待ち」、1台で確認できた投稿は「1台に保存済み・複製待ち（1/2）」と表示します。
- 異なる2台の確認で待ち表示が消えます。投稿をし直さなくても、同じ投稿が自動で再送されます。

## インストールと起動

| OS | ダウンロードするファイル | 起動手順 |
| --- | --- | --- |
| Windows 10/11 x64 | `Kodamaita-1.1.0-win-x64.zip` | [.NET 10.0.15以降のRuntime](https://dotnet.microsoft.com/download/dotnet/10.0) の Windows x64 を入れ、ZIPを展開して `Kodamaita.exe` を開く。 |
| Android ARM64（Android 6以降） | `Kodamaita-1.1.0-android-arm64.apk` | APKをダウンロードして開く。端末に求められた場合は、開いたブラウザーまたはファイルアプリに「この提供元を許可」を設定してインストールする。更新は既存アプリを削除せず上書きする。 |
| macOS（Appleシリコン／Intel） | `Kodamaita-1.1.0-osx-arm64.zip`（Appleシリコン）または `Kodamaita-1.1.0-osx-x64.zip`（Intel） | CPUに合う [.NET 10.0.15以降のRuntime](https://dotnet.microsoft.com/download/dotnet/10.0) を導入し、ZIPを展開。ターミナルで展開先に移動し `dotnet Kodamaita.Desktop.dll`。署名・公証済みのアプリではありません。 |
| Linux x64／ARM64 | `Kodamaita-1.1.0-linux-x64.zip` または `Kodamaita-1.1.0-linux-arm64.zip` | グラフィカルなデスクトップ環境で、CPUに合う [.NET 10.0.15以降のRuntime](https://dotnet.microsoft.com/download/dotnet/10.0) とディストリビューションのX11（WaylandではXWayland）・Fontconfigとデスクトップ用フォントを入れる。ZIPを展開し、展開先で `sh start-kodamaita.sh`。 |

Windowsでの起動・投稿、Android APKの署名と版番号を確認しています。macOS・Linuxは対象CPU向けのビルドです。デスクトップ版の設定・投稿はアプリの隣の `kodamaita-data` に保存されます。更新時はこのフォルダーを残してください。

## 最初の接続

起動すると接続先を自動で探します。接続先を案内された場合は、歯車から「接続先」に貼り付けて「接続先を保存して同期」。保管ノードを公開する手順は「サーバー公開手順」にあります。緑ランプになれば自己紹介とコテハンを設定できます。

投稿は公開されます。「排除」は自分の端末で投稿者を非表示にする機能で、設定の一番下から取り消せます。

[配布ファイル](https://github.com/hosinohito/kodamaita/releases)の改変確認には同梱の `SHA256SUMS.txt` を使えます。