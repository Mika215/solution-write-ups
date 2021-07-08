# [Add Up the Numbers from a Single Number](https://edabit.com/challenge/4gzDuDkompAqujpRi)

<!--
  describe the function's behavior in your own words.
  explain why someone might want to use this function
-->

This function takes any positive number as an argument and it adds up all the numbers from 1 to the given number which has been passed as an argument and it returns back the total(sum)number as a final result.

For instance if you passed 4 as an argument the function addUp will return the sum of all the numbers from 1 to 4.

> Here we go addUp(4) returns (1+2+3+4)=10.

This function could be useful in real world cases to xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx.......


## Syntax

> addUp(`number`) -> `number`

### Parameters

**num**: `number`

<!--
  describe the parameter
-->
we can pass any number as an argument that we want to addUP except ZERO and negative numbers, because our function adds up only positive numbers (starting from 1)
### Return Value: `number`

<!--
  describe the return value
-->
The function addUp, returns back the sum of the numbers between 1 and the given number as a return value.
However, if we pass zero or negative numbers as an argument then it always return back ZERO/error(out of range)

## Test Cases

<!--
  copy in the test cases from the original challenge

  if you write your own test cases in a sandbox file, include those too
-->

```
Test.assertEquals(addUp(4), 10)

Test.assertEquals(addUp(13), 91)

Test.assertEquals(addUp(600), 180300)

Test.assertEquals(addUp(392), 77028)

Test.assertEquals(addUp(53), 1431)

```

## Use Cases

<!--
  write a minimum of 2 use cases to show this functions behavior.

  try to find interesting _edge cases_, it's good for you ;)
  an edge case is when a function behaves different than you'd expect.
  This will help you and others better understand the function.

  https://www.geeksforgeeks.org/dont-forget-edge-cases/
-->

---

---

<!-- copy this section for every solution you study -->



## [_sir](https://edabit.com/user/F7iZc3vpy7d9ALD6D)

<!-- paste the solution here -->

```
function addUp(num) {
    return (num * (num + 1))/2;
  }
```

### Strategy

<!--
  Describe what strategy they used to pass this challenge.
  Careful! your strategy description should not mention
    the code they wrote to solve the challenge.

  Practice describing their strategy at a higher level:
  a simple way to understand strategy is to think of the important steps
  between the argument values and the return values.

  For example if they use a `for` loop
  you won't mention that `i` was incremented,
  but you might mention how the final result changes at each iteration.
-->
The function addUp takes any positive numbers(1=>) as an argument and then it returns out the sum of numbers between 1 and the number passed as an argument.

### Implementation

<!--
  Describe the solution written by this user.
  How did they use JS to implement their strategy?
  What language features did they use?
  What decisions do you think they made and why?
-->
 [_sir](https://edabit.com/user/F7iZc3vpy7d9ALD6D) have used a mathematical expression to precisely find out the sum of numbers between 1 and the number passed as an argument(a given number).

 The mathematical formula is `(num * (num + 1))/2;`
 to make it more clear lets break down this formula in to three simple steps before we get to the final return value.

For instance let's pass 4 as an argument i.e `addUp(4)` :

  - Step1 `(4*(4+1))/2;`

  - Step2 `(4*5)/2;`

  - Step3 `20/2;` which returns `10`


### Possible Refactors

<!--
  List a couple changes you could make in their code without changing their strategy.
  For example:
    `while` loops and `for` loops can often be interchanged.
    `if else`, `switch case` and `_ ? _ : _` can sometimes be interchanged.

  You don't need to actually rewrite the function.
  The goal of this section is that you exploring different JS language features
  and think of different ways to implement the same strategy.
-->

### References

<!--
  links that helped you to understand this solution or to think of possible refactors
-->
I  like the above short code written by [_sir](https://edabit.com/user/F7iZc3vpy7d9ALD6D) because of its simplicity.
But frankly i didn't understand why and how the numbers in the mathematical formula are peaked.I mean why he need to add 1 to the given number and then divided by 2?

---

> ... maybe even more write-ups?


## [Carbon](https://edabit.com/user/2PaATWytPkFGENDqK)

<!-- paste the solution here -->

```
function addUp(num) {
    var total = 0;
    for (var i = 1; i <= num; i++) {
      total += i;
    }
    return total;
  }
```

### Strategy

<!--
  Describe what strategy they used to pass this challenge.
  Careful! your strategy description should not mention
    the code they wrote to solve the challenge.

  Practice describing their strategy at a higher level:
  a simple way to understand strategy is to think of the important steps
  between the argument values and the return values.

  For example if they use a `for` loop
  you won't mention that `i` was incremented,
  but you might mention how the final result changes at each iteration.
-->

### Implementation

<!--
  Describe the solution written by this user.
  How did they use JS to implement their strategy?
  What language features did they use?
  What decisions do you think they made and why?
-->
[Carbon](https://edabit.com/user/2PaATWytPkFGENDqK) has used a for loop iteration to add each number between one and the number passed as an argument.
Below is the screen Shoot of my tracing table that i have used to understand each steps of code execution for this function.

![Alt "Tracing Table screen Shoot"](<img src="/carbon-addup-tracing-table.JPG">)


### Possible Refactors
<!--
  List a couple changes you could make in their code without changing their strategy.
  For example:
    `while` loops and `for` loops can often be interchanged.
    `if else`, `switch case` and `_ ? _ : _` can sometimes be interchanged.

  You don't need to actually rewrite the function.
  The goal of this section is that you exploring different JS language features
  and think of different ways to implement the same strategy.
-->

### References
This solution is exactly the same us Gabriel's solution(check my `sandbox.text.js`) however i chose this one
because the variable names are more clear comparing to Gabriel's(num, and sum are quite similar and tricky for me) 
<!--
  links that helped you to understand this solution or to think of possible refactors-->

  This video on the Mathematical formula [sum of sequential integers proof](https://www.youtube.com/watch?v=tpkzn2e5mtI)helped me to better undersatnd the formula.

---

### Remix

<!-- paste your remixed solution here -->
Below is my remix solution for the challenge


```
const addUp=(num)=>{
  //let minimum=1;  
     if(num<=0){
      alert('Your number should be a positive integer!');
      return;
     }
    let result=(num * (num + 1))/2;
    console.log('addUp:'+num+ '=>'+result); 

    return;
    }
    
    addUp(0);
```

### Strategy

### Implementation
- I used an arrow function to set up my `addUp` function
- I set a bottom line(number) to pass as an argument i.e 1;
- if - Condition checking if the input is a positive number i.e >=1;
- copied the mathematical formula from _sir and assigned it to a new variable name `result`.this makes it simple to call(read) the formula multiple times.
- unlike other solutions my remix solution can alert a message to remind the user that inputs should always be only positive integers
- incorporated logging for the developer to see the interaction from the back



### Possible Refactors

### Inspired By

<!--
  which solutions inspired your solution?
  what did you take from each one?
-->

### References

---

## Retrospective

<!--
  write any notes to help you review this exercise later, and to help others' study it.

  this might include:

  - good ideas to use later in your own code
  - less good ideas to avoid in your own code
  - new vocabulary you learned
  - the most important thing(s) you learned
  - something that you still don't understand but want to keep studying
  - something that surprised you
  - tricks you will want to remember and use later
-->
