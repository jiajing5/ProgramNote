* box-sizing 是控制 width 與 height 作用的對象空間，設定物件尺寸的計算方式
  * Content-box (預設值，寬高設定作用在內容範圍)
  * Border-box （寬高設定作用在邊框外緣的範圍內，padding 與 border 會直接內推）
* box-shadow : offset-x offset-y blur-size spread-size color
* 強制換行 word-wrap : break-word
* 使用clear可以清除float產生的浮動，注意clear樣式物件加入位置，需要在物件div標籤結束前加入即可清除內部小盒子產生浮動
  * none : 允許兩邊都可以有浮動物件
  * both : 不允許有浮動物件
  * left : 不允許左邊有浮動物件
  * right : 不允許右邊有浮動物件
