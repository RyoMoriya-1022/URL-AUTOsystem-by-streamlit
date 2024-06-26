# URL-auto-system
## 概要
このプログラムはstreamlitによるローカルホストアプリケーションです。jsonファイルの保存領域にURL、実行させたい時間を入力し、その情報をもとに任意の時間にURLを開くものとなっています。
## 開発環境
- OS Microsoft Windows 10 Home
- Python 3.12.0
- Docker python:3.9-slim

## 設計
- display.py
  - アプリケーションの表示とスクリプトの実行
- system.py
    - pandas,webbrowser,scheduleなどのモジュールを使用
- run.py
    - ローカルホストを開くためのコマンドを実行するスクリプト
  
## 使用方法
1. python環境が整備されている状態でrun.pyを実行する
2. 設定されるデフォルトサイトでローカルホストが立つ
3. 表に実行したいURL、時間などの情報を入力しSAVEボタンを押す
4. サイドバーから実行できる
5. ローカルホストを閉じる場合は実行したターミナルにctrl+Cを入力

## 注意
このアプリケーションはPCがスリープモードになると中断されてしまうため、設定でスリープモードをオフにする必要がある。

## 感想
このシステムが製作者が2022年に作成したものをリメイクした形となっている。リメイク前のデータはbranchのpastに配置してあるので興味がある方はぜひ。  

今回この小規模なアプリケーション作る(リメイク)際、可読性およびコード量の短さにこだわることにしてみた。  読みやすいコードを一から書くことはとても難しいことで、リメイク前のコードは、意味のないファイルや関数の区別、それによる各関数のつながりのわかりにくさなど、反省点のとても多い内容だった。実際にリメイクするとsystem.pyの一つのファイルに収まってしまったのは少し悲しみがありつつも可読性が高まり非常に良かった。  
このアプリケーションはstreamlitや他python packageを用いることで、非常に少ないコードで機能を持たせることができた。streamlitは特に手軽にwebアプリケーションを作ることができる。(html,cssで書いたら非常に時間がかかるデザインもお手軽にできる)  
ぜひ小規模アプリを開発する際は使ってみることをお勧めする。  

(小話)streamlitはクラウドにデプロイすることも簡単にできるため当初はその予定で開発していたのだが、streamlit cloudの使用によりwebbrowserパッケージが使用できないため各自でローカルホストを立ててもらうことにした。何かを開発するときはまず使用する環境のセキュリティを確認することをお勧めする。
