## Asynchronous JavaScript and XML
* 一套綜合性的瀏覽器端網頁開發技術
* Asynchronous：非同步
* JavaScript：使用的程式語言
* XML：Client 與 Server 交換資料用的資料與方法，近年由於 JSON 等格式的流行，使用 Ajax 處理的資料並不限於 XML
* 最早期的 Ajax 會利用 XMLHttpRequest 物件 ( XHR ) 來實作，但使用起來很麻煩，所以實務上很少直接使用原生的 XMLHttpRequest
* 取而代之的方法有很多種，過去較流行的是 jQuery 的 $.ajax()
* 新的替代方案
  * 例如 HTML5 提供 Fetch API
  * axios 是一個非常受歡迎的 JavaScript 函式庫，他有許多重要功能如：
    * 廣泛的瀏覽器支持
    * 可支援 Node.js 從後端發送的 Http request，意味著 axios 可以兼用於前端與後端專案
    * 直接將回應的 JSON 資料轉換成 JavaScript 的 Object
