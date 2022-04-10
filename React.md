* https://www.youtube.com/watch?v=zqV7NIFGDrQ
## React
* Javascript的UI庫
* 同Vue、Angular，也被稱為JS的「框架」
* 就是用來寫Web應用程式的工具(SPA、SSR)
  * Single Page Application：單頁的應用程式
  * Server Side Render：伺服器渲染的應用程式
* 讓前端專案開發騙得較容易管理
* 頁面組件化，比如一個header同時出現在多個頁面，就寫成元件重複用
* 使用率高的前端框架
* 除了寫Web，也可以寫App
* 查.map() .forEach promise await async 
## React Hook
* 用來簡化class的寫法
## State Hook & Effect Hook
* useState、useEffect
* 用Hook賦予元件「狀態」、「效果」，例如：動態顯示碼錶的時間
* 元件有了狀態(State hook)後，而有了什麼效果(Effect hook)
  * 元件：碼表的介面
  * 狀態：變動的秒數
  * 效果：因為秒數變動了，所以顯示出減少的樣子，或者做其他的事情等等
* useCallback、useMemo、memo
* useContext之Context是什麼
## 讀完需再學習
* React-Router：幫助App換頁
* React Context：管理共用狀態的資訊
* 理解為什麼需要Redux：偏向超大型應用
* 學習Class寫法
## Create React App
* https://zh-hant.reactjs.org/docs/create-a-new-react-app.html
* 
## Node.js
* 是一個執行環境/作業系統的概念(環境安裝包)
* 瀏覽器有直接執行javascript的能力/環境，電腦沒有，javascript沒有環境讓電腦執行，安裝Node.js讓電腦有能力執行js的檔案，電腦就可以連結數據庫或後端，可以把npm npx想像成是建立在Node.js的安裝包/工具
## webpack
* 不管使用什麼工具都會需要webpack打包，例如把箭頭函式轉換成IE看得懂的樣子
* 可以想像成是前端專案的管理器
```javascript
import React from 'react';
// React 可以寫一些API
import ReactDOM from 'react-dom';
// ReactDOM 把寫好的東西畫到頁面上
```
## JSX
* 在函示內寫像HTML的東西
* 在寫React的時候是寫Javascript，寫Javascript要表現畫面的話是用物件表現，不夠方便，JSX可用HTML的寫法建立React要求的物件
* 
