# jupyterlab_mysql
## ※M1Mac用です
jupyterlabとMySQLをセットにしたdocker-composeディレクトリです

(dbとworkは自動で生成されます)
```
jupyterlab_mysql
├── db => (MySQLのデータ保存場所)
│── work => （jupyterlabのコードを保存する場所）
│           
└── docker-compose.yml
```

※事前にDocker desktopのインストールが必要です。
## ディレクトリのクローンのやり方
ターミナルで下記を実行してください。
- SSH設定無しでクローンしたい方はこちら
```
https://github.com/keikois/jupyterlab_mysql.git
```
- SSHキーをGitHubで設定している方はこちら
```
git clone git@github.com:keikois/jupyterlab_mysql.git
```

クローンした後
```
cd jupyterlab_mysql
```
```
docker-compose up -d
```
上記コマンドを打つと、jupyterlabとMySQLとphpMyAdminが起動します。

localhost:8888をブラウザで開くとjupyterlabが開きます。（pyhtonとRとJulia言語が使えます）

- localhost:8888で起動後、workディレクトリを選択し、notebook => python3 (ipykernel)をクリック
- ここにpythonコードを書いた後、shift＋Enterでセルを実行できます。

localhost:8080をブラウザで開くとmySQLとphpMyAdminが連携された状態で開きます。

コンテナ終了コマンドは
```
docker-compose down
```
