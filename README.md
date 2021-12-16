# ロボットシステム学課題1～LEDの点灯～
4sのロボットシステム学でLEDを点灯させるデバイスドライバを作成  
Rasberry Pi4にUbuntuをインストールし動作を行う  
現時点では講義の通り入力によりLEDのONOFFを切り替えられるもの  
***  

## 使用した部品や機器　　
・Rasberry Pi 4  
・LED(青色)  
・ジャンパワイヤ×2  
・抵抗 220Ω×1  
***

## 動作手順    
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
  
 ## 今後の予定
  LEDを2つ別のピンで使用し交互に点灯するデバイスドライバを作成する  
  環境はすべて同じで、LED,抵抗それぞれ1個ずつ追加. デバイスドライバの変更
  ***
 
 
 
 
 
 
 
