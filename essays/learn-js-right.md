---
layout: essay
type: essay
title: Learning JavaScript the Right Way
date: 2016-09-01
labels:
  - Software Engineering
  - Learning
---

<img class="ui tiny left circular floated image" src="https://upload.wikimedia.org/wikipedia/commons/7/73/Javascript-736400_960_720.png">

JavaScript is a superstar of the modern web for good reason. It has flexibility far beyond that of traditional compiled languages and is the go-to tool for many agile developers. Anyone interested in web development should learn JavaScript. But they should learn it the right way. And that means understanding the unique features of the language and the how to write in a way that conforms to recommended standards.

## New Kids on the Block

### 1. Const and Let

The ability to write JavaScript is not the same as the ability to write good JavaScript. Follow modern best-practices, such as the most recent ECMAScript recommendations to take your use of the language to the next level. One ECMAScript 6 recommendation is replacing var with const and let in declarations for constants and variables, respectively. This makes it easier to recognize when you're dealing with a constant or a variable, for one thing. For another, constants and variables declared with const and let are block-scoped, meaning they are only available within the block in which they were declared. After reading the recommendations, I learned that the block-scoped nature of const and let is generally preferred to the function-scoped nature of var, because it can be easy to use a variable declared with var outside of the area in which you intend to use it.

### 2. Returning a Function from a Function

I was also not previously aware of the ability to return a function from another function in JavaScript, but it is a feature that makes JavaScript more powerful than many other languages. It can allow one to easily create variations of a function. As a simple example, in Java or C it is easy to implement a function that increments a value by a certain amount, but what if you need to increment various values by various amounts?

You could create one function to increment a value by two, one by 3, one by 4, and so on, or you could create a function that took two parameters, the first being a value to increment and the second a value by which to increment. In JavaScript, however, you also have the option of creating one function that acts as a sort of template which creates another function. In the case of incrementing functions, you could create a function that accepts the value by which to increment as an argument and returns a function that increments a value passed to it (the inner function) by the value of the parameter defined in the outer function.

#### Sound complicated?

For those with at least a little familiarity with JavaScript, this concept is probably better demonstrated with some simple code. So, here is an
 example as demonstrated by Philip Johnson, professor of Computer Science at the University of Hawaii:

```javascript
function makeInc(incVal) {
  return function(val) {
    return val + incVal;
  }
}

const inc2 = makeInc(2);

const inc10 = makeInc(10);

console.log(inc10(2000));
```

In the code above, calling the function makeInc actually returns a function that iterates a value by the amount passed to incVal. The functions returned by makeInc(2) and makeInc(10) are stored in the inc2 and inc10 constants. When inc10 is later called with an argument of 2000, the value returned from inc10 is 2010, because the inc10 function increments its passed value by 10.

Although this example may be simple, skillful use of this feature could save a developer hours of time.

## Athletic Software Engineering

Knowledge alone isn't enough to make a great software engineer, however. Practice, and specifically how you practice, is just as important. In the fall of 2016, I was taught one very useful technique in a software engineering course with Philip Johnson at the University of Hawaiʻi. Professor Johnson structured much of the course around a style of development which he has coined athletic software engineering.

### Workout of the Day

One of the central features of Professor Johnsons’ course is the Workout of the Day, or WOD (pronounced like wad), which takes the form of an in-class, timed, coding exercise. These in-class exercises are supplemented by practice WODs which are to be done at home beforehand. He had us do the practice problems under time constraints, which turned out to be absolutely essential preparation for the actual performance.

I believe that this kind of training, if used consistently, can develop your ability to solve problems on your feet, and perhaps even more importantly, build a habit of intense focus when solving problems under pressure. Just as with musical or athletic feats, it is the rehearsal of skills time and time again that allows one to perform as impeccably as possible on stage or in the arena.

<br>
