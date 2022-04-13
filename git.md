# gitとは
バージョン管理システム<br>
ファイル名に「日付」を付けたり「最新」と付けたりわけわからんくなる。<br><br>

# バージョン管理するとなにが嬉しいか
どのファイルの何を　誰が　いつ　何のために　変更したのかを残せる。<br>
↓<br>
最新のファイルがすぐにわかる。
<br><br>

# gitの仕組み
変更履歴を順々に記録する。<br>
記録を過去に遡れる。<br>
記録にメッセージを付けれる。
<br><br>

# 開発の流れ
リポジトリ：変更履歴を記録する場所。<br>
commit：個人リポジトリに変更履歴を記録。<br>
push：共有リポジトリに変更を共有。<br>
<br>
複数人での作業の流れ<br>
pull：共有リポジトリの情報を同期。<br>
変更⇒commit⇒push<br>
<br><br>

# githubとは
gitリポジトリ(コード)のホスティングサービス。<br>
ソーシャルコーディングの場。
<br><br>

# githubの特徴
プルリクエストによるコラボレーション。
<br><br>

## gitリポジトリのホスティングサービス
github, bitbuketもある。<br>
githubは非公開有料。
<br><br>


# コマンド

## バージョン確認
```cmd.exe
  $ git version
```
## gitの初期設定
```cmd.exe
$ git config --global user.name "github user name"
$ git config --global user.email github@example.com
```

## ローカルリポジトリの作成
.gitディレクトリが作成される。変更履歴などが保存される場所。<br>
```cmd.exe
$ git init
```

## ステージングエリアに変更を追加
```cmd.exe
$ git add "ファイル名"
```

## コミットして変更を記録
```cmd.exe
$ git commit -m "メッセージ"
$ git commit -v ⇒ 変更を見ながらメッセージ記入。
```

## 現在の状況を確認する。
ブランチがわかる。<br>
リモートリポジトリとのcommit差分数がわかる。<br>
ワーキングツリー(ローカル)とローカルリポジトリ(ステージングエリア)との差分がわかる。<br>commitするべき物はないよって。
```cmd.exe
$ git status ⇒ gitリポジトリの状況を表示する。
```

## 変更履歴を確認
commitとauthorとdateとメッセージがわかる。<br>
オプション<br>
--online<br>
一行で表示する。<br>
<br>
-p ファイル名<br>
ファイルの差分を表示する。<br>

-n 数字<br>
どんだけ分の履歴をみるか指定できる。<br>
```cmd.exe
$ git log
```

## ファイルの変更差分を確認(ステージとの差分)
```cmd.exe
$ git diff
```

## ステージとコミットの差分
```cmd.exr
$ git diff --staged
```

## githubにローカルリポジトリの内容をpush
originはエイリアス URLを登録
```cmd.exe
$ git remote add origin URL
```
```cmd.exe
$ git push origin master
```

# 基本的なワークフロー
1. ファイルの変更をステージングエリアへ追加する。
2. ローカルリポジトリにコミットする。
3. リモートリポジトリにプッシュする。

# ステージングエリア
複数ファイルを変更したときに、コミットするファイルを選択するためにあるのがステージングエリア。

# わかりやすいコミットメッセージ
1行目：変更内容の要約<br>
2行目：空白<br>
3行目：変更の理由<br>

# 管理しないファイルをgitの管理から外す。
.gitignoreファイルに指定することで、ファイルをgitの管理から外すことができる。<br>
自動生成されるファイルやパスワードが記載されているファイルなど。
