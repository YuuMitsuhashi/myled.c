## 概要  
ロボットシステム学課題1～LEDの点灯～
4sのロボットシステム学でLEDを点灯させるデバイスドライバを作成  
Rasberry Pi4にUbuntuをインストールし動作を行う  
現在(12/17の時点)では講義の内容を踏まえて、LEDを2個に増やし同時にONOFFを切り替えられるものである   
*** 
## 実行した動画  
  https://www.youtube.com/watch?v=_pElwhP2Sic
  
## 実行方法  
以下の文をUbuntuのターミナル画面で入力  
 ・LEDの点灯  
 `$ echo 1 > /dev/myled0`
 
 ・LEDの消灯  
 `$ echo 0 > /dev/myled0`  
 
 ***

## 使用した部品や機器　　
・Rasberry Pi 4  
・LED(青色,赤色)  
・ジャンパワイヤ6本  
・抵抗 220Ω×2
***

## インストール方法    
 `$ make`  ビルド
 
 `$ sudo insmod myled.ko`  カーネルモジュールをロードする
 
 `$ sudo chmod 666 /dev/myled0`  アクセス権限の変更  
 
 `$ sudo rmmod myled`  カーネルモジュールをアンロード  
 
 `$ make clean`  ビルドしたファイルの削除
 
 ***  
 
 ## 注意事項  
 ブレッドボードとRasberryPiを接続する際には、必ず使用ピンとブレッドボードが正しく接続されているか確認すること.  
 

 
 ## 回路関係    
 ・回路の様子  
 https://user-images.githubusercontent.com/72642701/146400441-40273226-e41a-4c56-aee6-cc1e4db8d921.jpg  
 
 ・回路図と使用したGPIOピン  
 https://user-images.githubusercontent.com/72642701/146402109-7fabb734-59ab-4051-9936-7ad9c0b6ca3f.jpg  

 
 
  
 ## LICENSE  
  myled.c is under GNU General Public License v3.0(https://www.gnu.org/licenses/gpl-3.0.ja.html)  
  
 ## 今後の予定
  LEDを2つ別のピンで使用し交互に点灯するデバイスドライバを作成する  
  環境はすべて同じで、LED,抵抗それぞれ1個ずつ追加. デバイスドライバの変更
  ***
 
 
 
 
 
 
 
