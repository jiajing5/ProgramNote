* https://www.youtube.com/watch?v=-O9bOlwd2nY&list=LL
* Java物件導向程式設計
## 1-1 程式
* Java程式語言執行過程：將Java程式經過編譯器編譯成Java的Bytecode(位元組碼)，再經由Java的虛擬機器(Java Vritual Machine, JVM)給我們的電腦硬體執行
## 1-2 安裝JDK
* JDK由oracle維護
## 1-3 安裝eclipse和IntelliJ
* eclipse：開發工具、撰寫Java程式
  * 新增專案：File>New>JavaProject
  * 新增Package套件(分類程式的地方，Name用"網域顛倒.名稱")：File>New>Package

## 3 撰寫第一支Java程式
* https://www.youtube.com/watch?v=DEtickir3AE&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=3
  * 新增第一個程式class類別(慣例首字大寫)：File>New>class
  * 開啟檔案撰寫第一個程式
    * Window>Show View>Project Explorer 可以開啟左邊頁籤
    * 放在package內的話就要寫 package testJava;
    * 程式進入點 public static void main(String[] args) {}
    * 執行程式 Run>Run as>Java Application
* IntelliJ：

## 4 基本型別與變數
* https://www.youtube.com/watch?v=S7yyN7Ev2ZY&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=4
* 變數型別關鍵字 byte
``` java
byte var2 = 12;
```
* 變數名稱首字為英文字/錢字號/底線
## 5 基本型別 - 布林值 (boolean)
* https://www.youtube.com/watch?v=oDO5lrsJoPM&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=5
* boolean
  * true/false
``` java
boolean var1;
var1 = true;
var1 = false;
```
## 6 基本型別 - 字元
* https://www.youtube.com/watch?v=UHIZZob_VuM&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=6
* char
  * 佔2^16
  * 0-65535
  * 可以進行整數運算
  * 96
  * 'a'
  * '\uxxxx' (\u+十六進位的數字)
``` java
char var1 = 97;
System.out.println(var1);
//印出a，97是a的ASCII code
char var2 = 'b';
System.out.println(var2);
char var3 = '\u6587';
System.out.println(var3);
//印出'文'
```
## 7 位元組
* https://www.youtube.com/watch?v=wnkefVByIz4&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=8
