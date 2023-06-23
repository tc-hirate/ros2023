============================================================
Linuxのインストール（PC）
============================================================

Linuxはオープンソースのオペレーティングシステム（OS）です。

PCにはUbuntu Desktop 22.04 LTSをインストールします。

|

Linuxのダウンロード
============================================================

Ubuntu Desktop 22.04 LTSのディスクイメージを `UbuntuのHP <https://releases.ubuntu.com/22.04/>`_ からダウンロードします。

.. image:: ./img/linux_download_img_01.png
   :width: 800px
   :align: center

|

ダウンロードフォルダに保存されます。

.. image:: ./img/linux_download_img_02.png
   :width: 800px
   :align: center

|

|

Rufusのダウンロード
============================================================

Rufus（ルーファス）は起動可能なUSBフラッシュドライブを作成することができるソフトウェアです。

Rufusを `RufusのHP <http://rufus.ie/ja/>`_ からダウンロードします。

.. image:: ./img/rufus_download_img_01.png
   :width: 800px
   :align: center

|

下のほうにスクロールしていくと、ダウンロードのリンクがあります。

ここから、Portableをダウンロードしてください。

.. image:: ./img/rufus_download_img_02.png
   :width: 800px
   :align: center

|

ダウンロードフォルダに保存されます。

.. image:: ./img/rufus_download_img_03.png
   :align: center

|

|

Live USBの作成
============================================================

ダウンロードしたRufusをダブルクリックすると、Rufusが起動します。

［選択］ボタンをクリック。

.. image:: ./img/live_usb_img_01.png
   :align: center

|

Ubuntuのイメージディスクファイルを選択。

.. image:: ./img/live_usb_img_02.png
   :align: center

|

［スタート］ボタンをクリック。

.. image:: ./img/live_usb_img_03.png
   :align: center

|

［OK］ボタンをクリック。

.. image:: ./img/live_usb_img_04.png
   :align: center

|

［はい］ボタンをクリック。

.. image:: ./img/live_usb_img_05.png
   :align: center

|

［OK］ボタンをクリック。

.. image:: ./img/live_usb_img_06.png
   :align: center

|

インストールメディアの作成中。

.. image:: ./img/live_usb_img_07.png
   :align: center

|

［閉じる］ボタンをクリック。

.. image:: ./img/live_usb_img_08.png
   :align: center

|

|

Linuxのインストール
============================================================

Live USBをPCに挿入してください。

PCの電源ボタンを押したら、［F12］キーを連打し、Boot Optionsの画面を表示させてください。

.. image:: ./img/linux_install_img_01.png
   :width: 800px
   :align: center

|

［↑］と［↓］を使ってUSB Storagr Deviceを選択し、［Enter］を押す。

.. image:: ./img/linux_install_img_02.png
   :width: 800px
   :align: center

|

Try or Install Ubuntuが選択されていることを確認し、［Enter］を押す。

.. image:: ./img/linux_install_img_03.png
   :width: 800px
   :align: center

|

しばらく待つ。

.. image:: ./img/linux_install_img_04.png
   :width: 800px
   :align: center

|

もう少し待つ。

.. image:: ./img/linux_install_img_05.png
   :width: 800px
   :align: center

|

Welcomeは、「English」が選択されいることを確認し、［Install Ubuntu］ボタンをクリック。

.. image:: ./img/linux_install_img_06.png
   :width: 800px
   :align: center

|

Keyboard layoutは、「Japanese」−「Japanese」を選択し、［Continue］ボタンをクリック。

.. image:: ./img/linux_install_img_07.png
   :width: 800px
   :align: center

|

Updates and other softwareは、デフォルトのまま ［Continue］ボタンをクリックする。

※有線LANを接続していないと、Wirelessの設定画面が出てくる。

.. image:: ./img/linux_install_img_08.png
   :width: 800px
   :align: center

|

Installation typeは、 ［Erase Ubuntu 22.04.2 LTS and reinstall］を選択し ［Install Now］ボタンをクリック。

※違う画面が出てくるかもしれない。

.. image:: ./img/linux_install_img_09.png
   :width: 800px
   :align: center

|

Write the changes to disks?ウィンドウが表示されたら ［Continue］ボタンをクリック。

.. image:: ./img/linux_install_img_10.png
   :width: 800px
   :align: center

|

Where are you?は、［Tokyo］が選択されていることを確認したら ［Continue］ボタンをクリック。

.. image:: ./img/linux_install_img_11.png
   :width: 800px
   :align: center

|

Who are you?は、次の通り入力してください。

|

Your name: ubuntu

Your computer's name: mbc***

Pick a username: ubuntu

Choose a password: hirate2020

Confirm your password: hirate2020

Require my password to login: Require my password to log in にチェック

|

入力できたら［Continue］ボタンをクリック。

.. image:: ./img/linux_install_img_12.png
   :width: 800px
   :align: center

|

インストールが始まる。

.. image:: ./img/linux_install_img_13.png
   :width: 800px
   :align: center

|

インストールが終了すると、 Installation Completeウィンドウが表示されるので ［Restart Now］ボタンをクリック。

.. image:: ./img/linux_install_img_14.png
   :width: 800px
   :align: center

|

Please remove the installation medium, then press ENTER というメッセージが表示されるので Live USBを抜いて［Enter］を押す。

.. image:: ./img/linux_install_img_15.png
   :width: 800px
   :align: center

|

|

Linuxへのログイン
============================================================

ログイン画面が表示されたら、 パスワードを入力してログインしてください。

.. image:: ./img/linux_login_img_01.png
   :width: 800px
   :align: center

|

はじめに、各種設定の画面が表示されるが、 全てデフォルトのままとします。

Connect Your Online Accountsは、 ［Skip］ボタンをクリック。

.. image:: ./img/linux_login_img_02.png
   :align: center

|

Livepatchは、 デフォルトのまま［Next］ボタンをクリック。

.. image:: ./img/linux_login_img_03.png
   :align: center

|

Help improve Ubuntuは、 デフォルトのまま［Next］ボタンをクリック。

.. image:: ./img/linux_login_img_04.png
   :align: center

|

Privacyは、 デフォルトのまま［Next］ボタンをクリック。

.. image:: ./img/linux_login_img_05.png
   :align: center

|

You're ready to go!は、 ［Done］ボタンをクリック。

.. image:: ./img/linux_login_img_06.png
   :align: center

|

Software Updaterが出てきたら、 ［Install Now］ボタンをクリック。

.. image:: ./img/linux_login_img_07.png
   :align: center

|

アップデート中。

.. image:: ./img/linux_login_img_08.png
   :align: center

|

アップデートが終了したら、 ［Restart Now］をクリックして再起動する。

.. image:: ./img/linux_login_img_09.png
   :align: center

|

Linuxの日本語化
============================================================

左下のワッフルメニューをクリックして、アプリケーションを表示する。
[Settings]をクリックする。

Linux Japanese 1

[Settings]が起動する。

Linux Japanese 2

[Region & Language]を選択し、[Manage Installed Languages]をクリックする。

Linux Japanese 3

[Install]をクリックする。
ここでパスワードの入力を求められるので、パスワードを入力する。

Linux Japanese 4

変更の適用中。

Linux Japanese 6

[Language]に日本語（まだグレー）があることを確認したら、[Close]をクリックする。

Linux Japanese 7

[Language]をクリックする。

Linux Japanese 8

[日本語]を選択して、[Select]をクリックする。

Linux Japanese 9

[Restart]をクリックして、再起動する。
実際はログアウトするだけなので、再度ログインする。

Linux Japanese 10

再起動すると次のウィンドウが出てくるので、
[次回から表示しない]にチェックをして、
[古い名前のままにする]をクリックする。

Linux Japanese 11

表示が日本語化された。
再度Settingsを起動して、[地域と言語]をクリックする。
[入力ソース]の下の[+]をクリックする。

Linux Japanese 12

[日本語]をクリックする。

Linux Japanese 13

[日本語(Mozc)]を選択して、[追加]をクリックする。

Linux Japanese 14

[入力ソース]に[日本語(Mozc)]が追加された。

Linux Japanese 15

これで日本語を入力することができるようになりました。
日本語と英語の切り替えは、[Windows] + [Space] で行います。
