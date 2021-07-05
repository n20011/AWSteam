# AWSサーバーを使用する時に使ったコマンド

## ssh command
### 制作したサーバーに接続するために使う
`ssh -i [プライベートkey] [user名]@[パブリックIPv4]`

## scp command
### サーバーへデータを転送するために使う
`scp -i [プライベートkey] [転送したいファイル] [user名]@[パブリックIPv4]:[転送先の指定]]`

<br>

# サーバー起動編
  
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

## マインクラフトの詳細設定
[こちらから](https://minecraft.server-memo.net/server-properties/)
