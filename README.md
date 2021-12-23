## 概要  
ロボットシステム学課題1～LEDの点灯～
4sのロボットシステム学でLEDを点灯させるデバイスドライバを作成  
Rasberry Pi4にUbuntuをインストールし動作を行う  
講義の内容を踏まえて、LEDを2個に増やし、交互に5回ずつ点滅させるものである。   
*** 
## 実行した動画  
  https://www.youtube.com/watch?v=1PtQh-5hERE
  
## 実行方法  
以下の文をUbuntuのターミナル画面で入力  
 ・LED(緑)の点灯  
 `$ echo 1 > /dev/myled0`  
 
 ・LED(赤)の点灯  
 `$ echo 2 > /dev/myled0`  
 
 ・2つのLEDが交互に5回ずつ点滅  
 `$ echo 3 > /dev/myled0`
 
 ・LEDの消灯  
 `$ echo 0 > /dev/myled0`  
 
 ***

## 使用した部品や機器　　
・Rasberry Pi 4  
・LED(緑色,赤色)  
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
 https://user-images.githubusercontent.com/72642701/147205129-7608b129-7888-4456-b735-67ccf61af8c6.jpg  
 
 ・回路図と使用したGPIOピン  
 https://user-images.githubusercontent.com/72642701/147205196-ec0f3f72-4da8-47f6-8fac-6c9002e966f7.jpg    

 ***
 
  
 ## LICENSE  
  myled.c is under GNU General Public License v3.0(https://www.gnu.org/licenses/gpl-3.0.ja.html)  
  ***
 
 
 
 
 
 
 
