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
