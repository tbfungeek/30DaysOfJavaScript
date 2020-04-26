<div align="center">
  <h1> JavaScript 30天挑战</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/asabeneh?style=social">
  </a>

  <sub>作者:
  <a href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br>
  <small> January, 2020</small>
  </sub>
</div>

[第二天 >>](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/02_Day/02_day_data_types.md)

![JavaScript30天挑战](./images/day_1_1.png)

- [📔第一天](#%f0%9f%93%94day-1)
  - [简介](#introduction)
  - [开始前准备](#requirements)
  - [开始](#setup)
    - [安装 Node.js](#install-nodejs)
    - [浏览器](#browser)
      - [安装 Google Chrome](#installing-google-chrome)
      - [打开 Google Chrome 终端](#opening-google-chrome-console)
      - [使用浏览器终端编写代码](#writing-code-on-browser-console)
        - [使用Console.log](#consolelog)
        - [Console.log 使用多个参数](#consolelog-with-multiple-arguments)
        - [注释](#comment)
        - [语法](#syntax)
      - [算术运算](#arithmetics)
    - [代码编辑器](#code-editor)
      - [安装 Visual Studio Code](#installing-visual-studio-code)
      - [使用Visual Studio Code](#how-to-use-visual-studio-code)
  - [将JavaScript添加到Web页面](#adding-javascript-to-a-web-page)
    - [内部脚本](#inline-script)
    - [内部脚本](#internal-script)
    - [外部脚本](#external-script)
    - [多外部脚本](#multiple-external-scripts)
  - [数据类型介绍](#introduction-to-data-types)
    - [Number](#number)
    - [String](#string)
    - [Booleans](#booleans)
    - [Undefined](#undefined)
    - [Null](#null)
  - [检查数据类型](#checking-data-types)
  - [注释](#comments)
  - [变量](#variables)
- [💻 第一天练习](#%f0%9f%92%bb-day-1-exercises)

# 📔第一天

## 简介

很荣幸你能加入JavaScript30天编程挑战，在这项挑战中你将会学到一名JavaScript程序员所必备的全部技能以及编程概念。加入[telegram 群组](https://t.me/ThirtyDaysOfJavaScript) 在这项挑战的最后你将有机会获得30DaysOfJavaScript 编程挑战的证书，

**30DaysOfJavaScript 挑战** 是一份面向初学者和高级JavaScript开发人员的指南。欢迎大家使用JavaScript，这门浏览器语言，我本人喜欢使用和教授JavaScript，我希望大家也和我一样能够喜欢上JavaScript。

通过这个循序渐进的教程，您将学会JavaScript，这门人类历史上最流行的编程语言。您可以使用JavaScript为你的网站添加交互，可以通过JavaScript来开发移动app，桌面应用，游戏等。现在JavaScript还能用于 **机器学习** 和 **_AI_**.近年来，JavaScript越来越流行，并且连续四年一直处于编程语言领先地位是Github上最常用的编程语言。

## 开始前准备

在这项挑战之前你不需要准备任何等前置知识，你仅仅需要：

1. 学习动机
2. 计算机
3. 网络
4. 浏览器
5. 代码编辑器

## 开始挑战

我相信你有很强的学习动力并且拥有想成为一名开发人员的强烈欲望，只要您有一台能上网的电脑就够了。

### 安装 Node.js

获取你现在不会立刻使用它，但是在后续您会使用到的，安装 [node.js](https://nodejs.org/en/).

![下载Node](images/download_node.png)

在下载后可以双击它安装

 ![安装 node](images/install_node.png)

我们可以通过打开我们设备的终端，或者其他命令行工具敲下如下命令来检查是否已经成功安装到我们本地的机器上。

```sh
asabeneh $ node -v
v12.14.0
```

这里我个人使用推荐的node版本 12.14.0。

### 浏览器

目前有很多浏览器，但我个人推荐Google Chrome浏览器。

#### 安装 Google Chrome

如果你还没有安装[Google Chrome](https://www.google.com/chrome/)，那么在开始前必须先安装下. 我们可以使用Google Chrome 的 console 来编写简短的代码，但是如果要开发应用我们一般不会使用它，而是使用专门的代码编辑器。
![Google Chrome](images/google_chrome.png)

#### 打开 Google Chrome Console

你可以通过点击Google Chrome 浏览器右上角的三个点按钮，或者通过快捷键打开Google Chrome Console。个人偏向使用快捷键方式。

![Opening chrome](images/opening_developer_tool.png)

通过快捷键打开Chrome Console

```sh
Mac 环境下
Command+Option+I

Windows 环境下:
Ctl+Shift+I
```

![Opening console](images/opening_chrome_console_shortcut.png)

打开Google Chrome终端后，大家可以尝试各个主要的功能，后续我们将会花费很多时间在Console上练习。我们会在控制台输入我们的代码, Google Console V8引擎会将我们的JavaScript代码转换为机器代码。

让我们尝试在Google Chrome console 输入JavaScript代码：

![write code on console](./images/js_code_on_chrome_console.png)

#### 在浏览器终端编写代码

我们可以在Google console 或者其他任意的浏览器终端编写JavaScript代码。但是这个挑战中我们重点使用Google Chrome console。可以通过下面的方式打开Google Chrome console。


```sh
Mac
Command+Option+I

Windows:
Ctl+Shift+I
```

##### Console.log

我们首先使用一个内置的方法 **console.log()**来编写我们的第一个JavaScript代码。我们传递一个参数作为输入数据，然后 **console.log()** 方法显示输出结果。下面的例子中我们传递'Hello, World' 作为输入数据或者console.log()的参数。

```js
console.log('Hello, World!')
```

##### 多参数 Console.log 

console.log(param1, param2, param3)可以传入多个参数:

![console log multiple arguments](./images/console_log_multipl_arguments.png)

```js
console.log('Hello', 'World', '!')
console.log('HAPPY', 'NEW', 'YEAR', 2020)
console.log('Welcome', 'to', 30, 'Days', 'Of', 'JavaScript')
```

正如上面的代码片段所示， *console.log()* 可以携带多个参数。 恭喜你，已经学会用*console.log()*写你的第一行JavaScript代码了。

##### 注释

注释对于提高代码的可读性有很大帮助，JavaScript不会执行代码的注释部分，在JavaScript中，任何使用//开头或者被/* */包裹的内容都会被作为代码注释。

** 例子: 单行注释**

 // This is the first comment  
 // This is the second comment  
 // I am a single line comment  

**例子: 多行注释**

  /*
  This is a multiline comment  
  Multiline comments can take multiple lines  
  JavaScript is the language of the web  
  */

##### 句法

JavaScript是一种编程语言。它和其他编程语言一样有自己的语法。如果我们编写的JavaScript语法没有符合语法要求，将引发不同类型的错误。稍后我们将探讨各种JavaScript错误。现在让我们看看语法错误。


![Error](images/raising_syntax_error.png)


上面的代码中我制造了一个错误来作为例子。控制台相应触发了语法错误，并给出了错误提示信息，这些错误提示信息非常有用。它告知我们犯了哪种类型的错误。通过阅读错误反馈信息，我们可以快速定位到问题通过调试更正语法并解决问题。


```js
console.log("Hello, World!")
console.log('Hello, World!')
```

到目前为止我们学会了如何使用*console.log()*，如果我们要输出文本或者字符串需要将文本或者字符串使用单引号，双引号或者反双引号括起来。

**例子:**

```js
console.log("Hello, World!")
console.log('Hello, World!')
console.log(`Hello, World!`)
```

#### 运算

接下来让我们使用*console.log()*在google chrome 终端中编写更多的JavaScript代码。除了输出文本之外我们还可以使用JavaScript来做算术运算。让我们来尝试做下面的简单计算。


![Arithmetic](images/arithmetic.png)

```js
console.log(2 + 3)   // Addition
console.log(3 - 2)   // Subtraction
console.log(2 * 3)   // Multiplication  
console.log(3 / 2)   // Division
console.log(3 % 2)   // Modulus - finding remainder
console.log(3 ** 2)  // Exponential
```

### 代码编辑器

虽然我们可以使用浏览器的console来编写代码，但是这种方式不适合大的工程，在现实开发环境中，开发者一般使用不同的代码编辑器来编写代码。在我们30天JavaScript挑战中我们推荐使用visual studio code。

#### 安装Visual studio code 

Visual studio code 是一个非常受欢迎的开源文本编辑器，个人推荐大家下载使用 Visual studio code [download](https://code.visualstudio.com/)作为编辑器，但是如果你有自己喜欢的编辑器，大家可以根据自己的意愿来选择。 

![Vscode](images/vscode.png)

如果你安装了visual studio code，就开始使用它吧。

#### 如何使用 visual studio code

双击打开visual studio code，当我们打开后我们可以看到下面的界面。大家可以尝试点击这些按钮来体验这些功能。

![Vscode ui](./images/vscode_ui.png)

![Vscode add project](./images/adding_project_to_vscode.png)

![Vscode open project](./images/opening_project_on_vscode.png)

![script file](images/scripts_on_vscode.png)

![running script](./images/running_script.png)

![coding running](./images/launched_on_new_tab.png)

## 往Web页面中添加JavaScript

JavaScript 可以通过如下三种方式添加到网页上:

- **_内联脚本_**
- **_内置脚本_**
- **_外部脚本_**
- **_多外部脚本_**

接下来的部分将展示往网页中添加JavaScript代码的不同方式：

### 内联脚本

在桌面或者任意地方创建一个30DaysOfJS的文件夹，在新创建的项目文件夹下新建一个**_index.html_** 文件。然后将下面的代码粘贴到文件上。使用浏览器打开。
[Chrome](https://www.google.com/chrome/).

```html
<!DOCTYPE html>
  <html>
    <head>
      <title>30DaysOfScript:Inline Script</title>
    </head>
    <body>
      <button onclick="alert('Welcome to 30DaysOfJavaScript!')">Click Me</button>
    </body>
  </html>
```

现在你可以往上面代码中添加第一个内联脚本。我们可以使用内置的 *alert()*方法 创建一个弹出的警告消息。

### 内部脚本

内部脚本可以放置在_head_或者_body_中。但是一般建议将它放在HTML文档的body中。首先我们先将它放置在页面的head部分：

```html
<!DOCTYPE html>
  <html>
    <head>
       <title>30DaysOfScript:Internal Script</title>
      <script>
        console.log("Welcome to 30DaysOfJavaScript")
      </script>
    </head>
    <body>
    </body>
  </html>
```

在body部分中编写JavaScript代码是最可取的地方。接下来我们来看下我们大部分情况下编写内部脚本的方式:

```html
<!DOCTYPE html>
  <html>
    <head>
      <title>30DaysOfScript:Internal Script</title>
    </head>
    <body>
       <button onclick="alert('Welcome to 30DaysOfJavaScript!');">Click Me</button>
      <script>
        console.log("Welcome to 30DaysOfJavaScript");
      </script>
    </body>
  </html>
```

打开浏览器控制台可以看到console.log（）的输出。


![js code from vscode](./images/js_code_vscode.png)

### External script

和内部脚本类似，外部脚本可以放在head或者body，一般推荐放在body。我们首先创建一个使用.js结尾的外部JavaScript文件。在这里我们将在项目目录中创建一个introduction.js 然后在body的最后通过如下代码将js文件链接进来。

```js
console.log('Welcome to 30DaysOfJavaScript')
```

External scripts in the head

```html
<!DOCTYPE html>
  <html>
    <head>
      <title>30DaysOfJavaScript:External script</title>
      <script src="introduction.js"></script>
    </head>
    <body>
    </body>
    </html>
```

将外部脚本放置在body中的例子：

```html
<!DOCTYPE html>
  <html>
    <head>
      <title>30DaysOfJavaScript:External script</title>
    </head>
    <body>
      //it could be in the header or in the body
      // Here is the recommended place to put the external script
      <script src="introduction.js"></script>
    </body>
    </html>
```

### 多外部脚本

我们可以链接多个外部JavaScript文件到一个网页中。接下来我们在项目文件夹中创建一个helloworld.js文件，并添加如下代码。

```js
console.log('Hello, World!')
```

```html
<!DOCTYPE html>
  <html>
    <head>
      <title>Multiple External Scripts</title>
    </head>
    <body>

      <script src ="./helloworld.js"></script>
      <script src="./introduction.js"></script>
    </body>
  </html>
```

大家在练习的时候需要注意一点：你们的main.js文件应该放在其他外部脚本的最后面。

![Multiple Script](./images/multiple_script.png)

## Introduction to Data types

In JavaScript and also other programming languages, there are different kinds of data types. The following are JavaScript primitive data types:_String, Number, Boolean, undefined, Null_, and _Symbol_.

### Number

- Integer: Integer(negative, zero and positive) numbers
        Example:
        ... -3, -2, -1, 0, 1, 2, 3 ...
- Float: Decimal number
        Example
        ... -3.5, -2.25, -1.0, 0.0, 1.1, 2.2, 3.5 ...

### String

A collection of one or more characters under a single quote, double-quote, or backtick.
**Example:**

```js
'Asabeneh'
'Finland'
'JavaScript is a beautiful programming language'
"I love teaching"
'I hope you are enjoying the first day'
`We can also create a string using a backtick`
```

### Booleans

A boolean value is either true or false. Any comparisons return a boolean value, which is either true or false.

A boolean data type is either a True or False value.

**Example:**

```js
    true  // if the light on ,the value is true
    false // if the light off, the value is False
```

### Undefined

In JavaScript, if we don't assign a value to a variable, the value is undefined. In addition to that, if a function is not returning anything, it returns undefined.

```js
let firstName;
console.log(firstName); //not defined, because it is not assigned to a value yet
```

### Null

Null in JavaScript means an empty value.

```js
let emptyValue = null
```

## Checking Data types

To check the data type of a certain data type, we use the **typeof** operator. See the following example.

```js
console.log(typeof 'Asabeneh') // string
console.log(typeof 5)          // number
console.log(typeof true )      // boolean
console.log(typeof null)       // object type
console.log(typeof undefined)  // undefined
```

## Comments

Commenting in JavaScript is similar to other programming languages. Comments are important in making your make code more readable.
There are two ways of commenting:

- _Single line commenting_
- _Multiline commenting_

```js
// commenting the code itself with a single comment
// let firstName = 'Asabeneh'; single line comment
// let lastName = 'Yetayeh'; single line comment
```

Multiline commenting:

```js
/*
    let location = 'Helsinki';
    let age = 100;
    let isMarried = true;
    This is a Multiple line comment
    */
```

## Variables

Variables are _containers_ of data. Variables used to _store_ data in a memory location. When a variable is declared, a memory location is reserved. When a variable is assigned to a value (data), the memory space will be filled with that data. To declare a variable, we use _var_, _let_, or _const_ keywords. We will talk more about var, let, and const in detail in other sections (scope). For now, the above explanation is enough.

For a variable that changes at a different time, we use _let_. If the data does not change at all, we use _const_. For example, PI, country name, gravity do no change, and we can use *const*.

- A JavaScript variable name  should not begin with a number.
- A JavaScript variable name does not allow special characters except dollar sign and underscore.
- A JavaScript variable name follows a camelCase convention.
- A JavaScript variable name should not have space between words.

The following are valid examples of JavaScript variables.
Valid variables in JavaScript:

```js
    firstName
    lastName
    country
    city
    capitalCity
    age
    isMarried

    first_name
    last_name
    is_marreid
    capital_city

    num1
    num_1
    _num_1
    $num1
    year2020
    year_2020
```

camelCase or the first way of declaring is conventional in JavaScript. In this material, we will use camelCase variables.
Invalid variable:

```sh
  first-name
  1_num
  num_#_1
```

Let us declare variables with different data types. To declare a variable, we need to use let or const keyword before the variable name. Following the variable name, we write an equal sign (assignment operator), and a value.

```js
  # Syntax
  let nameOfVariable = value  
```

**Examples: Variables**

```js
// Declaring different variables of different data types
let firstName = 'Asabeneh' // first name of a person
let lastName = 'Yetayeh' // last name of a person
let country = 'Finland' // country
let city = 'Helsinki' // capital city
let age = 100 // age in years
let isMarried = true

console.log(firstName, lastName, country, city, age, isMarried)
```

```sh
Asabeneh Yetayeh Finland Helsinki 100 True
```

```js
// Declaring variables with number values
let age = 100             // age in years
const gravity = 9.81      // earth gravity  in m/s2
const boilingPoint = 100  // water boiling point, temperature in oC
const PI = 3.14           // geometrical constant

console.log(gravity, boilingPoint, PI)
```

```sh
9.81 100 3.14
```

```js
// Variables can also be declaring in one line separated by comma
let name = 'Asabeneh', // name of a person
  job = 'teacher',
  live = 'Finland';
console.log(name, job, live);
```

```sh
Asabeneh teacher Finland
```

When you run the files on 01-Day folder you should get this:

![Day one](./images/day_1.png)

🌕  You are amazing. You have just completed day 1 challenge and you are in your way to greatness. Now do some exercises for your brain and for your muscle.

# 💻 Day 1: Exercises

1. Write a single line comment which says, _comments can make code readable_
2. Write another single comment which says, *welcome to 30DaysOfJavaScript*
3. Write a multiline comment which says, _comments can make code readable, easy to use_
   _and informative_

4. Create a variable.js file and declare variables and assign string, boolean, undefined and null data types
5. Create datatypes.js file and use the JavaScript ***typeof*** operator to check different data types. Check the data type of each variable
6. Declare four variables without assigning values
7. Declare four variables with assigning values
8. Declare variables to store your first name, last name, marital status, country and age in multiple lines
9. Declare variables to store your first name, last name, marital status, country and age in a single line
10. Declare two variables _myAge_ and _yourAge_ and assign them initial values and log to the browser console.

   ```sh
   I am 25 years old.
   You are 30 years old.
   ```

🎉 CONGRATULATIONS ! 🎉

[Day 2 >>](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/02_Day/02_day_data_types.md)
