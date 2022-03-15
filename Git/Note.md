學習筆記-YouTube六角學院的Git、GitHub教學
# Git & GitHub 入門
* 線上講義https://quip.com/pFUnA7u75HbL
## 終端機
* Win：*Git Bash*
    * 開始 > 搜尋輸入 > Git Bash
* Mac：*終端機*
    * 輸入「control + 空白」，關鍵字輸入「終端機」

## 終端機指令(開新的資料夾就要輸入)
* 前往要做版本控制的資料夾：cd
* 對資料夾做版本控制、初始化數據庫：git init (會出現.git隱藏檔，開啟本地數據庫)

## 嘗試 Git 是否有安裝成功
* 確認git是否安裝成功：git --version

## 設定個人資料(第一次開資料夾時輸入即可)
* 輸入姓名：git config --global user.name "gon"
* 輸入個人的 email：git config --global user.email "gonsakon@gmail.com"
* 查詢 git 設定內容：git config --list
* list檢視完回到指令狀態：按鍵盤小寫的q

## 基本指令架構
* 工作目錄working directory →add→ 索引staging area →commit→ 本地數據庫local repository →push→ 遠端數據庫remote repository
* 查看資料夾目前狀態：git status
* 在資料夾新增的檔案一開始會在工作目錄中，把要更新的檔案放入索引區讓git知道哪個檔案要加入這次更新
* 將檔案加入到索引：git add .
* 將索引檔案變成一個更新(commit)，進入到本地數據庫：git commit -m "修改內容"
* 觀察 commit 歷史紀錄： git log
* 下載遠端數據庫： git clone 數據庫網址
* 更新遠端數據庫： git push origin master
   * push為更新遠端數據庫
   * origin為遠端數據庫名稱

## Sourcetree

## 推資料上GitHub遠端數據庫 
* 建立遠端數據庫
* 在git bash輸入指令綁定資料夾
* 在資料夾.git > config確認有無綁定
* 在git bash輸入指令把資料推上去

## 讓別人可以看到網頁，變成靜態網頁source
* Settings > GitHub Pages > Source > master branch


# Git 遠端  Repository 操作
* 線上講義https://quip.com/GL4gAFIc2KdI

## 常用環境設定
* 編輯器更換：git config --global core.editor "code --wait"
* Git 縮寫：
    * $ git config --global alias.co checkout
    * $ git config --global alias.br branch
    * $ git config --global alias.st status
    * $ git config --global alias.ci commit
      * git config：設定git的一些基礎設定
      * --global：希望這台電腦都可以知道這個設定
      * alias.st：要設定的關鍵字是st，會等於空白右邊的status
* config --list 可以看是否改好
* 觀看所有 config 的設定：
    * Mac：~/.gitconfig
    * Win：C:\Users\$USER

## 11 https://www.youtube.com/watch?v=kajih2OHig0&list=PLYrA-SsMvTPOZeB6DHvB0ewl3miMf-2tj&index=11

