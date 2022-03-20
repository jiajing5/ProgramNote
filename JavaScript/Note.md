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
