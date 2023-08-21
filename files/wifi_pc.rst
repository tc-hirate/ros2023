============================================================
WiFi子機の使い方（PC）
============================================================

WiFiの速度を測定
============================================================

ツールをインストール。

.. code-block:: console

    ubuntu@mbc084:~$ sudo apt install speedtest-cli

|

速度を測定。

.. code-block:: console

    ubuntu@mbc084:~$ speedtest --simple
    Ping: 24.013 ms
    Download: 67.76 Mbit/s
    Upload: 39.07 Mbit/s

|

WiFi子機のドライバをインストール
============================================================

ツールのインストール。

.. code-block:: console

    ubuntu@mbc084:~$ sudo apt update
    ubuntu@mbc084:~$ sudo apt install git linux-headers-generic dkms

|

ダウンロードとインストール。

.. code-block:: console

    ubuntu@mbc084:~$ wget https://github.com/RinCat/RTL88x2BU-Linux-Driver/archive/master.zip
    ubuntu@mbc084:~$ unzip master.zip
    ubuntu@mbc084:~$ cd RTL88x2BU-Linux-Driver-master
    ubuntu@mbc084:~/RTL88x2BU-Linux-Driver-master$ sudo make uninstall
    ubuntu@mbc084:~/RTL88x2BU-Linux-Driver-master$ make clean
    ubuntu@mbc084:~/RTL88x2BU-Linux-Driver-master$ make
    ubuntu@mbc084:~/RTL88x2BU-Linux-Driver-master$ sudo make install
    ubuntu@mbc084:~/RTL88x2BU-Linux-Driver-master$ sudo modprobe 88x2bu

|

再起動。

.. code-block:: console

    ubuntu@mbc084:~/RTL88x2BU-Linux-Driver-master$ sudo shutdown -r now

|

もう一度、WiFiの速度を測定
============================================================

速度を測定。

.. code-block:: console

    ubuntu@mbc084:~$ speedtest --simple
    Ping: 24.187 ms
    Download: 197.15 Mbit/s
    Upload: 173.64 Mbit/s
