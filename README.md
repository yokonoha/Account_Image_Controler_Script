# Account_Image_Controler_Script
[J]ローカルストレージ領域にアカウントシステムを作り、そこにユーザー画像を登録するスクリプト  
## What is this?  
https://github.com/yokonoha/Account_System_Integration_Script  
↑コレと一緒に使うスクリプトです。このスクリプトではローカルストレージにアカウントシステム"らしきモノ"を作り、そのユーザーアイコンとしてエンドユーザーに任意の画像を登録させることが出来るスクリプトです。(...????)  
これが一体なぜ必要だったのかは、以下のサイトをご覧ください。  
https://caffeineapps.pages.dev/account  
だいぶ前に作ったので仕掛けを詳しく覚えておらず、[J]なコード(ジャンク)扱いです。使えるよというすごい方はこのリポジトリにてMITライセンスで配布していますので、ご活用下さい。  

実装例
```koredeiikana.html
<!--CaffeineAppsより引用-->
    <div class="G">  
<h3 id="002">アカウントユーザー画像設定</h3>
<img src="./ic2.png" width="40%" id="acimg2" style="border-radius: 500px;">
<canvas id="kagemusya" width="400px" height="400px" style="display: none;"></canvas>
<br>
<p id="010">設定したい画像を選択してください。画像はデバイス内で処理され、デバイス内に保存されます。</p>
<input type="file" accept="image/*" id="import">
    </div> 
```
御利用にはCanvas要素が必要です。Base64に変換するために使います。(ユーザーに見せるものではないので、CSSのdisplay値はnoneにセットされています。)  
こだわりは、どんなサイズの画像を読み込まれても引き延ばしを起こさないようにしたこと だったと思います!(遠い記憶)
