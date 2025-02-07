# Unexpected return value in foo function
This repository contains a JavaScript function `foo` that exhibits unexpected behavior when one of its arguments is 0. The function should return the sum of a and b unless both are 0, however, it currently returns 0 in such cases.

## Bug Report
The `foo` function is defined as:
```javascript
function foo(a,b){
    if (a === 0 || b === 0) {
        return 0;
    } 
    return a + b;
}
```
When called with `foo(0,1)`, it unexpectedly returns 0 instead of 1.  The same occurs with `foo(1,0)`. This is because the condition `a === 0 || b === 0` evaluates to true even when only one of the arguments is 0.

## Solution
The solution corrects the conditional logic to only return 0 when both `a` and `b` are 0. This ensures that the function returns the expected sum in all other cases.
The corrected function is available in `bugSolution.js`