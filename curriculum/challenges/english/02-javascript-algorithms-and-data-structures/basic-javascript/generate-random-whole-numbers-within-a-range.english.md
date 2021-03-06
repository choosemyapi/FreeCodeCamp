---
id: cf1111c1c12feddfaeb2bdef
title: Generate Random Whole Numbers within a Range
challengeType: 1
isHidden: false
videoUrl: 'https://scrimba.com/c/cm83yu6'
forumTopicId: 18187
---

## Description
<section id='description'>
Instead of generating a random number between zero and a given number like we did before, we can generate a random number that falls within a range of two specific numbers.
To do this, we'll define a minimum number <code>min</code> and a maximum number <code>max</code>.
Here's the formula we'll use. Take a moment to read it and try to understand what this code is doing:
<code>Math.floor(Math.random() * (max - min + 1)) + min</code>
</section>

## Instructions
<section id='instructions'>
Create a function called <code>randomRange</code> that takes a range <code>myMin</code> and <code>myMax</code> and returns a random number that's greater than or equal to <code>myMin</code>, and is less than or equal to <code>myMax</code>, inclusive.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: The lowest random number that can be generated by <code>randomRange</code> should be equal to your minimum number, <code>myMin</code>.
    testString: assert(calcMin === 5);
  - text: The highest random number that can be generated by <code>randomRange</code> should be equal to your maximum number, <code>myMax</code>.
    testString: assert(calcMax === 15);
  - text: The random number generated by <code>randomRange</code> should be an integer, not a decimal.
    testString: assert(randomRange(0,1) % 1 === 0 );
  - text: <code>randomRange</code> should use both <code>myMax</code> and <code>myMin</code>, and return a random number in your range.
    testString: assert((function(){if(code.match(/myMax/g).length > 1 && code.match(/myMin/g).length > 2 && code.match(/Math.floor/g) && code.match(/Math.random/g)){return true;}else{return false;}})());

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='js-seed'>

```js
function randomRange(myMin, myMax) {
  // Only change code below this line
  return 0;
  // Only change code above this line
}
```

</div>


### After Test
<div id='js-teardown'>

```js
var calcMin = 100;
var calcMax = -100;
for(var i = 0; i < 100; i++) {
  var result = randomRange(5,15);
  calcMin = Math.min(calcMin, result);
  calcMax = Math.max(calcMax, result);
}
(function(){
  if(typeof myRandom === 'number') {
    return "myRandom = " + myRandom;
  } else {
    return "myRandom undefined";
  }
})()
```

</div>

</section>

## Solution
<section id='solution'>


```js
function randomRange(myMin, myMax) {
  return Math.floor(Math.random() * (myMax - myMin + 1)) + myMin;
}
```

</section>
