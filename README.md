# wordpress-dev-local
WordPressのローカル開発環境です  
テーマをローカルで開発する時に利用することを想定しています

## 基本的な使い方(起動、WordPress動作確認)

1. .envファイルを編集する(何を記載するかは.envファイルに書いています)
2. dockerのビルド、起動する

```
$ docker-compose build --no-cache
$ docker-compose up -d
```

* http://localhost:2080/ で、WordPress、WordPress管理画面の確認ができます
* http://localhost:3080/ で、phpMyAdminが確認できます

## 構成

* データベース : mysql v8.3.0
* PHP : v8.3
* WordPress : v6.4.3

## テーマ開発の準備

1. 以下の様な配置でご利用ください

```
wordpress
├── wordpress-dev-local (このリポジトリ)
└── theme-XXXXX (theme開発用ディレクトリ。/html/wp-content/themes/theme-XXXXXに自動で配置されます)
```

2. docker-compose.ymlを環境に合わせて修正する

ここの箇所です

```
      # テーマを開発する場合は以下の行を有効にする(以下は1階層上にtheme用リポジトリが存在する場合の例)
      #- ../theme-XXX:/var/www/html/wp-content/themes/theme-XXX
```

3. 修正した場合は、基本的な使い方 2の手順をやり直してください
