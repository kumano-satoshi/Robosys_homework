# Robosys_homework1
### ・Raspberry Pi 3 Model B+を用いてLチカをさせるデバイスドライバを作成
　「3つのLEDを順番に点滅させるモード」と「3つのLEDを光らせ続けるモード」を作成
 
## ・実行環境
OS ... Raspbian 10.1
 
  kernel ... Linux version 4.19
  
  使用言語 ... C言語
  
## ・実行方法
~~~~
$ cd Robosys_homework/device_driver
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
~~~~
##### 点滅モードの場合
~~~~
$ echo 1 > /dev/myled0
~~~~
##### 光らせ続けるモードの場合
~~~~
$ echo 2 > /dev/myled0
~~~~
##### 消灯させる場合
~~~~
$ echo 3 > /dev/myled0
~~~~
##### カーネルモジュールをアンロードする
~~~~
$ sudo rmmod myled
~~~~
 
## ・実行動画
　https://www.youtube.com/watch?v=m6WCQWNXWUs
　
