* 高寬度間距字用rem
## box-sizing 
* 控制 width 與 height 作用的對象空間，設定物件尺寸的計算方式
  * Content-box (預設值，寬高設定作用在內容範圍)
  * Border-box （寬高設定作用在邊框外緣的範圍內，padding 與 border 會直接內推）
## box-shadow : offset-x offset-y blur-size spread-size color
## 強制換行 
*　word-wrap : break-word
## 使用clear可以清除float產生的浮動
* 注意clear樣式物件加入位置，需要在物件div標籤結束前加入即可清除內部小盒子產生浮動
  * none : 允許兩邊都可以有浮動物件
  * both : 不允許有浮動物件
  * left : 不允許左邊有浮動物件
  * right : 不允許右邊有浮動物件
## 在段落或者標題中的文稿內居中字句 text-align : center
## 行距 line-height
* 數值為"文字大小+上下增高的px"或"文字大小的倍數"
## 單位
* px：絕對單位，代表螢幕中每個「點」( pixel )。
* em：相對單位，每個子元素透過「倍數」乘以父元素文字的 px 值。
* rem：相對單位，每個元素透過「倍數」乘以根元素文字( html的font-size，預設為16px )的 px 值。
* %：相對單位，每個子元素透過「百分比」乘以父元素的 px 值。
## Chrome不支持css字體小於12px的解決辦法
* .small-font{
  font-size: 12px;
  -webkit-transform: scale(0.5);
}
* 兼容IE、FF要加上
.smallsize-font{
  Font-size: 6px;
}
  * transform:scale()這個屬性只可以縮放可以定義寬高的元素，而行內元素是沒有寬高的，我們可以加上一個display:inline-block;屬性
## 文字間距
* letter-spacing 字元間距控制 (每個字之間的距離控制)
* word-spacing 單字間距控制 (每個單字之間空白區的大小控制)
* white-space 空白區域處理
## flex
* flex-grow：依照設定比例分配剩餘空間
* flex-shrink：空間不夠時的壓縮比例
* flex-basis：表示其預設分配到的空間，與 width 很像，但優先程度較高
## 漸層
* https://www.oxxostudio.tw/articles/202008/css-gradient.html
* 可以套用漸層的 CSS 屬性有兩種，分別是：
 * background：元素的背景 ( 最常遇見 )
 * list-style-image：清單預設的符號圖案 ( 通常可用偽元素取代 )
* background:linear-gradient(方向, 顏色1 位置, 顏色2 位置); 
## 背景漸變和自動全屏
* body{
    background-image:-webkit-linear-gradient(60deg,rgba(218, 169, 215, 0.637),rgba(128, 174, 235, 0.904));
    background-position: center 0;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-size: cover;
    -webkit-background-size: cover;
    -o-background-size: cover;
    -moz-background-size: cover;
    -ms-background-size: cover;
}
