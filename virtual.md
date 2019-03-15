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
