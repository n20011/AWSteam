# AWSサーバーを使用する時に使ったコマンド  
AWSを使っていて遭遇したコマンドを自分のメモ用としてGitにあげます  
資料を見たら誰でもできる資料の素材に使えるかも？

## ssh command
制作したサーバーに接続するために使う  
`ssh -i [プライベートkey] [user名]@[パブリックIPv4]`

<br>
<br>

## scp command
サーバーへデータを転送するために使う  
`scp -i [プライベートkey] [転送したいファイル] [user名]@[パブリックIPv4]:[転送先の指定]]`

<br>
<br>
<br>
<br>
<br>

# サーバー起動後編
## chmod command
chmodでbedrock_serverの権限を変更しないとscreenが使えません。なので、  
`chmod 700 bedrock_server`  
これで使えるようになります。
  
## screen command 
コマンドプロントを閉じても起動したままにするために使う  
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

## わからないことなどを参考にさせてもらっている記事
- [server.proprties](https://lifework-blog.com/minecraft-setting-bedrock-server/)  
- [screen command](lhttps://qiita.com/hnishi/items/3190f2901f88e2594a5f)
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
