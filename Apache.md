# Apache
- Webサーバ(HTTPサーバ)ソフトウェアの一つ
- モジュール拡張可能(mod機能名)

## 使用目的
- Apacheを通してHTTPSをHTTPに変換してDjangoにおくりこもう

## バージョンと仮想環境の種類
- Apache2.2とApache2.4
	- 構文が少し違う
- CentOSとUbuntu
	- ディレクトリ構成が少し違う

## 手順
1. ApacheでHTTPの表示
2. ApacheでHTTPSの表示
3. ApacheでHTTPSを受取り、DjangoにHTTPとしておくりこむ(mod wsgi)


## 初期設定
1. インストール
2. 基本設定
3. モジュール導入

- ???
- ダウンロード: $ lynx http://httpd.apache.org/download.cgi
- 展開: $ gzip -d httpd-NN.tar.gz
        $ tar xvf httpd-NN.tar
        $ cd httpd-NN
- 設定: $ ./configure --prefix=PREFIX
- コンパイル: $ make
- インストール: $ make install
- カスタマイズ: $ vi PREFIX/conf/httpd.conf
- テスト: $ PREFIX/bin/apachectl -k start

- NN : 最新のバージョンナンバー
- PREFIX : インストールするサーバでのファイルシステムのパス(デフォルト:/usr/local/apache2)
- ???

- apt-get update
- apt-get install apache2 パッケージのインストール
-/etc/apache2/mods-available/dir.conf、/etc/apache2/conf-available/security.conf、/etc/apache2/apache2.confを編集
- /etc/init.d/apache2 restartでApache2を再起動


- sudo apt update
- sudo apt install apache2
- 起動:sudo service apache2 start
- 再起動:sudo service apache2 restart
- 停止:sudo service apache2 stop

