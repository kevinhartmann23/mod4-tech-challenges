# Bracket Matcher

Ever wonder how your linter knows if you have matching brackets? Well it's time to think of a solution to that!

Given a set of brackets, `[, {, (`, create a function that determines if the brackets are well-formed (match) or not - even with bracket nesting. For example:

```javascript
bracket('{}');

// => true
```

```javascript
bracket('{(');

// => false
```

```javascript
bracket('{()}');

// => true
```

```javascript
bracket('{[)][]}');

// => false
```

```javascript
bracket(']');

// => false
```

```javascript
bracket('({[]}{[]})');

// => true
```

## Instructions

1. Copy this markdown and paste in your own, private gist
2. In your private gist, fill out the questions below
4. Submit by the due time as instructed in Zoom


## Rewrite the question in your own words:
Create a function that takes in a set of brackets... `({ [] })` ... and returns a boolean if the brackets match and close each other out:

## What assumptions will you make about this problem if you cannot ask any more clarifying questions? What are your reasons for making those assumptions?
- Input will always be a string of brackets
- Input will never include other elements outside of `(){}[]`

## What are your initial thoughts about this problem? (high level design, 2-3 sentences)
In order for a bracket to be considered closed, its pair will be found in an index that can be determined by simple math
if index 0 is ( then index last should be )


## How would you identify the elements of this problem?

- [ ] Searching of Data
- [ ] Sorting of Data
- [x] Pattern Recognition
- [ ] Build/Navigate a Grid
- [ ] Math
- [ ] Language API knowledge
- [ ] Optimization


## Which data structure(s) do you think you'll use? What pros/cons do you see with that choice?
array prototype/ prototpye methods

## Write out a few lines of initial pseudocode: (mid-level design, NOT REAL CODE)
//Input: String of brackets
//Method:
- Convert string to array
- Operational Information: 
      - Add a possible matches object - key/value pairs = "(":")" etc.. 
      -  array.length (/2 to determine possible matches) - if arr.length is not divisible by 2 return false!
      -  compare possible matches to relitave index
      -  return true if all match, else return false
- iterate through array, compare first index with last, continue to check, 2index to 2nd to last, etc
//Output: Boolean
## Write out any implementation code OR link to repl
[REPL LINK](https://replit.com/@KevinHartmann23/BrackMatcher)
## What is the Big O complexity of your solution?
It iterates through an array only once so...... O(n)?
