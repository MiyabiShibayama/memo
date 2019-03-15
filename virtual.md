# 仮想環境について

## 構造
　　　　　　　 仮想環境 ...CentOS Ubuntu  
(デバイスドライバ)KVM   ...これを通して仮想マシンを立てる  
(土台)　　　　　Ubuntu  ...一番最初にパソコンに入ってるもの  
- これでパソコンの中にもう一つ小さいパソコンが！！

## コマンド
- virt-manager
	- 新しい仮想マシン立ち上げる
- apt-get install python3-venv
- python3 -m venv [名前]
- . ./venv/bin/activate
- deactivate

## 元のPCで仮想環境のPCを操作
1. 仮想環境のPCを立ち上げる
2. ssh username@ポート番号
3. 上記にあるコマンドを叩けばok

## Djangoでポート番号指定しない
- sudo ./venv/bin/python3 manage.py runserver localhost:80
- これでネット上のhttpには:80表示されない(デフォルトで指定されているため)
