Codewars Solutions

https://www.codewars.com/kata/55902c5eaa8069a5b4000083

function formatMoney(amount){
return `$${amount.toFixed(2)}`;
}

https://www.codewars.com/kata/55fd2d567d94ac3bc9000064

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