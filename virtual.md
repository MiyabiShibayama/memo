# 仮想環境について

## 構造
　　　　　　　 仮想環境 ...CentOS Ubuntu 
(デバイスドライバ)KVM   ...これを通して仮想マシンを立てる  
(土台)　　　　　Ubuntu  ...一番最初にパソコンに入ってるもの  
- これでパソコンの中にもう一つ小さいパソコンが！！

## KVM
- sudo apt install -y qemu-kvm libvirt0 libvirt-bin virt-manager bridge-utils
	- qemu-kvmとKVM設定用のパッケージをインストール
- sudo systemctl enable libvirt-bin
	- libvirt-binをsystemdに登録
- sudo gpasswd libvirtd -a <username>
	- libvirtdグループに所属しているとsudoなしでvirt-managerやvirshを実行できる
- sudo mkdir /var/lib/libvirt/iso
- sudo mv ubuntu-16.04-desktop-amd64.iso /var/lib/libvirt/iso/
- sudo chown libvirt-qemu:libvirtd \ /var/lib/libvirt/iso/ubuntu-16.04-desktop-amd64.iso
	- bvirtdグループのユーザで共有できるようにiso用のディレクトリを作成
	- 仮想マシンで使用するubuntu-16.04-desktop-amd64.isoを格納

## 仮想環境
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
