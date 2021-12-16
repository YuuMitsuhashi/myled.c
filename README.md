# ロボットシステム学課題1～LEDの点灯～
4sのロボットシステム学でLEDを点灯させるデバイスドライバを作成  
現時点では講義の通り入力によりLEDのONOFFを切り替えられるもの  
***

## 環境
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

## 動作手順    
 `$ git clone https://github.com/YuuMitsuhashi/myled.c`　クローンをする 
 
 `$ cd myled.c/`  ディレクトリ移動 
 
 `$ make`  ビルド
 
 `$ sudo insmod myled.ko`  カーネルモジュールをロードする
 
 `$ sudo chmod 666 /dev/myled0`  アクセス権限の変更  
 
 `$ sudo rmmod myled`  カーネルモジュールをアンロード  
 
 `$ make clean`  ビルドしたファイルの削除
 
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
 
 
 
 
 
 
 
