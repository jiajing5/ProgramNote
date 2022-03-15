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
* 在段落或者標題中的文稿內居中字句 text-align : center
* 行距 line-height 數值為"文字大小+上下增高的px"或"文字大小的倍數"

* px：絕對單位，代表螢幕中每個「點」( pixel )。
* em：相對單位，每個子元素透過「倍數」乘以父元素文字的 px 值。
* rem：相對單位，每個元素透過「倍數」乘以根元素文字( html的font-size，預設為16px )的 px 值。
* %：相對單位，每個子元素透過「百分比」乘以父元素的 px 值。

* 高寬度間距字用rem
