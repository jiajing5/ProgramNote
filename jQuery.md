* 以Javascript來編寫的函式庫，先幫你實作了很多Javascript的函數功能，用途是讓開發者可以更輕鬆方便的製作網站功能，最重要的是它是免費的。
* 引入jQuery CDN的script必須要放在你的寫的jQuery程式碼的前面
## Selector
* 回傳值的一定是Array
* $("#id")
* $(".class")
* 更改內容
  * $("#id").html("...");
  * $("#id")[0].innerHtml = "...";
* typeof看出 $ 是一個function
## 為避免程式碼順序問題，可將jQuery程式於document ready以後再做
  * 將程式寫在$(document).ready(function(){...})裡面
  * 可縮寫成$(function(){...})
