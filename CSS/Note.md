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
## 英文字間距
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
## 裁切圖片
*  position:absolute;
*  clip:rect(10px,290px,290px,10px);
   *  position 固定裁切的位置，值：上、右、下、左(上、下的起點是上方為 0，右、左的起點是左邊為 0)
## 捲軸
* 透過 overflow 的設定，可以讓圖片或文字區塊在固定的範圍內呈現，如果超出範圍的話會自動變成捲軸呈現方式(隱藏超出父元素的子元素)
  * overflow: auto; //預設會自動使用捲軸
  * visible; //顯示的文字或圖片會直接超出範圍，不使用捲軸
  * hidden; //自動隱藏超出的文字或圖片
  * scroll; //自動產生捲軸
  * inherit; //繼承自父元素的可見性
    * overflow-x:hidden; //隱藏水平捲軸
    * overflow-y:auto; //顯示垂直捲軸
## position 定位 https://www.runoob.com/css/css-positioning.html
* 設定「物件定位時所要的參考對像」
* static (靜態定位)：
  * HTML 元素的默認值，即沒有定位，遵循正常的文檔流對象。
  * 不會受到 top, bottom, left, right影響。
* relative (相對定位)：
  * 相對定位元素的定位是相對其正常位置，但它原本所佔的空間不會改變。
* fixed (固定定位)：
  * 元素的位置相對於瀏覽器窗口是固定位置，即使窗口是滾動的它也不會移動。
  * 使元素的位置與文檔流無關，因此不佔據空間，Fixed定位的元素和其他元素重疊。
* absolute (絕對定位)：
  * 絕對定位的元素的位置相對於最近的已定位父元素，如果元素沒有已定位的父元素，那麼它的位置相對於<html>。
  * 會從資料流中抽離，不佔據空間，absolute 定位的元素和其他元素重疊。
* sticky (黏貼定位)：
  * 基於用戶的滾動位置來定位。
  * 它的行為就像 position:relative; 而當頁面滾動超出目標區域時，它的表現就像 position:fixed;，它會固定在目標位置。元素定位表現為在跨越特定閾值前為相對定位，之後為固定定位。
  * 指定 top, right, bottom 或 left 四個閾值其中之一，才可使粘性定位生效。
## z-index 
* 設定元素的堆疊順序，設定值越高越前面，可以為負數，例如：z-index: -1。只能在有設定位（position）的元素上才會奏效。可為position: static、absolute、relative、fixed。
## 字體
* Google Font https://fonts.google.com/
* @font-face 
  * @font-face {
  font-family: Gentium;
  src: url(http://example.com/fonts/Gentium.woff);
}
  * p { font-family: Gentium, serif; }
  * /* Gentium 字型 */
  * @font-face {
  font-family: MyGentium;
  src: local(Gentium),    /* 指定使用者電腦中的 Gentium 字型 */
       url(Gentium.woff); /* 如果使用者電腦中找不到，則從網路下載 */
}
## text-decoration
* text-decoration:none; //預設值，無額外文字特效
* overline;	//文字增加上線特效
* underline;	//文字增加底線特效
* line-through;	//文字增加刪除線特效
 
 ## 使用 CSS border 製作梯形、三角形、對話框
 * https://www.footmark.com.tw/news/web-design/css/css-border-create-triangle/
 
 ## 小圖示變色
 * https://www.gushiciku.cn/pl/20XH/zh-tw
 * 使用亮度濾鏡
   * 圖示變黑色
.black {
    filter: brightness(0);
}
   * 圖示變白色
.white {
    filter: brightness(100);
}
* 使用遮罩 mask
## Selector https://developer.mozilla.org/zh-TW/docs/Glossary/CSS_Selector
* 鄰接同層選擇器 A + B
* 通用同層選擇器 A ~ B
* 直屬選擇器 A > B
* 後代選擇器 A B
* :first-child是CSS當中的一種偽類別（pseudo-class），代表任何身為長子的元素（親元素的第一個子元素）。
* :first-of-type 代表本節點為兄弟節點中第一個此類型節點。
## grid
* https://nicolakacha.coderbridge.io/2020/09/22/css-flex-grid-2/
## 轉換theme
* 用css variable轉換theme https://medium.com/@haxzie/dark-and-light-theme-switcher-using-css-variables-and-pure-javascript-zocada-dd0059d72fa2
* 連結各別theme的css檔案轉換theme https://www.youtube.com/watch?v=dOIU773P1iw
## 色碼轉換器
* https://www.peko-step.com/zhtw/tool/hslrgb.html
## creat On/Off FlipSwitch
* https://proto.io/freebies/onoff/
