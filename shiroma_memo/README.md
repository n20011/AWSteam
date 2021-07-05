# AWSサーバーを使用する時に使ったコマンド

## ssh command
### 制作したサーバーに接続するために使う
`ssh -i [プライベートkey] [user名]@[パブリックIPv4]`

<br>
<br>

## scp command
### サーバーへデータを転送するために使う
`scp -i [プライベートkey] [転送したいファイル] [user名]@[パブリックIPv4]:[転送先の指定]]`

<br>
<br>
<br>
<br>
<br>

# サーバー起動後編
  
## screen command 
### コマンドプロントを閉じても起動したままにするために使う
`LD_LIBRARY_PATH=. screen ./bedrock_server`
  
停止するには以下のコマンドを行う  
  
3~4桁の番号を確認する
`screen -ls`
 
 セッションに接続 
`screen -r [番号]`
  
stopと入力しサーバーを終了できる
`stop`

<br>
<br>

## マインクラフトの詳細設定
[参照先](https://minecraft.server-memo.net/server-properties/)

<br>
<br>

## マインクラフトにアップデートが来たら・・・  
1. wgetを使い最新のサーバーをインストールする  
`sudo wget [最新サーバーのアドレス]`

2. 4つのファイルをcpで上書きする
    - `cp [旧バージョンのディレクトリ] /server.properties [新バージョンのディレクトリ]`
    - `cp [旧バージョンのディレクトリ] /permissions.json [新バージョンのディレクトリ]`
    - `cp [旧バージョンのディレクトリ] /whitelist.json [新バージョンのディレクトリ]`
    - `cp -r [旧バージョンのディレクトリ] /worlds [新バージョンのディレクトリ]`
