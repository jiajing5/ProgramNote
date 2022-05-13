* 文字教學
* https://yubin551.gitbook.io/java-note/
* Java程式設計教學 (新手)
* https://www.youtube.com/playlist?list=PLTb8yNz82VDW-Ka3DMZUvhf16zZCPFiGe
* Java程式設計教學 (初級)
* https://www.youtube.com/playlist?list=PLTb8yNz82VDVmwVPKbrylbitOnXZRlxFo
* 
* Java物件導向程式設計

## 1-1 程式
* https://www.youtube.com/watch?v=-O9bOlwd2nY&list=LL
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

## 1 Java 建置開發環境 (一) 瞭解所需工具
* https://www.youtube.com/watch?v=2pCUIryNx0I&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=1&t=2s
* 命令列程式語言
* Java SE(standard version) => Java標準版本
  * JDK(Java Develop Kit) => Java開發工具
    * 內含JRE(Java Runtime Environment) => Java執行環境
  * JRE(Java Runtime Environment) => Java執行環境(不需要開發時)
* IDE(Integrated Develop Environment) => 整合開發環境
  * NetBeans => Apache
  * Eclipse

## 2 Java 建置開發環境 (二) 下載所需要的檔案
* https://www.youtube.com/watch?v=BciK_NlTN5g&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=2
* 1.搜尋Java JDK
  * 下載8的版本
* 2.搜尋Eclipse下載

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
  * 0-65535 (字元無正負號，故從0開始)
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
* byte的範圍-128~127之間
* short的範圍-32768~32767之間

### 基本與參考資料型態差異
* https://yubin551.gitbook.io/java-note/basic_java_programming/datatype/primitive_reference_difference
* 記憶體區間：在執行時期可分為三個部份
  * 1.Global 全域：
    * 用來放全域變數(global variable)、靜態變數(static variable)。
  * 2.Stack 堆疊區：
    * 作業系統會自動化管理這個區塊，而要讓系統可以清楚的管理這些資訊，代表裡面存放的東西必須事先可以被計算好它的生命週期。這個區塊主要用來存放：區域變數(local variable)、方法的參數(method parameter)與方法的回傳位址(method return address)等。
    * 上述這些東西在編譯時期就可以決定好生命週期，所以系統會管理什麼時候要回收資源。如果Stack區不夠用或是遞回涵式(recursive function)沒寫好，會產 StackOverflowError 。
``` java
// 基本資料型態的宣告及給值： (int為例)
int value ;
value = 10;
```
  * 3.Heap 堆積區：
    * 可以被預測的資料放在堆疊區(Stack Memory)，而不可被預測的資料就放在堆積區(Heap Memory)。很多時候程式在執行時期才會知道要使用多少記憶體，而且該區塊的記憶體不知道什麼時候會不需要使用，通常透過new關鍵字的東西會被存放在這邊(c++也是，c的話就是malloc()及calloc()。)
    * 這裡的資料系統不會自動回收，所以隨著程式執行記憶體會越來越少，所以程式設計師必須自行管理此區的記憶體，但Java有『Garbage Collection 垃圾回收』機制，會幫你檢查哪部份的記憶體已不在使用，就會幫你釋放那部份的記憶體空間。倘若Heap區記憶體不夠用，會產生OutOfMemoryError。
``` java
// 參考資料型態的宣告及給值： (假設有個自訂類別Human)
Human tina;
tina = new Human();
```
## 8 整數 int 運算
* https://www.youtube.com/watch?v=PSyalXdy97E&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=8
``` java
int var1 = 10; int var2 = 3;
int var3;
var3 = var1 + var2;
System.out.printf("10 + 3 = %d\n", var3); //10 + 3 = 13
// System.out.printf("要顯示的字串", 值)
// %識別符號，printf內的百分比(%)都是特殊的識別符號
// d呈現十進位的整數值
// \n換行
```
## 9 浮點數float 與 倍精度浮點數double 運算
* https://www.youtube.com/watch?v=6UIU3bdReTs&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=9
``` java
float var1 = 10;
float var2 = 3.1f;
// 寫成小數點會被視為double空間存放，要表現float的話要加上f
float var3;
var3 = var1 + var2;
System.out.printf("10 + 3.1f = %.2f\n", var3); // 10 + 3.1f = 13.10
// f代表福點數
// %.2f 取小數點兩位
var3 = var1 / var2;
System.out.printf("10 / 3.1f = %.2f\n", var3); // 10 / 3.1f = 3.23
var3 = var1 % var2;
System.out.printf("10 %% 3.1f = %.2f\n", var3); // 10 % 3.1f = 0.70
var3++;
System.out.printf("var3++ = %.2f\n", var3); // var3++ = 1.70
```
## 10 基本型別混合運算
* https://www.youtube.com/watch?v=bfIFuVT35yg&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=10
``` java
byte var1 = 10;
short var2 = 3;
// short var3 = var1 + var2;
// byte, short, char, int的範圍經過運算，都會變成int的範圍存放，再給值的時候就會出問題
int var3 = var1 + var2;
long var3 = var1 + var2; // long
float var3 = var1 + var2; // float
double var3 = var1 + var2; // double
```
## 11 基本型別轉型處理
* https://www.youtube.com/watch?v=W9Cv3ZxGYWQ&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=11
* 較大的部分放到小的可能會喪精度，要強制轉型
``` java
byte var1;
//		short var2 = 2;
short var2 = 129;
// var1= var2; short佔有的空間比byte大，會編譯失敗，要強制轉型
var1 = (byte)var2;
//		System.out.println(var1); // 2
System.out.println(var1); // -127
//		由小到大byte, short, char, int, long, float, double
```
## 12 判斷式 if 的基本語法
* https://www.youtube.com/watch?v=-hO-HXHLjpQ&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=12
* if(boolean值){...}
``` java
int score = 70;
if(score>=60) {
	System.out.println("Pass");
}
System.out.println("End");
```
## 13 if 單列與區塊結構
* https://www.youtube.com/watch?v=1quKC_V4DIs&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=13
* if(boolean值)單列敘述句;
``` java
int score = 70;
if(score>=60) 
	System.out.println("Pass");

System.out.println("End");
```
## 14 if else 語法格式
* https://www.youtube.com/watch?v=RqG2Rpk75yI&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=14
* if(boolean值){...} else{...}
``` java
int score = 90;
if(score>=60) { 
	System.out.println("Pass");
}else {
	System.out.println("Down");
}
System.out.println("End");
```
## 15 存取修飾字的基本認識
* Java進階物件導向課程
* https://www.youtube.com/watch?v=KxNq5XiGT2g&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=15
* 一般類別 (定義類別時寫在左邊的)
  * public：完全公開
    * public class Access012 {}
  * 沒有：相同Package下才能使用
    * class Access013 {}

## 16 存取修飾字實作驗證
* https://www.youtube.com/watch?v=ijBxL354Phc&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=16&t=3s
* 類別中 (定義類別的大括號內)
  * public：完全公開
  * protected：相同Package及繼承的子類別
  * 沒有：相同Package
  * private：同類別


## 17 建構式的核心觀念
* https://www.youtube.com/watch?v=3gPKFsBD-ZE&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=17
* 任何類別一定會有建構式
* 沒有定義建構式的類別
  * 將會在編譯時期以父類別無傳參數建構式為其唯一建構式
  * 如果父類別不存在無傳參數建構式，則將編譯失敗
* 建構式並不會繼承給子類別
* 基本型別的第一次給值就是初始化
* 物件的第一次給值是new出指定建構式
* 任何建構式在於確保任何物件產生時，會將所有父類別物件實體也產生
  * 也因此才會有繼承的特性

## 18 物件實體建構觀念
* https://www.youtube.com/watch?v=SGvkjFwDSqk&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=18
* 物件初始化
  * 物件被new呼叫建構式
  * new 建構式
* new
  * 產生物件實體
  * 回傳記憶體的存取位址
* 建構式
  * 進行該物件的初始化
* 建構式意義
  * 1.確保祖宗八代都在定義
  * 2.將該物件的一些屬性方法呼叫都在此時初始執行它，進行初始化

## 19 Overloading(覆載)的意義
* https://www.youtube.com/watch?v=xrvppuSreNk&list=PLzH33jxgvsncJIRlerW8Ll8S25v1RTjJJ&index=19
* 類別方法的特性
  * 直覺性的程式呼叫
  * 所以方法名稱一樣
  * 但是參數列不一樣
    * 個數
    * 型別
* 並不在意的是
  * 存取修飾字
  * 傳回值型別
