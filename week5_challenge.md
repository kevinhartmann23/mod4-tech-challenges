# Problem - Roman Numerals
![Roman Numerals](https://media.giphy.com/media/xT5LMNd1ieywmnI3Qc/giphy.gif)

Write a recursive function that converts an integer into a string such that the number is represented in Roman Numerals in the most efficient way.

For example, the number `4` could be written as `IIII` but it's more efficient to use `IV`since that's a shorter string.

Assume no number is greater than 4,000.

Here are the Roman Numeral equivalents you'll need to know:
- M=1000
- CM=900 
- D=500 
- CD=400
- C=100 
- XC=90 
- L=50 
- XL=40
- X=10 
- IX=9 
- V=5 
- IV=4 
- I=1

## JS Starter Code
```js
function toRoman(num) {
  // your code goes here
}

console.log(toRoman(128));  // should return "CXXVIII"
console.log(toRoman(2000)); // should return "MM"
console.log(toRoman(2017)); // should return "MMXVII"
console.log(toRoman(1999)); // should return "MCMXCIX"
```

## Ruby Starter Code
```rb
def to_roman(num)
  # your code goes here
end

puts to_roman(128)   # should return "CXXVIII"
puts to_roman(2000)  # should return "MM"
puts to_roman(2017)  # should return "MMXVII"
puts to_roman(1999)  # should return "MCMXCIX"
```

# Instructions

1. Copy this markdown and paste in your own, privte gist
2. In your private gist, fill out the questions below
4. Submit by the due time as instructed in Zoom

Do not publish your code on a public repl.it or repo or other public means.

## Rewrite the question in your own words:
Write a function that converts an integer (input) to a string (output): the string must represt the intergers value in roman numerals

## What assumptions will you make about this problem if you cannot ask any more clarifying questions? What are your reasons for making those assumptions?
- Input will not be greater than 4000
- 

## What are your initial thoughts about this problem? (high level design, 2-3 sentences)
- Use an object to set key:value pairs of romanNumeralValue:integerValue
- Utilize a few math related methods to break down input value to the remainder from key:value pairs

## How would you identify the elements of this problem?

- [ ] Searching of Data
- [ ] Sorting of Data
- [x] Pattern Recognition
- [ ] Build/Navigate a Grid
- [x] Math
- [ ] Language API knowledge
- [ ] Optimization


## Which data structure(s) do you think you'll use? What pros/cons do you see with that choice?
Map, i believe?

## Write out a few lines of initial pseudocode: (mid-level design, NOT REAL CODE)
- Create an object of key:value pairs (romanNumeralValue:valueAsInteger)
- set result to an empty string
- iterate through object keys
- determine a replace amount, checking input divided by each keys value (ex: 2000 / 1000 = 2)
- Subtract input by the (replace amount multiplied by unique key's value) (ex: 2000 - (2 * 1000)
- Concatenate result (empty string) with key as manytimes as the value of the replace amount

## Write out any implementation code OR link to repl
[REPL](https://replit.com/@KevinHartmann23/Roman-Numeral-Converter)

## What is the Big O complexity of your solution?
Constant Time - the iteration will always be the same, no matter what the value of `num` is
O(1)
