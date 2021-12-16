# ロボットシステム学課題1～LEDの点灯～
4sのロボットシステム学でLEDを点灯させるデバイスドライバを作成  
現時点では講義の通り入力によりLEDのONOFFを切り替えられるもの  
***

## 動作環境
・Raspberry Pi 4  
・OS Ubuntu 20.04 sever
***

## 使用した部品や機器　　
・Rasberry Pi 4  
・LED  
・ジャンパワイヤ×2  
・抵抗 220Ω×1  
***

## 回路図とピン配置

***

## 使用方法について  
・以下の手順でコマンド入力インストール
 `$ git clone https://github.com/YuuMitsuhashi/myled.c`  
 
 `$ cd myled.c/`  
 
 `$ make`
 
 `$ sudo insmod myled.ko`
 
 `$ sudo chmod 666 /dev/myled0`  
 
 ・削除はこちら  
 `$ sudo rmmod myled`  
 `$ make clean`  
 
 ***
 
 ## 実行方法
 ・LEDの点灯  
 `$ echo 1 > /dev/myled0`
 
 ・LEDの消灯  
 `$ echo 0 > /dev/myled0`  
 
 ***
 
 ## 実行した動画  
  https://youtu.be/QDOI0Hoa17U
  
 ## LICENSE  
  GNU General Public License v3.0
  
  ***
 
 
 
 
 
 
 
