# 提升 (hoisting)

**執行環境 (execution content)**

* Creation Phase
  * 程式會知道哪裡有用到變數跟函式，並替它們在記憶體留一個位子。
  * 函式在宣告的時候，就被放入了記憶體。
  * 所有變數在建立階段被預設成 undefined
  * Creation Phase 的時候，包含 Variable Environment, this 和 Outer Environment 都會被建立，而 this 有些情況指向 global environment、有些時候則是指向到某個物件 Object。
* Execute Phase

### 範例一

```js
// 這是比較好的做法，不依賴 hoisting。
var a = 'Hello World';
console.log(a);

function b() {
  console.log('呼叫 b');
}
b();
```
<!-- Hello World, 呼叫 b -->

### 範例二

```js
console.log(a); // ?
b();

var a = 'Hello World';

function b() {
  console.log('呼叫 b');  // ?
}
```
<!-- undefined, 呼叫 b -->

### 範例三

```js
console.log(a); // ?
console.log(b); // ?
b();  // ?

var a = 'Hello World';

var b = function() {
  console.log('呼叫 b');
}
```
<!-- undefined, undefined, b is not a function -->
<!--function expressions are not hoisted. -->