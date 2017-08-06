# 範圍鏈 (scope chain)

* 整個搜尋範圍鏈到外部環境的過程，整條鏈子叫做範圍鏈。
  * 範圍：我能夠取得這個變數的地方。
  * 鏈：外部環境參照的連結
* 執行順序會決定它如何被呼叫。

**外部環境**

* 每個執行環境，都會有外部環境 (Reference to Outer Environment)。
* 當你需要某個執行環境內的程式碼的變數，如果它無法找到變數，它會到外部環境尋找變數。

### 範例

![](assets/scope-chain.png)

**範例一**

```js
function b() {
  console.log(myVar);
}

function a() {
  var myVar = 2;
  b();
}

var myVar = 1;
a();
```
<!-- 1 -->

**範例二**

```js
function a() {
  function b() {
    console.log(myVar); // ?
  }
  var myVar = 2;
  b();
}

var myVar = 1;
a(); 
```
<!-- 2 -->
<!-- 當 a 還沒被執行時，不可能執行 b，所以 a 是 b 的外部參照。 -->

**範例三**

```js
function a() {
  b();
  myVal = 2;
  function b() {
    console.log(myVar);
  }
}

var myVar = 1;
a();
```
<!-- 1 -->