# configファイルについて

## [公式サイト](https://docs.python.org/ja/3/library/configparser.html)

[1]
- import configparser
- config = configparser.ConfigParser()
[2]
- from configparser import ConfigParser
- config = ConfigParser()

- [1]と[2]は同じ

1. はじめにconf.py(loadファイル)[project名のディレクトリ]とexample.conf(confファイル)[etcのディレクトリ]を用意する
2. 最終的にviews.py(主要ファイル)に読み込みできるようにしたいため準備していく
3. example.confは読み込ませる内容を、
4. conf.pyはviews.pyにexample.confを読み込ませるものを書く
5. 準備が整ったら、views.pyで使用する

- configuration(設定)の意味 >>> conf
- 中身はプログラムを使用する上で変更するかもしれないもの書く(ex.パスワードなど)
- githubにのせると困るものなどをconfigファイルにしておくとviews.pyをそのままpushできるので便利


