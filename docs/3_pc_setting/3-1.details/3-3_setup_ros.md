## ROS設定

cube-petit用のPCで設定を行います。


## ROS2 Jazzyの導入


ターミナルを開いて以下コマンドを実行します。
ROS2 Jazzyがインストールされます。

パスワードを求められたらパスワードを入力してください。
(yes)と表示されたらyesと入力しエンターキーを押してください。

```bash
source ~/work/setup_cube_petit/setup_ros.bash
```

SSHキーの登録をしていない場合はいくつかパッケージが入らずエラーが出ます。
以下のコマンドを実行してください。

```bash
cd ~/ros/src
rosdep install --from-path . --ignore-src -r -y

cd ~/ros
colcon build --symlink-install
```


---

[indexに戻る](../index.md)
|[PC設定に戻る](../3_pc_setting.md)
|[次のページ](./3-4_wire.md)
