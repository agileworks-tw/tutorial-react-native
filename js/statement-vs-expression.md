# expression VS statement

### 題外話

Syntax (語法 / 文法)

<!-- 語法決定怎麼去解讀程式碼 -->

```
she cooks an egg.
she is a cook.
```

```
* syntax
  * statements
    * expression statements
  * expressions
```

### expression （表達式)

會產生一個值(會回傳一個值)

* 物件實字 (object literals)

```
{ key1: 'value1', key2: 'value2'}
```

* function expression

```js
var add = function(x, y) {
  return x + y;
}
add(1, 2);
```

* invoking function expression (立即呼叫函式)

```js
(function sayHello() {
    alert("hello!");
})();
```

### statement （陳述式)

<!--Statements are the building blocks of every program. -->

* 完成某項任務的操作
* 會產生附影響 (side effect)

<!-- 解釋什麼叫 side effect -->
<!-- 會影響一個變數或物件的狀態 -->

<!--通常一個 statement 是獨立的，只會完成某項任務，不過如果它影響了整個程式例如: 異動了機器內部的狀態，或者影響後面的 statement，這些造成的改變我們就稱為 side effect (副作用)-->

例如：

```js
var x // 宣告
x = 1; // 賦予值

// 條件判斷
if(x > 0){
  console.log('hi hi');
}
```

**statement block**

```c#
static void main(){
  var counter;
  counter = 1;
  // do something...
  // do something...
  // do something...
  // do something...
}
```

#### function declaration / function statement

```js
function add(a,b) {return a + b};

function hi(name) {
  console.log('hi ' + name);
}
hi('alincode');
```

#### declaration statement

```js
var message;
```

#### expression statement

* expression statements 屬於一種特殊的 statements，會產生一個值，並完成某項任務。

```
x += 1;

counter++;
```

如果在始於 statement 位置的地方放入 expressions，就叫做 expression statement。

<!--
我們已經看到有一些 expression 和 statement 語法上是沒有區別的。
這意味著相同的程式碼會有不同行為取決於它出現在 expression 的位置，
或者是 statement 位置。
-->

<!--為了防止產生疑慮，javascript 會禁止 expression statement 使用 {} 或 function 開頭。-->


### expression 與 statement 之間明顯的差異

* statement 位置，一定可以放 expression，但 expression 位置，大多數情況都不能放 statement。

```js
var x = 1;
var y = 2;

if(x >= 0){
  x = y;
} else {
  x = -y;
}
```

* expression：一定有回傳值

```js
var x = 1;
var y = 2;

var x = (y >= 0 ? y: -y);
```

### function expression VS function statement

**function expression**

```js
var addFunc = function(x, y) {
  return x + y;
}
```

**function declaration / function statement**

```js
function hi(name) {
  console.log('hi ' + name);
}
hi('alincode');
```

### 延伸閱讀

* <https://edux.pjwstk.edu.pl/mat/260/lec/PRG2CPP_files/node37.html>