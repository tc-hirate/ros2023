============================================================
WiFi子機の使い方（Raspberry Pi）
============================================================


WiFiの速度を測定
============================================================

ツールをインストール。

.. code-block:: console

    pi@zumo00:~$ sudo apt install speedtest-cli

|

速度を測定。

.. code-block:: console

    pi@zumo00:~$ speedtest --simple
    Ping: 56.993 ms
    Download: 40.93 Mbit/s
    Upload: 33.86 Mbit/s

|

WiFi子機のドライバをインストール
============================================================

ツールのインストール。

.. code-block:: console

    pi@zumo00:~$ sudo apt update
    pi@zumo00:~$ sudo apt install dkms build-essential linux-headers-generic
    pi@zumo00:~$ sudo apt install git

|

ダウンロードとインストール。

.. code-block:: console

    pi@zumo00:~$ git clone https://github.com/aircrack-ng/rtl8812au.git
    pi@zumo00:~$ cd rtl8812au

|

Makefileの編集

.. code-block:: console

    pi@zumo00:~/rtl8812au$ nano Makefile 

.. code-block:: console

    ###################### Platform Related #######################
    CONFIG_PLATFORM_I386_PC = n
    ・・・・・
    CONFIG_PLATFORM_ARM64_RPI = y

|

シャットダウン。

.. code-block:: console

    pi@zumo00:~/rtl8812au$ sudo shutdown -h now

|

WiFi子機を接続して、電源ON。

起動後、IPアドレスを確認すると、「4: wlx30de4bcfff61」が追加されている。

.. code-block:: console

    pi@zumo00:~$ ip a
    1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
        link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
        inet 127.0.0.1/8 scope host lo
        valid_lft forever preferred_lft forever
        inet6 ::1/128 scope host 
        valid_lft forever preferred_lft forever
    2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
        link/ether b8:27:eb:71:91:bf brd ff:ff:ff:ff:ff:ff
        inet 192.168.1.32/24 metric 100 brd 192.168.1.255 scope global dynamic eth0
        valid_lft 259035sec preferred_lft 259035sec
        inet6 fe80::ba27:ebff:fe71:91bf/64 scope link 
        valid_lft forever preferred_lft forever
    3: wlan0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
        link/ether b8:27:eb:24:c4:ea brd ff:ff:ff:ff:ff:ff
        inet 192.168.1.250/24 brd 192.168.1.255 scope global wlan0
        valid_lft forever preferred_lft forever
        inet6 fe80::ba27:ebff:fe24:c4ea/64 scope link 
        valid_lft forever preferred_lft forever
    4: wlx30de4bcfff61: <BROADCAST,MULTICAST> mtu 2312 qdisc noop state DOWN group default qlen 1000
        link/ether 30:de:4b:cf:ff:61 brd ff:ff:ff:ff:ff:ff

|

ネットワークの設定を変更する。

.. code-block:: console

    pi@zumo00:~$ sudo nano /etc/netplan/99_config.yaml

.. code-block:: console

        wifis:
    #       wlan0:
            wlx30de4bcfff61:

設定を反映させる。

.. code-block:: console

    pi@zumo00:~$ sudo netplan apply

|

再起動。

.. code-block:: console

    pi@zumo00:~$ sudo shutdown -r now

|

もう一度、WiFiの速度を測定
============================================================

速度を測定。

.. code-block:: console

    pi@zumo00:~$ speedtest --simple
    Ping: 22.697 ms
    Download: 175.04 Mbit/s
    Upload: 150.72 Mbit/s
