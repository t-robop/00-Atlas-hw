# 00-Atlas-hw（旧ScriptArduinoRC）
スクリプト組み立て型のArduinoラジコンシステム (Arduino側プログラム)   

コントローラーアプリ側のプログラム : https://github.com/t-robop/ScriptRobotController   

# 目的
GUIでプログラムのフローチャートを作って、ラジコンを動かす　⇛　自分の思い通りの動作を実行させるための論理的思考力を養おう

# 開発中で使用する用語
orderId : ラジコンに対する動作命令    
      1 : 前進  2 : 後退  3 : 左回転  4 : 右回転    
Time : 動作命令の実行時間    
Speed : 動作命令のモータパワー値

# 実装内容   
## A実装   
- Bluetoothで送られてきた文字列の読み込み ← Done!     
- 文字列を処理ごとに分けて正規化 ← Done!    
- 正規化後の文字列を元に処理を分けてモータ動作 ← Done!

## B実装
- for文ブロックへの対応     
- 値設定箇所のデザイン周り

## C実装  

# 扱うデータ  
例: 102100100 (1命令分) (9byte)    

   1桁目 -> imageId    
   2,3桁目 -> Time    
   4,5,6桁目 -> Speed (右回転)     
   7,8,9桁目 -> Speed (左回転)    

   モータ値100で2秒間前進
