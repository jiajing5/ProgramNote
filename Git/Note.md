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
   * git push -u origin main

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

## 遠端儲存庫(Repository)操作
* 註冊遠端儲存庫：git remote add origin 遠端儲存庫網址
* 更新資料到遠端 master 分支：git push -u origin master
* -u 是指他預設會推到哪個遠端數據庫服務
* origin 可以改它的遠端數據庫名稱，例如 *git push -u github master*
* 一個本地數據庫可以綁訂一個以上的遠端數據庫，遠端數據庫名稱不能一樣，可以先推到測試主機上確認沒問題再推到正式主機

## Bitbucket

## Git 版本細節
* branch：分支，預設分支叫做 master
* HEAD：指標，目前當下的位置
* origin：預設遠端儲存庫名稱
* 回頭觀看版本內容：git checkout 編號
* 返回最新的版本：git checkout master(分支名稱)

## 17
* https://www.youtube.com/watch?v=sM2_e8ysjyg&list=PLYrA-SsMvTPOZeB6DHvB0ewl3miMf-2tj&index=17
## 新增檔案時，檔案還沒加追蹤時，清空工作目錄
* 顯示此次清除的檔案：git clean -n
* 強制清除檔案：git clean -f 
## 檔案已加入追蹤，清空工作目錄
* 還原工作目錄上已更改的檔案 ：git checkout -- <file>
## 檔案加入到索引，退到工作目錄
* 加入索引的檔案還原到工作目錄：git reset HEAD
## 版本還原
* 還原前兩個版本：git reset HEAD^^
* 還原前兩個版本，所有更新檔案都放棄：git reset HEAD^^ --hard
* 觀看詳細歷史紀錄：git reflog
* 還原到特定 commit：git reset commit編號 --hard
* git reset 參數介紹 (https://gitbook.tw/chapters/using-git/reset-commit.html)

01~09堂線上講義：https://hexschool.tw/n1C7O
10~18堂線上講義：https://hexschool.tw/PDcLZ
19~25堂線上講義：https://hexschool.tw/qCPbw
26~32堂線上講義：https://hexschool.tw/v9bxz
33~36堂線上講義：https://hexschool.tw/jjq1M

## 20
## branch 介紹
* 分支就像是便利貼，貼在某個 commit 上
* 分支合併，主要是兩個 commit 進行合併
## 開分支流程
* 新增分支：git branch 分支名稱
* 查看分支：git branch 
* 切換分支：git checkout 分支名稱
  * 用git checkout分支名稱時，HEAD也會依照對應位置指定commit位置
* 刪除分支：git branch -d 分支名稱 、-D 是強制刪除
* 還原上個版本：git reset HEAD^ (^以HEAD位置為基準向前還原幾個版本)

## 21
## 合併分支 && 快轉機制
* 合併分支：git merge 分支名稱
* 取消快轉：git merge 分支名稱 --no-ff
   * 產生新的commit，可以知道有做過合併
* 觀看線圖：git log —oneline -graph
* 還原合併前狀態：git reset —hard ORIG_HEAD
## 快轉機制
* 取消快轉：兩個不同任務分支合併時，取消快轉
* 預設使用快轉：本地與遠端兩條相同的任務分支時，可以用快轉

## 23
   * https://www.youtube.com/watch?v=M_ioHIuY2jg&list=PLYrA-SsMvTPOZeB6DHvB0ewl3miMf-2tj&index=23
