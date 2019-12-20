Codewars Solutions

=== https://www.codewars.com/kata/55902c5eaa8069a5b4000083 ===
```
function formatMoney(amount){
return `$${amount.toFixed(2)}`;
}
```
=== https://www.codewars.com/kata/55fd2d567d94ac3bc9000064 ===
```
function rowSumOddNumbers(n) {
  let c = skipNumbers(n);
  let firstOddInRow = c * 2 + 1;
  let sum = 0;
  for (let i = 0; i < n; i++) {
  sum += firstOddInRow + i*2;
  }
  return sum;
}

function skipNumbers(n){
  let count = 0;
  for (let i = 1; i < n; i++){
    count += i;
  }
  return count;
}
// Math.pow(n,3)//

```
=== https://www.codewars.com/kata/514b92a657cdc65150000006 ===
```
function solution(number){
  let sum = 0;
  for (let i = 3; i < number; i++){
  if (i % 3 === 0 || i % 5 === 0){
      sum += i;
  }
  }
  return sum;
}
```
=== https://www.codewars.com/kata/57eaeb9578748ff92a000009 ===
```
function sumMix(x){
let sum = 0;
  for (let i = 0; i < x.length; i++){
    if (typeof x[i] === 'string') {
    x[i] = Number(x[i]);
    }
  sum += x[i];
  }
return sum;
}
```
=== https://www.codewars.com/kata/55fd2d567d94ac3bc9000064 ===
```
function rowSumOddNumbers(n) {
  let c = skipNumbers(n);
  let firstOddInRow = c * 2 + 1;
  let sum = 0;
  for (let i = 0; i < n; i++) {
  sum += firstOddInRow + i*2;
  }
  return sum;
}

function skipNumbers(n){
  let count = 0;
  for (let i = 1; i < n; i++){
    count += i;
  }
  return count;
}
// or return n*n*n
```
=== https://www.codewars.com/kata/59dd3ccdded72fc78b000b25 ===
```
function whatday(num) {
  let arr = ["Sunday", "Monday", "Tuesday", "Wednesday" ,"Thursday", "Friday", "Saturday"];
  if (num > 7 || num <= 0) {
    return 'Wrong, please enter a number between 1 and 7';
  } else {
    return arr[num - 1];
  }
}

````
Mumbling 7 (lev)

=== https://www.codewars.com/kata/5667e8f4e3f572a8f2000039 ===
```
function accum(s) {
    let str = '';
    for (let i = 0; i < s.length; i++){
        let c = s[i];
        str = str + '-';
        for (let j = 0; j < i + 1; j++){
            if (j === 0) str = str + c.toUpperCase();
            else str = str + c.toLowerCase();
        }
    }
    str = str.substring(1);
    return str;
}
```
Type of sum (8 lev)

=== https://www.codewars.com/kata/type-of-sum/solutions/javascript ===
```
function typeOfSum(a, b) {
  return typeof (a+b)
}

```
Switch it Up! (8 lev)

=== https://www.codewars.com/kata/5808dcb8f0ed42ae34000031 ===

JavaScript:
```
function switchItUp(number){
let arr = ['Zero', 'One', 'Two', 'Three', 'Four', 'Five', 'Six', 'Seven', 'Eight', 'Nine'];
return arr[number];

}
```
==============

7 kyu
Filter Coffee

===https://www.codewars.com/kata/56069d0c4af7f633910000d3===

JavaScript:
```
function search(budget, prices) {
let str = '';
let arr = [];
for (let i = 0; i < prices.length; i++)
  if (prices[i] <= budget) arr.push(prices[i]);

arr.sort((a, b) =>  a - b);

return arr.join();
}
```
6 kyu
String average

===https://www.codewars.com/kata/5966847f4025872c7d00015b===

JavaScript:
```
function averageString(str) {
  let arr = ['zero', 'one', 'two', 'three', 'four', 'five', 'six','seven', 'eight', 'nine'];
  let arrStr = str.split(' ');
  let sum = 0;
  for (let i = 0; i < arrStr.length; i++){
    if (arrStr[i] === '' || arr.indexOf(arrStr[i]) === -1) return 'n/a';
    sum += arr.indexOf(arrStr[i]);
  }
  let avg = Math.floor(sum/arrStr.length);
  return arr[avg];
}

```
6 kyu
Sort the odd

===https://www.codewars.com/kata/578aa45ee9fd15ff4600090d===

JavaScript:
```
function sortArray(array) {

  let odd = array.filter(a => a % 2 !== 0).sort((a, b) => a - b);
  let res = array.map(a => a % 2 !== 0 ? odd.shift() : a);

return res;
}

```
7 kyu
Maximum Triplet Sum (Array Series #7)
JavaScript:

===https://www.codewars.com/kata/5aa1bcda373c2eb596000112===
```
function maxTriSum(numbers){
let sum = 0;
  let res = numbers.sort((a, b) => b - a);
  let arr = [];
  for (let i = 0; i < res.length; i++){
    if (arr.length >= 3){
      break
    }
    if (!arr.includes(res[i])){
      arr.push(res[i]);
      sum += res[i];
    }
  }
 return sum;
}
```
7 kyu
Sum of Array Averages

===https://www.codewars.com/kata/56d5166ec87df55dbe000063/solutions/javascript===

JavaScript:
```
const sumAverage = (arr) => {
  let result;
  let sumAvg = 0;
  for (i = 0; i < arr.length; i++) {
    let subSum = arr[i].reduce(function(sum, elem) {
	    return (sum + elem);
    });
    let subAvg = subSum / arr[i].length;
    sumAvg += subAvg;
  }
  return result = Math.floor(sumAvg);
 
}
```
7 kyu
Drying Potatoes
=== https://www.codewars.com/kata/drying-potatoes/train/javascript  ===
JavaScript:
```
function potatoes(initialPercentOfWater, 
  initialWeight, finalPercentOfWater) 
{
    console.log(`(${initialPercentOfWater}, ${initialWeight}, ${finalPercentOfWater})`)
    
    let dry = initialWeight * (100 - initialPercentOfWater) / 100;
    let persDryAfter = 100 - finalPercentOfWater;
    let kgWaterAfter = finalPercentOfWater / persDryAfter * dry;
    
    console.log(`total: ${kgWaterAfter + dry}`)
    let total = Math.trunc(kgWaterAfter + dry);
    return total;
}
```

7 kyu
Sum of a Beach
===https://www.codewars.com/kata/5b37a50642b27ebf2e000010===
JavaScript:

```

  function sumOfABeach(beach) {
  let reg = /sand|water|fish|sun/gi;
  let arr = beach.match(reg);
  return !arr ? 0 : arr.length;
}
```
7 kyu
Array Leaders (Array Series #3)
===https://www.codewars.com/kata/5a651865fd56cb55760000e0===
JavaScript:
```
var arrayLeaders = num => {
    let arr = [];
    for (let i = 0; i < num.length; i++){
      let sum = 0
      for (let j = i+1; j < num.length; j++){
        sum += num[j];
      }
      if (num[i] > sum){
        arr.push(num[i]);
      }
    }

  return arr
}
```
7 kyu
Beginner Series #3 Sum of Numbers
===https://www.codewars.com/kata/55f2b110f61eb01779000053/solutions/javascript===
```
const GetSum = (a, b) => {
  let min = Math.min(a, b),
      max = Math.max(a, b);
  return (max - min + 1) * (min + max) / 2;
}
```
