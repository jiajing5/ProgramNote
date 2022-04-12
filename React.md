* https://www.youtube.com/watch?v=zqV7NIFGDrQ
* 1:23:40
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
## code
* 在箭頭函式中return JSX就會被視為一個js元件
* Home (State 狀態共享給Edit跟List，把data透過props傳遞)
  * Edit
  * List
    * Item
## CSS
* 可用物件方式寫
```javascript
const app = {
color:'red'
}
// 帶入JSX
<div style={app}></div>
```
* 其他第三方部件 styled-components
  * 可以把元件跟CSS寫在同一個javascript裡的方式
* 用純CSS
  * 寫入class用className
  ```javascript
  <div className="app"></div>
  ```
## 用陣列及arr.map重複產生item
* 要在JSX寫javascript都要加一個大括號
``` javascript
import Item from "./item"
const arr = [1, 2, 3]
const List = () => {
    return <div className="list">
    {
        arr.map(item => <Item/>)
        //會顯示
        //item
        //item
        //item
    }
    </div>
}
```
``` javascript
import Item from "./item"
const arr = [1, 2, 3]
const List = () => {
    return <div className="list">
    {
        arr.map(item => <div>{item}</div>) 
        //會顯示
        //1
        //2
        //3
    }
    </div>
}
```
* 會拿到一個陣列資料
* React希望用map函式渲染的時候要幫item加key上去
``` javascript
const List = ({ listData }) => {
    return <div className="list">
    {
        arr.map(item => <Item key={item} />)
    } 
    //key像是對item貼標籤，標籤要是獨一無二才能辨識出item，可以效能優化，不能用index因為內容改變的話react就要重新認識，會耗效能
    </div>
}
```
## useState 狀態
* 切版的時候要思考怎麼切各個不同元件，可以幫助去想狀態要怎麼分
* 在Home新增狀態
  * import { useState } from 'resect'
  * React第二個單字開頭要用大寫
  * 直接寫javascript的變數的話，ReactDOM會不知道跟React畫面有關，就不能改變變數，要讓變數給ReactDOM知道要重新渲染元件，要用useState
``` javascript
const [a, setA] = useState(100)
// const [變數, 對應的函式] = useState(初始值) 
function plus(){
setA(200) //直接把a變成200
}
//JSX
<button onClick={plus}>加法</button>

```
``` javascript
const [a, setA] = useState(100)
// const [變數, 對應的函式] = useState(初始值) 
function plus(){
 setA(function (prev) {
  return prev + 200
 })
}
//如果要寫多次setA(a+200)，會不準確，所以要透過變數拿到上一個值做準確的加減，例如a初始值100，點擊button後會+200，a變成300
//JSX
<button onClick={plus}>加法</button>

```
* 
## 討論Edit部分 1:20:30
* 取得input的值
  * 用javascript onchange事件 Linstener 拿到event.target.value
  * doucment.getElementById直接拿value
* 在React內寫的操作都要跟狀態變動有關才能拿到結果
  * 讓input各自綁定一個useState
* 要取得上一個值再塞入現在的data
``` javascript
function addItem() {
    add(function (prevData) {
      return [
        ...prevData,
        {
          note,
          date,
          time,
        },
      ];
    });
  }
```
## Item的部分
* 從List傳入{ note, date, time }
## List的部分
* 用解構賦值取出 const{note, date, time} = item
## npm包
* npm i prettier
  * 讓程式碼變漂亮，可以到官網查詢如何設定方法，例如變更單引號、建立標準化樣式
  * 到package.json的script新增"prettier":"prettier -w src/"
* uuid npm
  * npm install uuid
  * 產生唯一的ID
  * import { v4 } from 'uuid';
## deleteItem
  * ES6有一個API叫filter，可以過濾掉當前id並保持順序
  * 把當下item的id做比對，不等於就讓他回到陣列裡面
  * return prev.filter(item => item.id !== id)
* 把新增的東西新增在最上面要把解構陣列放在後面
``` javascript
function addItem() {
    add(function (prevData) {
      return [
        {
          note,
          date,
          time,
        },
        ...prevData,
      ];
    });
  }
```
## useEffect 1:43:20
1. 某個狀態或變數有變動後，要做什麼事情，例如data變動後跳出彈窗
  * 綁定data(依賴)，function有用到的話都加進去
``` javascript
useEffect(() => {
  window.alert("新增成功")
}, [data])
```
2. 清除內容
  * 外面的function是每次執行時會做的事
  * 裡面的function是每次渲染結束後要開始下一次新的渲染會做的事
``` javascript 
  useEffect(() => {
    // 綁定的事情
    return() => {
      //取消綁定
    }
  }, [data])
```
3. 只希望執行一次，但每次渲染都會執行，例如從後端拿資料
  * 不綁定
``` javascript 
  useEffect(() => {
   console.log('here')
  }, [])
```
## 讓useEffect拉API，拿到後端資料，安裝json server
* 模擬後端的工具
* npm i npm i json-server
* 參考官方文件
* 在資料夾建立一個db.json檔案
* 到package.json的script加入"server":"json-server --watch db.json"
* 到命令提示字元進入資料夾輸入npm run server
  * 會根據db.json的檔案執行
* 用fetch方式拿後端資料後，透過fetchData的方式去set到狀態裡
``` javascript 
useEffect(() => {
    fetch("http://localhost:3000/posts/1")
    .then(res => res.json())
    .then(data => {
    console.log(data);
    })
  }, [])
```
* 在global資料夾建立constants.js管理變數export
``` javascript 
useEffect(() => {
    fetch(API_GET_DATA)
    .then(res => res.json())
    .then(data => {
    console.log(data);
    })
  }, [])
```
* 可以用async function讓程式碼更簡潔，可以拿到跟原本一樣的東西
* useEffect內不支援async的方式，只能用.then
``` javascript
async function fetchData(setData){ //把setData放進當參數
  const res = await fetch(API_GET_DATA) //拿到response
  const {data} = await res.json()//用jason函式解構出來，拿到{data}
  // console.log(data);
  setData(data)
}
useEffect(() => {
  fetchData(setData)
}, [])
```

* 
