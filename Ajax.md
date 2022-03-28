## Asynchronous JavaScript and XML
* 一套綜合性的瀏覽器端網頁開發技術
* Asynchronous：非同步
* JavaScript：使用的程式語言
* XML：Client 與 Server 交換資料用的資料與方法，近年由於 JSON 等格式的流行，使用 Ajax 處理的資料並不限於 XML
##同步請求 (Synchronous request)
* 客戶端 (client) 對伺服器端 (server) 送出 request ，並且在收到伺服器端的 response 之後才會繼續下一步的動作，等待的期間無法處理其他事情。這個作法並不理想，因為通常伺服器端的運算速度比本地電腦慢上好幾倍。
## 非同步請求 (Asynchronous request)
*　客戶端 (client) 對伺服器端 (server) 送出 request 之後，不需要等待結果，仍可以持續處理其他事情，甚至繼續送出其他 request。Responese 傳回之後，就被融合進當下頁面或應用中。
## Ajax 實現非同步請求
* 最早期的 Ajax 會利用 XMLHttpRequest 物件 ( XHR ) 來實作，但使用起來很麻煩，所以實務上很少直接使用原生的 XMLHttpRequest
* 取而代之的方法有很多種，過去較流行的是 jQuery 的 $.ajax()
* 新的替代方案
  * 例如 HTML5 提供 Fetch API
  * axios 是一個非常受歡迎的 JavaScript 函式庫，他有許多重要功能如：
    * 廣泛的瀏覽器支持
    * 可支援 Node.js 從後端發送的 Http request，意味著 axios 可以兼用於前端與後端專案
    * 直接將回應的 JSON 資料轉換成 JavaScript 的 Object
## 用 axios 發送 GET Requests
* axios.get(url)
* then() 函式負責處理成功接收到的 response，response 參數就是接收到的回應，而所需的資訊則放置在 response.data 裡面
* catch() 函式負責處理發生錯誤的狀況，也就是 error
