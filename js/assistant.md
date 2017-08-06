# 助教協助項目

### 練習題

1. BMI

```js
function getBMI(height, weight) {
  return new Number(weight / (height * height)).toFixed(1);
}

console.log(getBMI(1.6, 50));

function getMessage(height, weight) {
  var bmi = getBMI(height, weight);
  var message;
  if(bmi < 18.5){
    message = '體重過輕';
  } else if(18.5 <= bmi && bmi < 24){
    message = '正常範圍';
  } else {
    message = '異常範圍';
  }
  return message;
}
console.log(getMessage(1.6, 50));
```