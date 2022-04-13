# Gitを1人で使いこなせるようになる

## 目的
Gitを1人で使いこなせるようになって、今後チームでGitを使うようになった際に最低限は扱えるようにしておきたい。 <br/>
そのため、個人の趣味開発でGitを使えるようにしておく。

## 使用するコマンド(5種 + 2種)

### git clone URL

$ git clone https://github.com/yuekami/SampleTakashi.git

上記コマンドでgithub上のコードを取得できる。
第二引数に直下のディレクトリを指定することもできる。

### git init

$ git init

上記コマンドでローカルリポジトリの作成を行う。
.git ディレクトリを作成して、そこでバージョン管理等を行ってくれるようになる。

### git add ディレクトリ名

$ git add ディレクトリ名

上記コマンドでローカルの変更をステージングエリアに追加できる。

### git commit

$ git commit -v

上記コマンドでローカルリポジトリに変更を追加できる。

### git remote add origin URL

$ git remote add origin URL

上記コマンドでorigin(ローカルリポジトリ)をURLのリモートリポジトリと紐づかせる。

### git push origin master

上記コマンドでmasterブランチにoriginの内容を追加できる。

### git pull origin master

上記コマンドでリモートリポジトリの内容をローカルに反映させる

### git status と git log

慣れてきたら記載。
あとマークダウンを綺麗にしたい。
