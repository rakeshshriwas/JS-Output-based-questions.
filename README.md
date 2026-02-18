# JS-Output-based-questions.


### 1. Write a function check() that returns the first non-repeating character in the string.

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


**Output**
first non-repeating character :: c
```
