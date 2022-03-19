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
