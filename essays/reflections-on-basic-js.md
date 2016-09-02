---
layout: essay
type: essay
title: Reflections on Basic JavaScript
date: 2016-09-01
labels:
  - Software Engineering
  - Learning
---

<img class="ui tiny left circular floated image" src="https://upload.wikimedia.org/wikipedia/commons/7/73/Javascript-736400_960_720.png">

After approximately two weeks of learning JavaScript through ICS 314, Software Engineering, I am happy to say that I have learned some things that are new, interesting, and useful, all at the same time.

I have some previous experience with JavaScript as a result of taking ICS 215, Introduction to Scripting, but I was not introduced to ECMAScript 6 recommendations in that course. One such recommendation is replacing var with const and let in declarations for constants and variables, respectively. Constants and variables declared with const and let are also block-scoped, meaning they are only available within the block in which they were declared. I have learned that the block-scoped nature of const and let is preferred to the function-scoped nature of var, because it can be easy to use a variable declared with var without intending to.

I was also not previously aware of the ability to return a function from another function in JavaScript. It seems that this can allow one to easily create variations of a function. As a simple example, in Java or C it is easy to implement a function that increments a value by a certain amount, but what if you need to increment various values by various amounts?

You could create one function to increment a value by two, one by 3, one by 4, and so on, or you could create a function that took two parameters, the first being a value to increment and the second a value by which to increment. In JavaScript, however, you also have the option of creating one function that acts as a sort of template which creates another function. In the case of incrementing functions, you could create a function that accepts the value by which to increment as an argument and returns a function that increments a value passed to it (the inner function) by the value of the parameter defined in the outer function.

Sound complicated? For those with at least a little familiarity with JavaScript, this concept is probably better demonstrated with some simple code. So, here is an example as demonstrated by my ICS 314 professor:

```
function makeInc(incVal) {
  return function(val) {
    return val + incVal;
  }
}

const inc2 = makeInc(2);

const inc10 = makeInc(10);

console.log(inc10(2000));
```

In the code above, calling the function makeInc actually returns an iterator function that iterates a value by the amount passed to incVal. The functions returned by makeInc(2) and makeInc(10) are stored in the inc2 and inc10 constants. When inc10 is later called with an argument of 2000, the value returned from inc10 is 2010, because the inc10 function increments its passed value by 10.

Although this example may be simple, I anticipate that the opportunity for creative use of this feature may present itself frequently in this class.

This fall 2016 software engineering course in which I am enrolled is taught by Philip Johnson, professor of Information and Computer Sciences at the University of Hawaiʻi. Professor Johnson has structured the course around a style of development called athletic software engineering, of which he is the creator.

One of the central features of Professor Johnsons’ pedagogy is the Workout of the Day, or WOD, which takes the form of an in-class, timed, coding exercise. These in-class exercises are supplemented by practice WODs which are to be done at home beforehand. I think that these opportunities to practice similar problems under time constraints are absolutely essential preparation for the actual performance. Just as with musical or athletic feats, it is the practice of basic and advanced skills time and time again that allows one to perform as impeccably as possible under pressure.

I participated in my first real WOD today and, although I felt some anxiety at the start, I was able to draw on my practice WOD experiences to finish the assignment within Rx time. I’m sure that these exercises will become more difficult in the future, but I think that as long as I prepare appropriately I will enjoy this class. I look forward to achieving greater confidence and fluency in JavaScript as a result of this learning technique.

