---
title: JS基本語法
date: 2020-05-14 21:52:09
tags: js
category: JavaScript
---
# 語句（statement）
下面是一行賦值語句
```
var a = 1+2; 
```
- `var`：關鍵字，用來宣告變量。
- `a`：變量名。
- `1+2`（表達式），計算式，返回3。
- `;`(分號)用來結尾語句，也可以用換行來結尾語句。

# 變量（variable）
## 概念

  - 變量是對“值”的具名引用，利用名儲存“值”，在使用名來調用“值”。
      ```
      var a = 1;
      ```
  - 上面的語句在聲明`a`後將`1`這個值賦予了`a`這個變量名，現在`a`=`1`了。
  - 聲明和賦值是兩個步驟。
      ```
      var a;  // 聲明
      a = 1;  // 賦值
      ```
  - 如果只是聲明而沒有賦值，則變量的值為`undefined`(無定義)
  - 可以在一個語句中聲明多個變量，像下面一樣。
     ```
     var a, b; //中間用逗號隔開
     ```

## 變量提升

  - 由於JS引擎的運作方式為先獲取全部變量然後在運行，因此變量會全部被提到頂部（但值不會，所以變量會是未賦值的狀態，直到運行到賦值那行才會賦值）。

# 標識符（identifier）

- 標識符指的是用來識別各種值的名稱。
- 最常見的標識符就是變量名，以及後面會提到的函數名。
- JavaScript語言的標識符對於大小寫敏感，所以`a`和`A`是兩個不同的標識符。
- 標識符的命名規則如下：
  1. 第一個字符，可以是任何Unicode字母，以及美元符號（`$`）和下劃綫（`_`）。
  2.  剩下的字符，除了字母、`$`、`_`之外還可以是數字`0~9`。
  3.  JavaScript 有一些保留字，不能用作標識符：
        > arguments、break、case、catch、class、const、continue、debugger、default、delete、do、else、enum、eval、export、extends、false、finally、for、function、if、implements、import、in、instanceof、interface、let、new、null、package、private、protected、public、return、static、super、switch、this、throw、true、try、typeof、var、void、while、with、yield。

# 注釋（comments）

- 源碼中對於代碼進行解釋的就是注釋。
  ```
  // 這是單行注釋

  /* 這是多行注釋，
  第二行 */
  ```

# 區塊（block）

- 包含語句的大刮號`{}`，稱作區塊。
- JS中的區塊不構成單獨的作用域。

# 條件語句（conditional statements）

- 依據不同的條件，執行不同的語句。

## if 結構

- `if` 結構先判斷一個表達式的布爾值，然後依照布爾值的真僞執行不同的語句。
  ```
  // if 結構
  if（布爾值）{
  語句；
  }
  // if...else if...else結構
  if（布爾值）{
  語句1；
  }else if（布爾值）{
  語句2；
  }else{
  語句3；
  }
  ```

## switch結構

- 當多個`if...else`連在一起時可以轉爲使用更方便的`switch`結構。
- 當表達式的值等於case值時，執行該case，如果所有值都不符合，執行`default`。
- `break`語句用於跳出`switch`結構。
- 表達式的值和case值之間的比較采用的是嚴格相等（`===`）。
  ```
  switch(表達式){
    case caseValue:
    //...
    break
    case caseValue:
    //...
    break
    default:
    //...
  }
  ```

## 三元運算符

- 三元運算符`?!`也可用於邏輯判斷。
  ```
    (條件) ? 表達式1 : 表達式2
  ```
- 上面代碼中，如果條件為真，執行表達式1，反之則執行表達式2。
 
  ```
    var msg = '數字' + n + '是' + (n % 2 === 0 ? '偶數' : '奇數');
  ```

- 上面代碼利用三元運算符，在字串中插入不同的值。

# 循環語句（looping statement）

- 循環語句用於重複執行某個操作，它有多種形式。
  
## while 循環

- `while` 語句包含一個循環條件和一段代碼塊，只要條件為`true`，就不斷循環執行代碼塊。
- 如果條件恆為`true`，則該循環為無限循環。
  ```
  while (條件){
    語句；
  }
  ```

## for 循環

- `for`語句是循環的另一種形式，和`while`語句不同的地方在於它有個迴圈計數器。
  ```
  for(初始化表達式；條件；遞增表達式){
    語句；
  }
  ```

