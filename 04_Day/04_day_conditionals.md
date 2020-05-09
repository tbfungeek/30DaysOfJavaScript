<div align="center">
  <h1> JavaScript 30天挑战 </h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/asabeneh?style=social">
  </a>

  <sub>Author:
  <a href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br>
  <small> January, 2020</small>
  </sub>
</div>

[<< Day 3](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/03_Day/03_booleans_operators_date.md) | [Day 5 >>](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/05_Day/05_day_arrays.md)

![Thirty Days Of JavaScript](../images/banners/day_1_4.png)

- [📔 第四天](#%f0%9f%93%94-day-4)
  - [条件语句]](#conditionals)
    - [if](#if)
    - [if else](#if-else)
    - [if else if else](#if-else-if-else)
    - [Switch](#switch)
    - [三目操作符]](#ternary-operators)
  - [💻 Exercises](#%f0%9f%92%bb-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# 📔 第四天

## 条件语句

默认情况下JavaScript中的语句从上到下按照顺序依次执行。如果处理逻辑需要基于不同的条件做出不同的决定则可以通过两种方式更改顺序执行流：

- 条件表达式: 在某个表达式为true的情况下包含一个或者多个语句的某个语句块将会被执行。
- 循环表达式: 只要某个表达式为true，包含一个或者多个语句的某个语句块将会被重复执行。

在这部分我们将会介绍 _if_, _else_ , _else if_ 语句。前面介绍的比较和逻辑操作符在这部分介绍中会起到帮助。

条件语句可以通过如下的方式实现：

- if
- if else
- if else if else
- switch
- 三元运算符

### if

在JavaScript和其他编程语言中，_if_ 关键字用于确定某个条件是否为true并执行对应的代码。要创建if条件，我们需要有if关键字，用括号扩起来的条件语句和花括号（{}）扩起来的代码块。

```js
// syntax
if (condition) {
  //this part of code run for truthy condition
}
```

**Example:**

```js
let num = 3
if (num > 0) {
  console.log(`${num} is a positive number`)
}
//  3 is a positive number
```

```js
let isRaining = true
if (isRaining) {
  console.log('Remember to take your rain coat.')
}
```

正如你所见的上面例子，3大于0 所以条件是true。对应的block将会被执行。但是如果条件语句为false，我们将看不到任何的结果输出。第二个例子也是同样道理。isRaining如果为false，对应的block也不会输出结果。为了看到条件语句值为false时候的执行效果可以使用 _else_ 关键字。

### if else

If condition is true the first block will be executed, if not the else condition will be executed.

如果条件为true则第一个block将会执行，如果不为true就会执行else对应的block。

```js
// syntax
if (condition) {
  // this part of code run for truthy condition
} else {
  // this part of code run for false condition
}
```

```js
let num = 3
if (num > 0) {
  console.log(`${num} is a positive number`)
} else {
  console.log(`${num} is a negative number`)
}
//  3 is a positive number

num = -3
if (num > 0) {
  console.log(`${num} is a positive number`)
} else {
  console.log(`${num} is a negative number`)
}
//  -3 is a negative number
```

```js
let isRaining = true
if (isRaining) {
  console.log('You need a rain coat.')
} else {
  console.log('No need for a rain coat.')
}
// You need a rain coat.

isRaining = false
if (isRaining) {
  console.log('You need a rain coat.')
} else {
  console.log('No need for a rain coat.')
}
// No need for a rain coat.
```

The above condition is false, therefore the else block was executed. How about if our condition is more than two, we will use *else if* conditions.

### if else if else

On our daily life, we make decision on daily basis. We make decision not by checking  one or two conditions instead we make decisions based on multiple conditions. As similar to our daily life, programming is also full conditions. We use *else if* when we have multiple conditions.

```js
// syntax
if (condition) {
     // code
} else if (condition) {
   // code
} else {
    //  code

}
```

**Example:**

```js
let a = 0
if (a > 0) {
  console.log(`${a} is a positive number`)
} else if (a < 0) {
  console.log(`${a} is a negative number`)
} else if (a == 0) {
  console.log(`${a} is zero`)
} else {
  console.log(`${a} is not a number`)
}
```

```js
// if else if else
let weather = 'sunny'
if (weather === 'rainy') {
  console.log('You need a rain coat.')
} else if (weather === 'cloudy') {
  console.log('It might be cold, you need a jacket.')
} else if (weather === 'sunny') {
  console.log('Go out freely.')
} else {
  console.log('No need for rain coat.')
}
```

### Switch

Switch  is an alternative for **if else if else else**.
The switch statement starts with a switch keyword followed by a parenthesis and code block. Inside the code block we will have different cases. Case block run if the value in the switch statement parenthesis match with the case vale. The break is to terminate and it does not go down after the condition is satisfied.  The default block run if all the cases don't satisfy the condition.

```js
switch(caseValue){
  case 1:
    // code
    break
  case 2:
   // code
   break
  case 3:
  // code
  default:
   // code
}
```

```js
let weather = 'cloudy'
switch (weather) {
  case 'rainy':
    console.log('You need a rain coat.')
    break
  case 'cloudy':
    console.log('It might be cold, you need a jacket.')
    break
  case 'sunny':
    console.log('Go out freely.')
    break
  default:
    console.log(' No need for rain coat.')
}

// Switch More Examples
let dayUserInput = prompt('What day is today ?')
let day = dayUserInput.toLowerCase()

switch (day) {
  case 'monday':
    console.log('Today is Monday')
    break
  case 'tuesday':
    console.log('Today is Tuesday')
    break
  case 'wednesday':
    console.log('Today is Wednesday')
    break
  case 'thursday':
    console.log('Today is Thursday')
    break
  case 'friday':
    console.log('Today is Friday')
    break
  case 'saturday':
    console.log('Today is Saturday')
    break
  case 'sunday':
    console.log('Today is Sunday')
    break
  default:
    console.log('It is not a week day.')
}

```

### Ternary Operators

Another way to write conditionals is using ternary operators. We have covered this in other sections but we should also mention it here.

```js
let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
```

🌕  You are extraordinary and you have a remarkable potential. You have just completed day 4 challenges and you are four steps a head in to your way to greatness. Now do some exercises for your brain and for your muscle.  

## 💻 Exercises

### Exercises: Level 1

1. Get user input using prompt(“Enter your age:”). If user is 18 or older , give feedback:You are old enough to drive but if not 18 give feedback to wait for the years he supposed to wait for.

   ```sh
   Enter your age: 30
   You are old enough to drive.

   Enter your age:15
   You are left with 3 years to drive.
   ```

1. Compare the values of myAge and yourAge using if … else. Based on the comparison log to console who is older (me or you). Use prompt(“Enter your age:”) to get the age as input.

   ```sh
   Enter your age: 30
   You are 5 years older than me.
   ```

1. If a is greater than b return 'a is greater than b' else 'a is less than b'. Try to implement in to ways

    - using if else
    - ternary operator.

    ```js
      let a = 4
      let b = 3
    ```

    ```sh
      4 is greater than 3
    ```

1. Even numbers are divisible by 2 and the remainder is zero. How do you check if a number is even or not using JavaScript?

    ```sh
    Enter a number: 2
    2 is an even number

    Enter a number: 9
    9 is is an odd number.
    ```

### Exercises: Level 2

1. Write a code which  can give grade to students according to theirs scores:
   - 80-100, A
   - 70-89, B
   - 60-69, C
   - 50-59, D
   - 0-49, F
1. Check if the season is Autumn, Winter, Spring or Summer.
   If the user input is:
   - September, October or November, the season is Autumn.
   - December, January or February, the season is Winter.
   - March, April or May, the season is Spring
   - June, July or August, the season is Summer
1. Check if a day is weekend day or a working day. Your script will take day as an input.

```sh
    What is the day is today? Saturday
    Saturday is a weekend day.

    What is the day today? saturDaY
    Saturday is a weekend day.

    What is the day today? Friday
    Friday is a work day.

    What is the day today? FrIDAy
    Friday is a work day.
  ```

### Exercises: Level 3

1. Write a program which tells the number days in a month.

  ```sh
    Enter month: January
    January has 31 days.

    Enter month: JANUARY
    January has 31 day

    Enter month: February
    February has 28 days.

    Enter month: FEbruary
    February has 28 days.
  ```

🎉 CONGRATULATIONS ! 🎉

[<< Day 3](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/03_Day/03_booleans_operators_date.md) | [Day 5 >>](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/05_Day/05_day_arrays.md)
