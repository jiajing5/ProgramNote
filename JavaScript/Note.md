## Screen.width 
* The read-only property returns the width of the screen in CSS pixels.
* https://dotblogs.com.tw/puma/2009/04/02/javascript-width-height-clientwidth-availwidth-screen
## DOM的事件傳遞機制
1. capture phase
2. target phase
3. bubbling phase
* https://blog.techbridge.cc/2017/07/15/javascript-event-propagation/
* addEventListener
  * 有第三個參數，true代表把這個 listener 添加到捕獲階段，false或是沒有傳就代表把這個 listener 添加到冒泡階段。
* event.stopPropagation()
  * 阻止事件繼續冒泡
* event.preventDefault()
  * 停止事件的默認動作 (例如：阻止a標籤的超連結)
* Once preventDefault has been called it will remain in effect throughout the remainder of the event's propagation.
## test()
* 用於檢測一個字符串是否匹配某個模式，如果字符串中有匹配的值返回 true，否則返回 false
* 正則表達式驗證email格式
  * https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_Expressions
  * const regexMatch = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/.test(email.value)
## match()
* 搭配正規表示式 (Regex)來找出字串中匹配的內容
* 返回一個陣列，第一個元素是完整匹配內容，接著是匹配的群組 (capturing group)；如果沒有匹配則返回 null。
* str.match(regexp)
## 常用事件 event
* https://medium.com/%E9%A6%AC%E6%A0%BC%E8%95%BE%E7%89%B9%E7%9A%84%E5%86%92%E9%9A%AA%E8%80%85%E6%97%A5%E8%AA%8C/js-%E4%BA%8B%E4%BB%B6%E7%AD%86%E8%A8%98-%E4%B8%8B-68c7596cb4bc
## Trigger a Button Click on Enter
* https://www.w3schools.com/howto/howto_js_trigger_button_enter.asp
## toFixed()
* 可把 Number 四捨五入為指定小數位數的數字
## slice()
* The slice() method returns a shallow copy of a portion of an array into a new array object selected from begin to end (end not included). The original array will not be modified.
  * arr.slice(begin)
  * arr.slice(begin, end)
## splice()
* The splice() method changes the contents of an array by removing existing elements and/or adding new elements.
* 回傳被刪除的項目。
  * array.splice(start)
  * array.splice(start, deleteCount)
  * array.splice(start, deleteCount, item1, item2, ...)
    * start 增加/刪除項目的位置，負數代表從後方算起。
    * deleteCount 刪除的個數，如為0則不會刪除。
    * item… 添加的新項目。
## split()
* The split() method splits a String object into an array of strings by separating the string into substrings.
* 分割字串成字串組
  * stringObject.split(separator,howmany)
    * separator 字串符或正則表達式，從該參數指定的地方分割stringObject。
    * howmany 返回值的最大長度，超過該長度則不顯示。
* https://medium.com/@bebebobohaha/slice-splice-split-%E5%82%BB%E5%82%BB%E5%88%86%E4%B8%8D%E6%B8%85-46d9c8992729
## 模組管理
   * 將每個檔案視為一個獨立的模組匯出，並在另一個檔案匯入使用
   * https://www.casper.tw/development/2020/03/25/import-export/
* export
  * named export（具名匯出）：可匯獨立的物件、變數、函式等等，匯出前必須給予特定名稱，而匯入時也必須使用相同的名稱。另外，一個檔案中可以有多個 named export。
  * default export（預設匯出）：一個檔案僅能有唯一的 default export，而此類型不需要給予名稱。
    * 兩者也可共存於同一個檔案內，只不過 default export 僅能有一個。
    * 
* import
  * 會因為匯出方法不同而改變
* Side Effect 模組
  * 有些模組並沒有實作 export，例如可直接執行的函式檔案，載入後會直接執行，不需要例外的呼叫
* 
## innerText
* 代表節點及其後代之「已渲染」（rendered）文字內容，display: none 的字不會顯示，和 HTML 渲染後呈現的樣子相像
## innerHTML
* 取得在一個節點內完整的標籤和文字，包括原始碼的換行
## textContent
* 取得在一個節點內的文字並包括換行，會取得呈現在 HTML 原始碼內的換行、空格和文字， <br> 會忽略，取得的文字與換行會和原始碼相像
## outerHTML
* 包括節點和節點內的全部 HTML 標籤和文字
## createTextNode()
* 要注意在建立新節點後，只有 textContent 是唯一可用方法
* https://orandigo.github.io/blog/2020/03/22/20200322-innerText-innerHTML-textContent-outerHTML/
* 
