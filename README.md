# JS-Output-based-questions.


### 1. Write a function that returns the first non-repeating character in the string.

```javascript
const dataString = "aabbcddeeff";

function check(){
  for(let char of dataString){
  if(dataString.indexOf(char) === dataString.lastIndexOf(char)){
    return char;
  }
}
  return null;
}

console.log("first non-repeating character :: ", check());

Output:
first non-repeating character :: c
```

### 2. Write a function that takes a string as input and returns the total number of vowels (a, e, i, o, u) in the string.

```javascript
const sentence = "The happiest place on Earth";

const VOWELS = ["a", "e", "i", "o", "u"];

// Solution 1
function countVowels(sentence) {
  let vowelCount = 0;

  for (let char of sentence.toLowerCase()) {
    if (VOWELS.includes(char)) {
      vowelCount++;
    }
  }
  return vowelCount;
}

// Solution 2
function countVowels(sentence) {
  return [...sentence.toLowerCase()].reduce(
    (count, char) => VOWELS.includes(char) ? count + 1 : count,
    0
  );
}

console.log(countVowels("Total number of vowels ::", sentence));

Output:
Total number of vowels :: 9
```
