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
壁紙の変更、サイドバーを隠す、スリープモードの解除、Chromeのインストール

```
source ~/work/setup_cube_petit/setup_pc.sh
```

(オプション)②以下のコマンドを叩くと開発環境がインストールされます。
GitKraken, VSCode
```
source ~/work/setup_cube_petit/setup_dev_tools.sh
```

---

[indexに戻る](../index.md)
|[PC設定に戻る](../3_pc_setting.md)
|[次のページ](./3-2_setup_pc.md)
