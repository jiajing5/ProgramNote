## Application Programming Interface 應用程式介面
* 維基百科對 API 的定義：在電腦程式設計裡，應用程式介面 (API) 是用於打造應用程式軟體的一組副程式定義、協定與工具。一般而言，API 是指各種軟體組件之間一套明確定義的溝通方法。好的 API 提供模塊，並且由工程師將它們組合在一起，如此一來讓寫程式變得更簡單。
## 介面 (Interface)
* 「人」作為一個主體，如果人要去使用機械、物品或是應用軟體，人無法直接和這些東西進行互動，因此需要有一個「介面」，來讓兩個主體之間可以溝通。
* 例如，收音機的調頻按鈕、咖啡機的控制面板、Google Maps 的前端網頁
## API 的使用者
* 正在開發軟體應用程式的工程師
* Google Maps API 讓開發者能和 Google Maps 系統溝通，取得 Google Maps 的資料
## Web API 與 HTTP
* 在 Web Application 的開發情境下的 API 被稱為 Web API，在 Web API (Google Map API)作用時，客戶端(例，餐廳網頁)和伺服器端(Google Map)會透過 HTTP 通訊協定來進行請求與回應。
## HTTP 通訊協定
* HTTP (HyperText Transfer Protocol) 是通訊協定 (Transfer Protocol) 的一種，通訊協定制定了規則和標準，讓設備之間不但能認出彼此，也能夠根據不同情境選擇溝通的方式，而 HTTP 是專門用於瀏覽器與伺服器之間的通訊協定。
* 根據 HTTP 規範，伺服器端和客戶端進行請求與回應時，會使用定義明確的請求格式 (request format) 和回應格式 (response format)。
  * Request format：客戶端需要使用特定的 HTTP 動詞，對 URL 發出請求，例如Rails 採用的 RESTful
  * Response format：伺服器端回應時採用的資料格式，API 的設計者可以自行決定資料回傳的格式，例如XML、JSON、Protocol Buffers、Thrift、YAML 等等
    * XML：Extensible Markup Language，是一種標記式 (markup) 語言，使用 < > 定義標記，標記的頭尾之間夾帶著內容，可以想像成是 HTML 標籤語法的延伸。
    * JSON： JavaScript Object Notation 的縮寫，它參考了 JavaScript 中物件結構的表示方式。
* https://tw.alphacamp.co/blog/api-introduction-understand-web-api-http-json
## HTTP status code
* 這些代碼對 SEO 會有相當程度的影響
* 2開頭代表連線成功
* 3開頭代表轉址
  * 假設使用者搜尋某關鍵字，連到 A 頁面被轉址到 B 頁面：
    * 如果是 301 永久轉址 --> 該關鍵字的流量會被算在 B 頁面
    * 如果是 302 暫時轉址 --> 該關鍵字的流量會被算在 A 頁面
* 4開頭代表有錯誤
* 5開頭則是表示伺服器有問題
  * 如果網站伺服器回應太多4或5開頭的錯誤代碼，搜尋引擎也會降低網站的 SEO 評價
## 伺服器（server）
* 俗稱的網站主機，是一種特殊用來回應客戶端 request 的電腦，這種電腦不需要螢幕，因為它跟一般電腦不一樣，不需要給人看，只跟機器溝通
* 伺服器也是電腦，跟一般電腦一樣也需要安裝作業系統，市面上目前以 Linux 、Unix 和 Windows （不是家用電腦作業系統，而是微軟針對伺服器特別出的作業系統）三種為主流，所以當你聽到某工程師要用 Linux 架 server ，意思就他要在電腦上安裝 Linux 這套作業系統，並且把這台電腦當作伺服器來接收來自世界各地客戶端的 request。
* 除了作業系統之外，伺服器還需要安裝一套軟體，這樣工程師才方便管理伺服器，比較為人熟知的有 Apache 跟 Nginx。
* 網路上所看到的影片、圖片還有各式各樣的檔案（這些檔案稱之為資源），都存放在實體的伺服器中，當我們連線到這些網站或服務時，客戶端就發出了 request 給伺服器，伺服器再根據 request 給出相對應的回應，而回應中通常會包含一些資源。
* 除了檔案，伺服器上面還存有資料庫，你可以把資料庫想像成是 excel 的表格，上頭有各式各樣的欄位記錄，以 Facebook 的伺服器來說，裡面會有資料庫儲存每個使用者的 ID 、朋友、照片、曾經發過的貼文等等。
## CDN（Content Delivery Network）
* 伺服器跟客戶端的距離會影響連線速度，為了解決這類型的問題，於是就有了 CDN
* CDN 是一種快取機制，是「透過節點伺服器減輕主伺服器負擔，並增快連線速度的一種方法」，例如，原本我們連 Facebook 每次都要連美國主機，但因為 Facebook 在亞洲各區設有 CDN 伺服器，我們只要連到距離比較近的 CDN 伺服器，就可以讀取到一模一樣的內容，而且速度更快。
## DNS（Domain Name Server）
* 每個網站伺服器在網路上都有一個地址，這個地址就是所謂的 IP 位置，IP 是由一串數字所組成，但是這長串數字實在太難記了，對人類完全沒有可讀性可言，所以用域名替代 IP，當我們連到 yahoo.com 的時候，事實上是連到位置在 98.138.253.109 的主機
* DNS 是專門用來把域名解析成 IP 的伺服器
* https://tw.alphacamp.co/blog/2016-10-25-coding-basics-for-marketers-1
* 
