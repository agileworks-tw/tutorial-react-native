# this

每當被呼叫新的執行環境，就會被創造。

### 對類別語言而言 this 是什麼？

* this
* super

<!-- 在 class 語言 this 往往指向 instance-->

```java
public class CashCard extends Card {

	private String number;
	private int balance;
	private int bonus;

	public CashCard(String number, int balance, int bonus) {
		this.number = number;
		this.balance = balance;
		this.bonus = bonus;
	}

  public getBalance() {
		return this.balance;
	}

	public static void main(String[] args) {
		CashCard cashcard = new CashCard();
	}
}
```

### 當不清楚 this 指向哪裡，你將會遇到什麼問題？

* 無意間宣告了全域變數

### 範例

<!-- 兩個 this 都指向 global -->

**範例一**

```js
// function statement
function a() {
  this.myValue = 'hello';
  console.log(this);
}
console.log('=== 1 ===');
a();
```
<!-- window -->

```js
// function expressions
var b = function() {
  this.myValue = 'hello';
  console.log(this);
}

console.log('=== 2 ===');
b();
```
<!-- window -->

```js
console.log(myValue);
```
<!-- hello -->

**範例二**

<!--當函式連結到物件方法時，this 關鍵字就會指向那個連結到的物件。-->

```js
var myObject = {
  name: 'alincode',
  log: function() {
    this.name = 'daisy';
    console.log(this);  // ?
  }
}

// 物件方法
myObject.log();
```

<!-- daisy 發 dayz -->

**範例三**

物件方法裡面宣告一個函式

```js
var myObject = {
  name: 'alincode',
  log: function() {
    var setName = function(newname) {
      this.name = newname;	// 這裡的 this 代表的是？
      console.log(this);
    }
    setName('daisy');
  }
}

myObject.log();
```
<!-- setName 函式並不是物件方法，所以這裡的 this 是指向 globel -->

**範例四**

解決範例三的 pattern

```js
var myObject = {
  name: 'alincode',
  log: function() {
    var self = this;
    var setName = function(newname) {
      self.name = newname;
    }
    setName('daisy');
    console.log(self);
  }
}

myObject.log();
```