# Yesod-Auth HashDB の例

Yesod で認証処理を行うための情報が少なく、特に HashDB
を用いた説明があまりにもわかりにくいものばかりだったので、これから始めようという方に少しでもお役に立てばと思いそのサンプルを作成しました。

DB には SQLite を使用するようになっていますので、一度 Yesod を起動して Yesod に自動的にテーブルを作成させたあと以下のようにで SQLite
コンソールを起動して INSERT 文を実行してください。

``` sh
sqlite3 auth-example.sqlite3
```

``` sql
insert into user values (1, 'user', 'da00ec2e6ff9ed4d342b24a16e262c82f3c8b10b', 'salt');
```

これによって、ログインユーザ名が "user"、パスワードが "secret" のユーザが作成されます。

ログイン画面の URL は [http://localhost:3000/auth/login](http://localhost:3000/auth/login) です。

[http://localhost:3000/auth/logout](http://localhost:3000/auth/logout) にアクセスするとログアウトします。
