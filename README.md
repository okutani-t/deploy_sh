# deploy_sh

deploy.sh is the simplest way to deploy your applications.

## Requirement

ssh-agentを起動しておく（win,Linux）。

```
$ sudo vi ~/.bashrc
eval `ssh-agent` > /dev/null 2>&1
ssh-add ~/.ssh/id_rsa > /dev/null 2>&1
$ source ~/.bashrc
```

## Settings

「ここから～ここまで」の中を適宜編集。

### ■deploy_path

デプロイしたい場所を記述。

```
例: deploy_path=/var/www/
```

### ■proj_name

プロジェクトの名前を記述。

```
例: proj_name=myapp
```

### ■remote_path

リモートリポジトリのパスを記述。GitHubでもBitbucketでもなんでもOK。

```
例: remote_path=git@github.com:okutani-t/first-git.git
```

### ■branch

デプロイするブランチを指定。

```
例1: branch=master
例2: branch=develop
```

### ■host

SSHで接続するときの情報。user@hostの形で記載。

~/.ssh/configを設定しておけばhostnameだけでもOK。

```
例1: host=okutani@example.com
例2: host=sakura
```

## Usage

実行権限をつけて実行。

```
$ chmod +x deploy.sh
$ ./deploy.sh
```

## Install

このリポジトリをcloneすればOK。場所はどこでもいいがプロジェクトに配置しておくと分かりやすい。

```
$ git clone https://github.com/okutani-t/deploy_sh.git
```

## Licence

MIT

## Blog Article

さらに詳しいことは以下の記事からどうぞ。

・記事準備中

bareリポジトリ作成してプッシュしてデプロイする方法もある。以下参照。

[git pushで本番環境に”自動デプロイ”できる環境を作ってみよう！ | vdeep](http://vdeep.net/git-push-deploy)

## Author

[okutani](http://okutani.net)
