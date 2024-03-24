# wordpress-dev-local
WordPressのローカル開発環境です  
テーマをローカルで開発する時に利用することを想定しています

## 使い方

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
