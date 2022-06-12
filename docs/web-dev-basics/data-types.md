---
sidebar_position: 2
---

# Data Types

All data is represented as 0s and 1s in a computer. A sequence of 0s and 1s could represent an instruction, a number, some text, etc. This is where **data types** come into play, they allow the programmer to indicate what kind of data they want to represent.

In JavaScript, there are a few basic data types:

| Data Type | Examples                        | Description                                                   |
| --------- | ------------------------------- | ------------------------------------------------------------- |
| `number`  | `5`, `-1`, `Infinity`, `3.1415` | Any numeric quantity                                          |
| `string`  | `"A"`, `"Hello World"`, `"3"`   | Any plain text within double or single quotes (`""` or `''`). |
| `boolean` | `true`, `false`                 | Often the result of a logical expression (e.g. `x < 5`).      |

Data types are inferred when you create variables. For example, in the statement `let age = 15`, `age` becomes a variable of type `number` because the number literal `15` was assigned to `age`.

## Objects: A Group of Variables and Functions

Objects are more complex data types. They may have multiple variables and functions stored together in a group. Here's a simple example of a object representation of a Pokemon with HP and one attack:

```javascript
const pikachu = {
  hp: 40,
  spark: function (opponent) {
    const sparkDamage = 10;
    opponent.hp = opponent.hp - sparkDamage;
  },
};
```

If we add another Pokemon, you can see how the objects can interact with each other. Try running the code yourself by putting it in a `<script>` element or pasting it in a browser's developer console.

```javascript
// Remember, we can use const because we are only assigning
// data to a variable once.
const pikachu = {
  hp: 40,
  spark: function (opponent) {
    const damage = 10;
    opponent.hp = opponent.hp - damage;
  },
};

const bulbasaur = {
  hp: 40,
  tackle: function (opponent) {
    const damage = 10;
    opponent.hp = opponent.hp - damage;
  },
};

pikachu.spark(bulbasaur);
// 30
console.log(bulbasaur.hp);
```

Let's break down the code.

- A variable that is a member of an object is called an **field**.
- A function that is a member of an object is called a **method**.
- To access fields and methods of an object, use the `.` operator. You've already been doing this!

```javascript
// Accessing the spark method of the pikachu object
pikachu.spark();
// Accessing the hp field of the bulbasaur object
bulbasaur.hp;
// Accessing the log method of the console object
console.log();
```

- Creating an object is called **instantiation**. We were using an **instance** of the pikachu object, etc.
- This way of defining an object is called **JSON**: **JavaScript Object Notation**.

```javascript
// Creating an instance of the pikachu object.
// JSON starts and ends with curly braces {}.
// Each field and method is defined with its name followed by a colon, the data, and a comma.
const bulbasaur = {
  hp: 40,
  tackle: function (opponent) {
    const damage = 10;
    opponent.hp = opponent.hp - damage;
  },
};
```

## The `Math` object

There are lots of built-in objects in JavaScript and the `Math` object is one of these. Here are some of its fields and methods (full list [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)).

| Property         | Description                                  |
| ---------------- | -------------------------------------------- |
| `Math.E`         | The constant &ee;, approx. 2.718             |
| `Math.PI`        | The constant &pi;, approx. 3.14159           |
| `Math.pow(x, y)` | Calculates x to the power y (x<sup>y</sup>)  |
| `Math.random()`  | Produces a random decimal number from 0 to 1 |

We're going to use the `Math.random()` function to generate random numbers of different ranges in the practice task below, so let's walk through how to do that.

```javascript
const zeroToOne = Math.random();
const zeroToTen = zeroToOne * 10;
const negFiveToFive = zeroToTen - 5;
// Here's a one-liner to generate a number from -5 to 5.
console.log(Math.random() * 10 - 5);
// What is the range of this?
console.log(Math.random() * 10 + 5);
```

The next section in this tutorial is about more of these built-in objects; for a full list, click [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects) and [here](https://developer.mozilla.org/en-US/docs/Web/API).

## Practice Task: RPG Game Simulation

> Be sure to get the starter JavaScript code from the bottom of the page.

- Create two characters (Pokemon or otherwise) that each have an `hp` field, a `speed` field, and `attack` method.
- The hp fields should be numbers.
- The speeds should be numbers that are different for each player. The speeds determine who goes first.
- The `attack` method should lower the other player's hp by a random amount. It should also log a message to the console indicating which player is attacking which.
- Every time you refresh the page with your code, Player 1 or Player 2 will randomly win.

```javascript
const player1 = {
  // TODO
};

const player2 = {
  // TODO
};

// This logic will run your game.
// No need to modify anything below.
while (player1.hp > 0 && player2.hp > 0) {
  if (player1.speed > player2.speed) {
    player1.attack(player2);
    player2.attack(player1);
  } else {
    player2.attack(player1);
    player1.attack(player2);
  }
}

if (player1.hp <= 0) {
  console.log("Player 2 wins!");
} else {
  console.log("Player 1 wins!");
}
```
