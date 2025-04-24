## PC設定

cube-petit用のPCで設定を行います。


## ネットワーク設定 & git net-toolsの導入

無線Wifiもしくは有線イーサネット接続をします。


詳細は[GithubのReadmeを見てください](https://github.com/AiriYokochi/setup_cube_petit/tree/feature/ros2_jazzy)

ターミナルを開いて以下コマンドを実行します。

```
sudo apt install -y git
mkdir -p ~/work && cd ~/work/
git clone https://github.com/AiriYokochi/setup_cube_petit.git -b feature/ros2_jazzy
```

①以下のコマンドを叩くとPCの全般の設定が始まります。
パスワードを求められたらパスワードを入力してください。
壁紙の変更、サイドバーを隠す、スリープモードの解除、Chromeのインストール
完了すると、背景画像が顔になります。
```
source ~/work/setup_cube_petit/setup_pc.bash
```
初回にChromeを開くとパスワードを求められますが、空白でエンターキーを二回押してください。



(オプション)②以下のコマンドを叩くと開発環境がインストールされます。
GitKraken, VSCode
```
source ~/work/setup_cube_petit/setup_dev_tools.bash
```

## SSHの設定

Cube petitのオプション機能を利用するためにはGithubのsbgisenグループに
アクセスできるSSH Keyの登録が必要です。
ターミナルで以下のコマンドを叩いて、エンターを3回押してください。
```
ssh-keygen
```
次に以下のコマンドを入力してください。
```
cat ~/.ssh/id_*.pub
```
表示された内容を以下のサイトにアクセスして入力してください。
https://github.com/settings/keys

緑色の[New SSH Key]ボタンをクリック

Titleにロボット名(自分がわかりやすいようにつける)
Keyに先程のコマンドの結果をコピペ(ssh~~~~~~~~ cube-petit@cube-petit-XX)

[Add SSH key]をクリック
`You have successfully added the key '<title>'.`と表示されたら成功です。

---

[indexに戻る](../index.md)
|[PC設定に戻る](../3_pc_setting.md)
|[次のページ](./3-2_setup_ros.md)
