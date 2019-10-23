# The Challenge - Towers of Hanoi

For today's challenge, we're going to have you try to build a program that lets you play one of the most classic games that most programmers learn on. The goal of Towers of Hanoi is to move a set of discs of different sizes from one peg to another while only allowing the player to take the topmost disc off the peg and not putting a larger disc on top of a smaller one. Here is a site that lets you see the game being played with the ability to change the amount of pegs/discs: http://towersofhanoi.info/Animate.aspx.

The story goes that priests in a temple move 64 discs around 3 pegs to fulfill the prophecy that if they complete their task the world will end. Thankfully, based on the math that we know, to complete this task would take 2^64-1 seconds to complete, or ~585 billion years. We won't have you try to solve this puzzle. We suggest that you start with 3 - 5 discs in your initial solution.

For the most part, we will let you control your own structure and technique for this project.

Here are the requirements:

First of all it will need a board. We'll utilize a 2D array to do this:

```js
var board = [
  [3, 2, 1],
  [],
  []
];
```

Next, to play the game, you'll want to create a function called `moveDisc` that takes two parameters - the "start peg" and the "end peg". It will look like this:

```js
var moveDisc = function (startPeg, endPeg) {
  // write your code here ;)
};
```

To call the function and play the game, you can do something like this:

```js
moveDisc(1, 2);
```

The above move would move the "disc" from the first peg to the second peg. The `board` array would now look like this:

```js
var board = [
  [3, 2],
  [1],
  []
];
```

You can keep on playing until you end up with a "win" situation, like this:

```js
var board = [
  [],
  [3, 2, 1],
  []
];
```

Essentially all the discs have been moved from one peg to another. You'll need to write a function that checks for this win scenario and alerts "Winner!" or something like that. It's up to you.

Also, be sure to prevent illegal moves. For example, if our board looked like this:

```js
var board = [
  [3, 2],
  [1],
  []
];
```

This would be an illegal move:

```js
moveDisc(1, 2);
```

Because the disc `2` cannot be pushed on top of the disk `1` (in other words, you cannot move a disk at the moment from the first peg to the second).

That is all. Have fun!
