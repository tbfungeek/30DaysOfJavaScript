<div align="center">
  <h1> JavaScript 30天挑战</h1>
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

[<< 第二天](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/02_Day/02_day_data_types.md) | [第四天 >>](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/04_Day/04_day_conditionals.md)

![JavaScript 第三天挑战](../images/banners/day_1_3.png)

- [📔 第三天](#%f0%9f%93%94-day-3)
  - [Booleans](#booleans)
    - [True 值](#truthy-values)
    - [False 值](#falsy-values)
  - [Undefined](#undefined)
  - [Null](#null)
  - [操作符](#operators)
    - [赋值操作符](#assignment-operators)
    - [算术操作符](#arithmetic-operators)
    - [比较操作符](#comparison-operators)
    - [逻辑操作符](#logical-operators)
    - [自增操作符](#increment-operator)
    - [自减操作符](#decrement-operator)
    - [三元操作符]](#ternary-operators)
    - [符号优先级](#operator-precendence)
  - [Window 方法](#window-methods)
    - [Window alert() 方法](#window-alert-method)
    - [Window prompt() 方法](#window-prompt-method)
    - [Window confirm() 方法](#window-confirm-method)
  - [Date 对象](#date-object)
    - [创建 time 对象](#creating-a-time-object)
    - [获取完整的年份](#getting-full-year)
    - [获取月份](#getting-month)
    - [获取date](#getting-date)
    - [获取天](#getting-day)
    - [获取小时](#getting-hours)
    - [获取分钟](#getting-minutes)
    - [获取秒](#getting-seconds)
    - [获取time]](#getting-time)
  - [💻 第三天练习](#%f0%9f%92%bb-day-3-exercises)
    - [练习: 等级1](#exercises-level-1)
    - [练习: 等级2](#exercises-level-2)
    - [练习: 等级3](#exercises-level-3)

# 📔 第三天

## Booleans

boolean 代表一个包含 _true_ 或者 _false_ 两种可能值的数据类型。在进行比较操作的时候使用这些操作符号会让逻辑变得更清晰。任何比较都会返回一个布尔值，该布尔值可以为true或false。

**练习: Boolean 值**

```js
let isLightOn = true
let isRaining = false
let isHungry = false
let isMarried = true
let truValue = 4 > 3    // true
let falseValue = 4 < 3  // false
```

### True 值

- 除了zero之外的所有numbers数据都是True
- 所有的string类型都是True
- 值为True的变量

### False 值

- 0
- 0n
- null
- undefined
- NaN
- false 布尔值
- '', "", ``, 空字符


## Undefined

如果我们声明了一个变量，在我们未给它赋值之前它的值是undefined。在一个方法没有返回值的情况下它的返回值被认为是undefined

```js
let firstName
console.log(firstName) //not defined, because it is not assigned to a value yet
```

## Null

```js
let empty = null
console.log(empty) // -> null , means no value
```

## 操作符

### 赋值操作符

在JavaScript中等号属于赋值符号，它用于将一个值赋给一个变量。

```js
let firstName = 'Asabeneh'
let country = 'Finland'
```

### 算术操作符

算术操作符是一系列数学符号


- 加号(+): a + b
- 减号(-): a - b
- 乘号(*): a * b
- 除号(/): a / b
- 去余数(%): a % b
- 指数覆盖(**): a ** b

```js
let numOne = 4
let numTwo = 3
let sum = numOne + numTwo
let diff = numOne - numTwo
let mult = numOne * numTwo
let div = numOne / numTwo
let remainder = numOne % numTwo
let powerOf = numOne ** numTwo

console.log(sum, diff, mult, div, remainder, powerOf) // 7,1,12,1.33,1, 64

```

```js
let PI = 3.14
let radius = 100          // length in meter

const gravity = 9.81      // in m/s2
let mass = 72             // in Kilogram
const boilingPoint = 100  // temperature in oC, boiling point of water
const bodyTemp = 37       // body temperature in oC

//Let us calculate area of a circle
const areaOfCircle = PI * radius * radius
console.log(areaOfCircle)  //  314 m

// Let us calculate weight of an object
const weight = mass * gravity
console.log(weight)        // 706.32 N(Newton)

//Concatenating string with numbers using string interpolation
/*
 The boiling point of water is 100 oC.
 Human body temperature is 37 oC.
 The gravity of earth is 9.81 m/s2.
 */
console.log(
  `The boiling point of water is ${boilingPoint} oC.\nHuman body temperature is ${bodyTemp} oC.\nThe gravity of earth is ${gravity} m / s2.`
)
```

### 比较操作符

在代码中我们一般会遇到比较数值大小的情况，这种情况下我们使用比较操作符来比较某个数值是大于，小于还是等于另一个数值。

![Comparison Operators](../images/comparison_operators.png)
**例子: 比较操作符**

```js
console.log(3 > 2)              // true, because 3 is greater than 2
console.log(3 >= 2)             // true, because 3 is greater than 2
console.log(3 < 2)              // false,  because 3 is greater than 2
console.log(2 < 3)              // true, because 2 is less than 3
console.log(2 <= 3)             // true, because 2 is less than 3
console.log(3 == 2)             // false, because 3 is not equal to 2
console.log(3 != 2)             // true, because 3 is not equal to 2
console.log(3 == '3')           // true, compare only value
console.log(3 === '3')          // false, compare both value and data type
console.log(3 !== '3')          // true, compare both value and data type
console.log(3 !== '3')          // true, compare both value and data type
console.log(3 != 3)             // false, compare only value
console.log(3 !== 3)            // false, compare both value and data type
console.log(0 == false)         // true, equivalent
console.log(0 == '')            // true, equivalent
console.log(0 == ' ')           // true, equivalent
console.log(0 === '')           // false, not exactly the same
console.log(0 === false)        // false, not exactly the same
console.log(1 == true)          // true, equivalent
console.log(1 === true)         // false, not exactly the same
console.log(undefined == null)  // true
console.log(undefined === null) // false
console.log(NaN == NaN)         // false, not equal
console.log(NaN === NaN)        // false
console.log(typeof NaN)         // number

console.log('mango'.length == 'avocado'.length)  // false
console.log('mango'.length != 'avocado'.length)  // true
console.log('mango'.length < 'avocado'.length)   // true
console.log('milk'.length != 'meat'.length)      // false
console.log('milk'.length == 'meat'.length)      // true
console.log('tomato'.length == 'potato'.length)  // true
console.log('python'.length > 'dragon'.length)   // false
```

尝试通过上面的逻辑理解上述的比较操作符，不通过任何逻辑只是干巴巴强行记忆可能会比较难以理解。JavaScript在某种意义上是一种宽泛数据类型的编程语言。但是除非我们非常擅长，否则可能返回并非我们期望的结果。

根据以往经验，如果==的值不为true，则===的值也不应该相等。使用===比使用==更安全。以下
[link](https://dorey.github.io/JavaScript-Equality-Table/)具有数据类型比较的详尽列表。

### 逻辑操作符

下面是一些常见的逻辑操作符：&&(与) , ||(或) and !(非). && 只有在两边操作数都是真的时候才返回真. || 在一个操作数为真的时候就会返回真。! 会在操作数为真的时候返回false，操作数为false的时候返回true。

```js
//&& ampersand operator example

const check = 4 > 3 && 10 > 5 // true && true -> true
const check = 4 > 3 && 10 < 5 // true && false -> false
const check = 4 < 3 && 10 < 5 // false && false -> false

//|| pipe or operator, example

const check = 4 > 3 || 10 > 5 // true  || true -> true
const check = 4 > 3 || 10 < 5 // true  || false -> true
const check = 4 < 3 || 10 < 5 // false || false -> false

//! Negation examples

let check = 4 > 3            // true
let check = !(4 > 3)         //  false
let isLightOn = true
let isLightOff = !isLightOn  // false
let isMarried = !false       // true
```

### 自增操作符

JavaScrip中我们使用自增操作符来对存储在一个变量中的数值进行加1操作。自增操作符号又可分成前缀自增和后缀自增。我们借下来来看下它们的用法：

1. 前置自增

```js
let count = 0
console.log(++count) // 1
console.log(count)   // 1
```

1. 后置自增

```js
let count = 0
console.log(count++) // 0
console.log(count)  // 1
```

我们用得最多的是后置自增，你至少需要知道如何使用后置自增操作符。

### 自减操作符

JavaScrip中我们使用自减操作符来对存储在一个变量中的数值进行减1操作。自减操作符号又可分成前缀自减和后缀自减。我们借下来来看下它们的用法：

1. 前置自减

```js
let count = 0
console.log(--count) // -1
console.log(count)  // -1
```

1. 后置自减

```js
let count = 0
console.log(count--) // 0
console.log(count)   // -1
```

### 三目运算符

可以使用三目运算符来编写一个条件语句。大家可以看下如下例子来看下怎么使用三目运算符:


```js
let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
isRaining = false

isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
```

```sh
You need a rain coat.
No need for a rain coat.
```

```js
let number = 5
number > 0
  ? console.log(`${number} is a positive number`)
  : console.log(`${number} is a negative number`)
number = -5

number > 0
  ? console.log(`${number} is a positive number`)
  : console.log(`${number} is a negative number`)
```

```sh
5 is a positive number
-5 is a negative number
```

### 操作符优先级

关于操作符优先级部分这里推荐大家阅读下面的文档：

[link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)

## Window 方法

### Window alert() 方法

如你刚开始看到的那样，alert()方法显示一个带有指定消息和OK按钮的警报框。这是一个内置方法，它带有参数。

```js
alert(message)
```

```js
alert('Welcome to 30DaysOfJavaScript')
```

不要使用过多的警报，因为它会带给用户烦人的感觉，最好仅将其用于测试。

### Window prompt() 方法

window prompt方法会在浏览器上显示一个带有输入的提示框，以获取输入值，并且输入数据可以存储在变量中。

```js
prompt('required text', 'optional text')
```

```js
let number = prompt('Enter number', 'number goes here')
console.log(number)
```

### Window confirm() 方法

Confirm()方法会显示一个对话框，其中包含指定的消息以及“确定”和“取消”按钮。确认框通常用于请求用户许可以执行某项操作。窗口confirm（）将字符串作为参数。单击“确定”将产生真值，单击“取消”按钮将产生假值。

```js
const agree = confirm('Are you sure you like to delete? ')
console.log(agree) // result will be true or false based on what you click on the dialog box
```

上述部分并非全部的window方法。我们会在接下来的章节中进一步深入介绍window 方法

## Date 对象

时间是一个十分重要的东西，我们可能需要知道某个活动或者事件的时期，在JavaScript 当前时间和日期是通过JavaScript对象创建的。我们通过Date类创建的对象提供了许多方法来操作日期和时间。我们用于获取时间和日期信息的方法一般以 _get_开头。 
_getFullYear(), getMonths(), getDate(), getDay(), getHours(), getMinutes, getSeconds(), getMilliseconds(), getTime(), getDay()_
![Date time Object](../images/date_time_object.png)

### 创建一个时间对象

一旦我们创建了时间对象，时间对象将会提供关于时间的信息，接下来让我们创建一个时间对象：

```js
const now = new Date()
console.log(now) // Sat Jan 04 2020 00:56:41 GMT+0200 (Eastern European Standard Time)
```

我们已经创建了一个时间对象，我们可以通过我们上面表格提到的方法来访问时间信息。

### 获取完整的年份

我们试着从一个时间对象中抽取完整的年份信息。

```js
const now = new Date()
console.log(now.getFullYear()) // 2020
```

### 获取月份信息

我们试着从一个时间对象中抽取完整的月份信息。

```js
const now = new Date()
console.log(now.getMonth()) // 0, because the month is January,  month(0-11)
```

### 获取日期信息

让我们试着从一个时间对象获取日期信息。

```js
const now = new Date()
console.log(now.getDate()) // 4, because the day of the month is 4th,  day(0-31)
```

### 获取天数信息

让我们试着从一个时间对象获取一周中的第几天信息。

```js
const now = new Date()
console.log(now.getDay()) // 6, because the day is Saturday which is the 5th day,
// Getting the weekday as a number (0-6)
```

### 获取小时信息

让我们试着从一个时间对象获取小时信息。

```js
const now = new Date()
console.log(now.getHours()) // 0, because the time is 00:56:41
```

### 获取分钟信息

让我们试着从一个时间对象获取分钟信息。

```js
const now = new Date()
console.log(now.getMinutes()) // 56, because the time is 00:56:41
```

### 获取秒信息

让我们试着从一个时间对象获取秒信息。

```js
const now = new Date()
console.log(now.getSeconds()) // 41, because the time is 00:56:41
```

### 获取 time 信息

这个方法将会给出距离1970年1月1日的毫秒数，同时它也是一个Unix时间。我们可以以如下几种方式获得unix时间。


1. 通过 _getTime()_

```js
const now = new Date() //
console.log(now.getTime()) // 1578092201341, this is the number of seconds passed from January 1, 1970 to January 4, 2020 00:56:41
```

1. 通过 _Date.now()_

```js
const allSeconds = Date.now() //
console.log(allSeconds) // 1578092201341, this is the number of seconds passed from January 1, 1970 to January 4, 2020 00:56:41

const timeInSeconds = new Date().getTime()
console.log(allSeconds == timeInSeconds) // true
```

接下来我们就可以将时间格式化为可读的形式。

**Example:**

```js
const now = new Date()
const year = now.getFullYear() // return year
const month = now.getMonth() + 1 // return month(0 - 11)
const date = now.getDate() // return date (1 - 31)
const hours = now.getHours() // return number (0 - 23)
const minutes = now.getMinutes() // return number (0 -59)

console.log(`${date}/${month}/${year} ${hours}:${minutes}`) // 4/1/2020 0:56
```

## 💻 第三天练习

### Exercises: Level 1

1. Declare firstName, lastName, country, city, age, isMarried, year variable and assign value to it and use the typeof operator to check different data types.
2. Check if type of '10' is equal to 10
3. Check if parseInt('9.8') is equal to 10
4. Boolean value is either true or false.
   1. Write three JavaScript statement which provide truthy value.
   2. Write three JavaScript statement which provide falsy value.

5. Figure out the result of the following comparison expression first without using console.log(). After you decide the result confirm it using console.log()
   1. 4 > 3
   2. 4 >= 3
   3. 4 < 3
   4. 4 <= 3
   5. 4 == 4
   6. 4 === 4
   7. 4 != 4
   8. 4 !== 4
   9. 4 != '4'
   10. 4 == '4'
   11. 4 === '4'
   12. Find the length of python and jargon and make a falsy comparison statement.

6. Figure out the result of the following expressions first without using console.log(). After you decide the result confirm it by using console.log()
   1. 4 > 3 && 10 < 12
   2. 4 > 3 && 10 > 12
   3. 4 > 3 || 10 < 12
   4. 4 > 3 || 10 > 12
   5. !(4 > 3)
   6. !(4 < 3)
   7. !(false)
   8. !(4 > 3 && 10 < 12)
   9. !(4 > 3 && 10 > 12)
   10. !(4 === '4')
   11. There is no 'on' in both dragon and python

7. Use the Date object to do the following activities
   1. What is the year today?
   2. What is the month today as a number?
   3. What is the date today?
   4. What is the day today as a number?
   5. What is the hours now?
   6. What is the minutes now?
   7. Find out the numbers of seconds elapsed from January 1, 1970 to now.

### Exercises: Level 2

1. Write a script that prompt the user to enter base and height of the triangle and calculate an area of a triangle (area = 0.5 x b x h).

   ```sh
   Enter base: 20
   Enter height: 10
   The area of the triangle is 50
   ```

1. Write a script that prompt the user to enter side a, side b, and side c of the triangle and and calculate the perimeter of triangle (perimeter = a + b + c)

   ```sh
   Enter side a: 5
   Enter side b: 4
   Enter side c: 3
   The perimeter of the triangle is 12
   ```

1. Get length and width using prompt and calculate an area of rectangle (area = length x width and the perimeter of rectangle (perimeter = 2 x (length + width))
1. Get radius using prompt and calculate the area of a circle (area = pi x r x r) and circumference of a circle(c = 2 x pi x r) where pi = 3.14.
1. Calculate the slope, x-intercept and y-intercept of y = 2x -2
1. Slope is (m = y2-y1/x2-x1). Find the slope between point (2, 2) and point(6,10)
1. Compare the slope of above two questions.
1. Calculate the value of y (y = x^2 + 6x + 9). Try to use different x values and figure out at what x value y is 0.
1. Writ a script that prompt a user to enters hours and rate per hour. Calculate pay of the person?

    ```sh
    Enter hours: 40
    Enter rate per hour: 28
    Your weekly earning is 1120
    ```

1. If the length of your name is greater than 7 say, your name is long else say your name is short.
1. Compare your first name length and your family name length and you should get this output.

    ```js
    let firstName = 'Asabeneh'
    let lastName = 'Yetayeh'
    ```

    ```sh
    Your first name, Asabeneh is longer than your family name, Yetayeh
    ```

1. Declare two variables _myAge_ and _yourAge_ and assign them initial values and myAge and yourAge.

   ```js
   let myAge = 250
   let yourAge = 25
   ```

   ```sh
   I am 225 years older than you.
   ```

1. Using prompt get the year the user was born and if the user is 18 or above allow the user to drive if not tell the user to wait a certain amount of years.

    ```sh

    Enter birth year: 1995
    You are 25. You are old enough to drive

    Enter birth year: 2005
    You are 15. You will be allowed to drive after 3 years.
    ```

1. Write a script that prompt the user to enter number of years. Calculate the number of seconds a person can live. Assume some one lives just hundred years

   ```sh
   Enter number of yours you live: 100
   You lived 3153600000 seconds.
   ```

1. Create a human readable time format using the Date time object
   1. YYY-MM-DD HH:mm
   2. DD-MM-YYYY HH:mm
   3. DD/MM/YYY HH:mm

### Exercises: Level 3

1. Create a human readable time format using the Date time object. The hour and the minute should be all time two digits(7 hours should be 07 and 5 minutes should be 05 )
   1. YYY-MM-DD HH:mm eg. 20120-01-02 07:05

🎉 CONGRATULATIONS ! 🎉

[<< Day 2](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/02_Day/02_day_data_types.md) | [Day 4 >>](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/04_Day/04_day_conditionals.md)
