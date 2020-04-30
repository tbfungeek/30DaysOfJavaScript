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
</div>

[<< Day 1](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/readMe.md) | [Day 3 >>](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/03_Day/03_booleans_operators_date.md)

![JavaScript 30天挑战](../images/banners/day_1_2.png)

- [📔 第二天](#%f0%9f%93%94-day-2)
  - [数据类型](#data-types)
    - [元数据类型](#primitive-data-types)
    - [非元数据类型](#non-primitive-data-types)
  - [Numbers](#numbers)
    - [声明number数据类型](#declaring-number-data-types)
    - [Math 对象](#math-object)
      - [随机数生成器](#random-number-generator)
  - [Strings](#strings)
    - [拼接字符串](#string-concatenation)
      - [使用加号拼接字符串](#concatenating-using-addition-operator)
      - [长字符串](#long-literal-strings)
      - [字符串中的转义字符](#escape-sequences-in-string)
      - [模版字符串](#template-literalstemplate-strings)
    - [String 方法](#string-methods)
  - [检查和类型转换](#checking-data-types-and-casting)
    - [检查数据类型](#checking-data-types)
    - [转换数据类型](#changing-data-typecasting)
      - [String 转 Int](#string-to-int)
      - [String 转 Float](#string-to-float)
      - [Float 转 Int](#float-to-int)
  - [💻 第二天练习](#%f0%9f%92%bb-day-2-exercises)
    - [训练题: Level 1](#exercise-level-1)
    - [训练题: Level 2](#exercise-level-2)
    - [训练题: Level 3](#exercises-level-3)

# 📔 第二天

## 数据类型

在上一章节我们提到了一点关于数据类型的内容。数据或者值都有自己的数据类型，数据类型描述了数据的特征，它可以分成如下两类：

1. 元数据类型
2. 非元数据类型

### 元数据类型

在JavaScript中元数据类型包括：

 1. Numbers - 整型，浮点姓类型
 2. Strings - 任何通过单引号或者双引号扩起来的内容
 3. Booleans - 用于存放true or false值的类型
 4. Null - 空值或者无数据
 5. Undefined - 未初始化的类型

在JavaScript中非元数据类型包括：

1. Objects 对象
2. Functions 方法
3. Arrays 数组

接下来我们看下元数据类型和非元数据类型的真正意义：

*Primitive* 数据类型是不可变（不可修改）的。创建原始数据类型后，我们将无法修改

**Example:**

```js
let word = 'JavaScript'
```

任何在单引号，双引号或者反引号的数据都是字符串。如果我们想要修改存储在*word*变量的字符串，JavaScript将会抛出异常，


```js
word[0] = 'Y'
```

上面的表达式将不会修改*word*变量中的字符串，因此我们可以认为strings是不可以修改的。元类型数据是通过它的值来比较大小的。借下来我们看下元数据比较大小
的例子：


```js
let numOne = 3
let numTwo = 3

console.log(numOne == numTwo)      // true

let js = 'JavaScript'
let py = 'Python'

console.log(js == py)             //false 

let lightOn = true
let lightOff = false

console.log(lightOn == lightOff) // false
```

### 非元数据类型

*非元数据类型* 是可修改或可变的。我们可以在非元数据类型创建后对它进行修改。让我们通过创建一个数组来看下这个特性。数组是一个方括号包裹的一个数值列表。数组可以包含相同或者不同的数据类型。数组通过它的index来获得对象。在JavaScript中数组的序号从0开始。比如数组的第一个元素index为0，第二个元素index元素为1，第三个元素index为2.


```js
let nums = [1, 2, 3]
nums[0] = 10

console.log(nums)  // [10, 2, 3]
```

正如下面所示，非元类型数据是可修改的，非元类型数据类型不能通过值的比较来比较大小。即使两个非元类型数据类型有相同的属性和值。他们也并非完全相等。


```js
let nums = [1, 2, 3]
let numbers = [1, 2, 3]

console.log(nums == numbers)  // false

let userOne = {
name:'Asabeneh',
role:'teaching',
country:'Finland'
}

let userTwo = {
name:'Asabeneh',
role:'teaching',
country:'Finland'
}

console.log(userOne == userTwo) // false
```
一般而言，我们不直接比较数组，方法，或者对象这些非元类型数据，非元类型数据又称为引用类型，因为它们通过引用而不是值进行比较。只有在两个对象指向同一个对象的时候，这两个非元类型才完全相等。

```js
let nums = [1, 2, 3]
let numbers = nums

console.log(nums == numbers)  // true

let userOne = {
name:'Asabeneh',
role:'teaching',
country:'Finland'
}

let userTwo = userOne

console.log(userOne == userTwo)  // true
```

如果你还难以理解元类型和非元类型，不要气馁你不是唯一有这种感觉的人。继续往下看，在后面再返回来看。接下来我们来看number数据类型。

## Numbers

Numbers 是可以用于进行算术运算的整形数值，我们来看下一些Numbers的例子：

### 声明number数据类型：

```js
let age = 35
const gravity = 9.81  //we use const for non-changing values, gravitational constant in  m/s2
let mass = 72         // mass in Kilogram
const PI = 3.14       // pi a geometrical constant

//More Examples
const boilingPoint = 100 // temperature in oC, boiling point of water which is a constant
const bodyTemp = 37      // oC average human body temperature, which is a constant

console.log(age, gravity, mass, PI, boilingPoint, bodyTemp)
```

### Math 对象

JavaScript中的Math对象提供了许多作用于numbers的方法。

```js

// 圆周率常量 PI 
const PI = Math.PI 
console.log(PI)                           // 3.141592653589793

// 四舍五入方法: round
// if above .5 up if less 0.5 down rounding
console.log(Math.round(PI))               // 3 to round values to the nearest number
console.log(Math.round(9.81))             // 10

//向下舍去
console.log(Math.floor(PI))               // 3 rounding down
//向上取舍
console.log(Math.ceil(PI))                // 4 rounding up
//最小值
console.log(Math.min(-5, 3, 20, 4,5, 10)) // -5, returns the minimum value
//最大值
console.log(Math.max(-5, 3, 20, 4,5, 10)) // 20, returns the maximum value

//随机数
const randNum = Math.random() // creates random number between 0 to 0.999999
console.log(randNum)
// Let us  create random number between 0 to 10
const num = Math.floor(Math.random () * 11) // creates random number between 0 and 10
console.log(num)

//绝对值
console.log(Math.abs(-10))      //10

//开方
console.log(Math.sqrt(100))     // 10
console.log(Math.sqrt(2))      //1.4142135623730951

//平方
console.log(Math.pow(3, 2)) // 9


console.log(Math.E) // 2.718
// Logarithm
//Returns the natural logarithm of base E of x, Math.log(x)
console.log(Math.log(2))    // 0.6931471805599453
console.log(Math.log(10))   // 2.302585092994046

// 三角函数
Math.sin(0)
Math.sin(60)

Math.cos(0)
Math.cos(60)
```

#### 随机数生成器

JavaScript Math对象提供了random()方法用于生成0 到 0.999999999...的随机数。

```js
let randomNum = Math.random() // generates 0 to 0.999
```

现在让我们看下如何使用random()方法产生0 and 10的随机数

```js
let randomNum = Math.random()         // generates 0 to 0.999
let numBtnZeroAndTen = randomNum * 11

console.log(numBtnZeroAndTen)         // this gives: min 0 and max 10.99

let randomNumRoundToFloor = Math.floor(numBtnZeroAndTen)
console.log(randomNumRoundToFloor)    // this gives between 0 and 10
```

## 字符串

字符串在单引号或者双引号括起来的文本。为了声明一个字符串我们需要一个变量名。赋值操作符，一个用单引号双引号或者反引号括起来的数值。接下来我们来看下string的例子。

```js
let space = ' '           // an empty space string
let firstName = 'Asabeneh'
let lastName = 'Yetayeh'
let country = 'Finland'
let city = 'Helsinki'
let language = 'JavaScript'
let job = 'teacher'
```

### 字符串连接

连接两个或者两个以上的字符称为字符连接。

```js
// Declaring different variables of different data types
let space = ' '
let firstName = 'Asabeneh'
let lastName = 'Yetayeh'
let country = 'Finland'
let city = 'Helsinki'
let language = 'JavaScript'
let job = 'teacher'
```

```js
let fullName = firstName + space + lastName; // concatenation, merging two string together.
console.log(fullName);
```

```sh
Asabeneh Yetayeh
```

我们可以以不同方式连接字符串：

#### 使用加号连接

使用加号连接字符串是一种比较老的方法。这种方式繁琐且容易出错,我们需要知道如何以这种方式进行连接，但是我强烈建议以第二种方式来连接。


```js
// Declaring different variables of different data types
let space = ' '
let firstName = 'Asabeneh'
let lastName = 'Yetayeh'
let country = 'Finland'
let city = 'Helsinki'
let language = 'JavaScript'
let job = 'teacher'
let age = 250
let fullName = firstName + space + lastName

let personInfoOne = fullName + '. I am ' + age + '. I live in ' + country; // ES5

console.log(personInfoOne)
```

```sh
Asabeneh Yetayeh. I am 250. I live in Finland
```

#### 长字串

string可以是一个单字符串或者段落甚至一页字符。如果string的长度过长，不能在一行内显示下，这种情况我们可以通过在每行的结尾添加反斜杠来暗示string将会延续到下一行。

**Example:**

```js
const paragraph = "My name is Asabeneh Yetayeh. I live in Finland, Helsinki.\
I am a teacher and I love teaching. I teach HTML, CSS, JavaScript, React, Redux, \
Node.js, Python, Data Analysis and D3.js for anyone who is interested to learn. \
In the end of 2019, I was thinking to expand my teaching and to reach \
to global audience and I started a Python challenge from November 20 - December 19.\
It was one of the most rewarding and inspiring experience.\
Now, we are in 2020. I am enjoying preparing the 30DaysOfJavaScript challenge and \
I hope you are enjoying too."
console.log(paragraph)
```

#### 转义字符

JavaScript和其他的编程语言用 \ + 一些字符 表示转义字符。我们来看下下面比较常见的转义字符：


- \n: new line
- \t: Tab means(8 spaces)
- \\\\: Back slash
- \\': Single quote (')
- \\":Double quote (")
  
```js
console.log('I hope every one is enjoying the 30 Days Of JavaScript challenge.\nDo you ?') // line break
console.log('Days\tTopics\tExercises')
console.log('Day 1\t3\t5')
console.log('Day 2\t3\t5')
console.log('Day 3\t3\t5')
console.log('Day 4\t3\t5')
console.log('This is a back slash  symbol (\\)') // To write a back slash
console.log('In every programming language it starts with \"Hello, World!\"')
console.log("In every programming language it starts with \'Hello, World!\'")
console.log('The saying \'Seeing is Believing\' is\'t correct in 2020')
```

#### 模板字符串

要创建模板字符串，我们需要两个反引号。我们可以将数据作为表达式插入模板字符串中。要注入数据，我们用大括号（{}）加上$符号将表达式括起来。请参见下面的语法。

```js
//Syntax
`String literal text`
`String literal text ${expression}`
```

**Example: 1**

```js
console.log(`The sum of 2 and 3 is 5`)              // statically writing the data
let a = 2
let b = 3
console.log(`The sum of ${a} and ${b} is ${a + b}`) // injecting the data dynamically
```

**Example:2**

```js
let firstName = 'Asabeneh'
let lastName = 'Yetayeh'
let country = 'Finland'
let city = 'Helsinki'
let language = 'JavaScript'
let job = 'teacher'
let age = 250
let fullName = firstName + ' ' + lastName

let personInfoTwo = `I am ${fullName}. I am ${age}. I live in ${country}.` //ES6 - String interpolation method
let personInfoThree = `I am ${fullName}. I live in ${city}, ${country}. I am a ${job}. I teach ${language}.`
console.log(personInfoTwo)
console.log(personInfoThree)
```

```sh
I am Asabeneh Yetayeh. I am 250. I live in Finland.
I am Asabeneh Yetayeh. I live in Helsinki, Finland. I am a teacher. I teach JavaScript.
```

使用字符串模板或字符串插值方法，我们可以添加表达式，该表达式可以是值或某些运算（比较，算术运算，三进制运算）。

```js
let a = 2
let b = 3
console.log(`${a} is greater than ${b}: ${a > b}`)
```

```sh
2 is greater than 3: false
```

### String 方法

在JavaScript中一切皆对象，string是一个元数据类型。意味着一旦被创建它就不能被修改。string对象有许多方法可以供我们使用。

1. *length*: string 的 *length* 方法将会返回字符串的长度.

  **Example:**

   ```js
   let js = 'JavaScript'
   console.log(js.length)         // 10
   let firstName = 'Asabeneh'
   console.log(firstName.length)  // 8
   ```

2. *访问string的字符*: 我们可以使用字符在字符串中的索引值来访问一个字符。字符串中以0作为字符串的开始，length - 1 作为字符串结尾的索引。


  ![Accessing sting by index](../images/string_indexes.png)
  

```js
let string = 'JavaScript'
let firstLetter = string[0]

console.log(firstLetter)           // J

let secondLetter = string[1]       // a
let thirdLetter = string[2]
let lastLetter = string[9]

console.log(lastLetter)            // t

let lastIndex = string.length - 1

console.log(lastIndex)  // 9
console.log(string[lastIndex])    // t
```

1. *toUpperCase()*: 这个方法将字符串转换成大写

```js
let string = 'JavaScript'

console.log(string.toUpperCase())     // JAVASCRIPT

let firstName = 'Asabeneh'

console.log(firstName.toUpperCase())  // ASABENEH

let country = 'Finland'

console.log(country.toUpperCase())    // FINLAND
```

4. *toLowerCase()*: 这个方法可以将字符串转换成小写字符。

```js
let string = 'JavasCript'

console.log(string.toLowerCase())     // javascript

let firstName = 'Asabeneh'

console.log(firstName.toLowerCase())  // asabeneh

let country = 'Finland'

console.log(country.toLowerCase())   // finland
```

5. *substr()*: 这个方法有两个参数第一个参数为起始索引，第二个参数表示要截取的字符长度。

```js
let string = 'JavaScript'
console.log(string.substr(4,6))    // Script

let country = 'Finland'
console.log(country.substr(3, 4))   // land
```

6. *substring()*: 它包含两个参数，开始字符索引和结束字符索引。它不包括结束索引那个字符。


```js
let string = 'JavaScript'

console.log(string.substring(0,4))     // Java
console.log(string.substring(4,10))    // Script
console.log(string.substring(4))       // Script

let country = 'Finland'

console.log(country.substring(0, 3))   // Fin
console.log(country.substring(3, 7))   // land
console.log(country.substring(3))      // land
```

7. *split()*: 在指定的位置分割字符串

```js
let string = '30 Days Of JavaScript'

console.log(string.split())     // ["30 Days Of JavaScript"]
console.log(string.split(' '))  // ["30", "Days", "Of", "JavaScript"]

let firstName = 'Asabeneh'

console.log(firstName.split())    // ["Asabeneh"]
console.log(firstName.split(''))  // ["A", "s", "a", "b", "e", "n", "e", "h"]

let countries = 'Finland, Sweden, Norway, Denmark, and Iceland'

console.log(countries.split(','))  // ["Finland", " Sweden", " Norway", " Denmark", " and Iceland"]
console.log(countries.split(', ')) //  ["Finland", "Sweden", "Norway", "Denmark", "and Iceland"]
```

8. *trim()*: 移除字符串开始和结尾的空字符串。

```js
let string = '   30 Days Of JavaScript   '

console.log(string)     
console.log(string.trim(' '))

let firstName = ' Asabeneh '

console.log(firstName)
console.log(firstName.trim())
```

```sh
   30 Days Of JavasCript   
30 Days Of JavasCript
  Asabeneh 
Asabeneh
```

9. *includes()*: *includes()*返回一个bool值，但有包含某个字符串的时候将会返回true，在没有包含字符串的时候返回false。

```js
let string = '30 Days Of JavaScript'

console.log(string.includes('Days'))     // true
console.log(string.includes('days'))     // false
console.log(string.includes('Script'))   // true
console.log(string.includes('script'))   // false
console.log(string.includes('java'))     // false
console.log(string.includes('Java'))     // true

let country = 'Finland'

console.log(country.includes('fin'))     // false
console.log(country.includes('Fin'))     // true
console.log(country.includes('land'))    // true
console.log(country.includes('Land'))    // false
```

10. *replace()*: 使用旧字符串替换掉新字符串

```js
string.replace(oldsubstring, newsubstring)
```

```js
let string = '30 Days Of JavaScript'
console.log(string.replace('JavaScript', 'Python')) // 30 Days Of Python

let country = 'Finland'
console.log(country.replace('Fin', 'Noman'))       // Nomanland
```

11. *charAt()*: 传入index返回在指定index的值

```js
string.charAt(index)
```

```js
let string = '30 Days Of JavaScript'
console.log(string.charAt(0))        // 3

let lastIndex = string.length - 1
console.log(string.charAt(lastIndex)) // t
```

12. *charCodeAt()*: 传入index返回在指定index的ASCII编码

```js
string.charCodeAt(index)
```

```js
let string = '30 Days Of JavaScript'
console.log(string.charCodeAt(3))        // D ASCII number is 51

let lastIndex = string.length - 1
console.log(string.charCodeAt(lastIndex)) // t ASCII is 116

```

1.  *indexOf()*: 传入一个子字符串，如果字符串包含这个子字符串，那么将会返回字符串在string中的第一个位置。如果不存在将会返回-1

```js
string.indexOf(substring)
```

```js
let string = '30 Days Of JavaScript'

console.log(string.indexOf('D'))          // 3
console.log(string.indexOf('Days'))       // 3
console.log(string.indexOf('days'))       // -1
console.log(string.indexOf('a'))          // 4
console.log(string.indexOf('JavaScript')) // 11
console.log(string.indexOf('Script'))     //15
console.log(string.indexOf('script'))     // -1
```

1.  *lastIndexOf()*: 传入一个子字符串，如果这个子字符串在string中，将会返回substring在string中的最后index。如果不存在则返回 -1

```js
//syntax
string.lastIndexOf(substring)
```

```js
let string = 'I love JavaScript. If you do not love JavaScript what else can you love.'

console.log(string.lastIndexOf('love'))       // 67
console.log(string.lastIndexOf('you'))        // 63
console.log(string.lastIndexOf('JavaScript')) // 38
```

15. *concat()*: 它可以传入多个子字符串，并将这些字符串拼接起来。


```js
string.concat(substring, substring, substring)
```

```js
let string = '30'
console.log(string.concat("Days", "Of", "JavaScript")) // 30DaysOfJavaScript

let country = 'Fin'
console.log(country.concat("land")) // Finland
```

16. *startsWith*: 判断某个字符串是否以某个子字符串开始

```js
//syntax
string.startsWith(substring)
```

```js
let string = 'Love is the best to in this world'

console.log(string.startsWith('Love'))   // true
console.log(string.startsWith('love'))   // false
console.log(string.startsWith('world'))  // false

let country = 'Finland'

console.log(country.startsWith('Fin'))   // true
console.log(country.startsWith('fin'))   // false
console.log(country.startsWith('land'))  //  false
```

17. *endsWith*: 判断一个字符串是否以某个字符串结尾

```js
string.endsWith(substring)
```

```js
let string = 'Love is the best to in this world'

console.log(string.endsWith('world'))         // true
console.log(string.endsWith('love'))          // false
console.log(string.endsWith('in this world')) // true

let country = 'Finland'

console.log(country.endsWith('land'))         // true
console.log(country.endsWith('fin'))          // false
console.log(country.endsWith('Fin'))          //  false
```

18. *search*: 传入一个参数，返回第一次出现的index

```js
string.search(substring)
```

```js
let string = 'I love JavaScript. If you do not love JavaScript what else can you love.'
console.log(string.search('love')) // 2
```

19. *match*: 它传入一个子字符串或者一个正则表达式作为一个参数，如果有匹配的则结果将会将这些结果放置在数组中返回。如果没匹配的则返回null。我们看下正则表达式长啥样。正则表达式以/开始并以/结束。

```js
let string = 'love'
let patternOne = /love/     // with out any flag
let patternTwo = /love/gi   // g-means to search in the whole text, i - case insensitive
```

匹配语法

```js
// syntax
string.match(substring)
```

```js
let string = 'I love JavaScript. If you do not love JavaScript what else can you love.'
console.log(string.match('love'))
```

```sh
["love", index: 2, input: "I love JavaScript. If you do not love JavaScript what else can you love.", groups: undefined]
```

```js
let pattern = /love/gi
console.log(string.match(pattern))   // ["love", "love", "love"]
```
让我们使用正则表达式从文本中提取数字。这不是介绍正则表达式的章节所以不用担心，我们将在其他部分介绍正则表达式。

```js
let txt = 'In 2019, I run 30 Days of Python. Now, in 2020 I super exited to start this challenge'
let regEx = /\d+/

// d with escape character means d not a normal d instead acts a digit
// + means one or more digit numbers,
// if there is g after that it means global, search everywhere.

console.log(txt.match(regEx))  // ["2", "0", "1", "9", "3", "0", "2", "0", "2", "0"]
console.log(txt.match(/\d+/g)) // ["2019", "30", "2020"]
```

20.   *repeat()*: 它需要传入一个整形参数，返回string字符串的重复数据。

```js
string.repeat(n)
```

```js
let string = 'love'
console.log(string.repeat(10)) // lovelovelovelovelovelovelovelovelovelove
```

## 检查数据类型和转换数据类型

### 检查数据类型

- 检查数据类型: 要检查某个数据的数据类型，我们可以使用_typeof_。我们也可以将一个数据类型转换为另一个数据类型。

  **Example:**

```js
// Different javascript data types
// Let's declare different data types

let firstName = 'Asabeneh'      // string
let lastName = 'Yetayeh'        // string
let country = 'Finland'         // string
let city = 'Helsinki'           // string
let age = 250                   // number, it is not my real age, do not worry about it
let job                         // undefined, because a value was not assigned

console.log(typeof 'Asabeneh')  // string
console.log(typeof firstName)   // string
console.log(typeof 10)          // number
console.log(typeof 3.14)        // number
console.log(typeof true)        // boolean
console.log(typeof false)       // boolean
console.log(typeof NaN)         // number
console.log(typeof job)         // undefined
console.log(typeof undefined)   // undefined
console.log(typeof null)        // object
```

### 转换数据类型

-  我们使用 _parseInt()_, _parseFloat()_,_Number()_, _+ sign_, _str()_ 来将某个数据转换为另一个数据类型。

#### 字符串转换为Int

我们可以使用下面几种方法将字符串数据转换为整形：

- parseInt()
- Number()
- Plus sign(+)

```js
let num = '10'
let numInt = parseInt(num)
console.log(numInt) // 10
```

```js
let num = '10'
let numInt = Number(num)

console.log(numInt) // 10
```

```js
let num = '10'
let numInt = +num

console.log(numInt) // 10
```

#### String 转换为 Float

我可以使用如下方式将String转换为Float：

- parseFloat()
- Number()
- Plus sign(+)

```js
let num = '9.81'
let numFloat = parseFloat(num)

console.log(numFloat) // 9.81
```

```js
let num = '9.81'
let numFloat = Number(num)

console.log(numFloat) // 9.81
```

```js
let num = '9.81'
let numFloat = +num

console.log(numInt) // 9.81
```

#### Float 转换为 Int

我们可以使用如下方式来将Float 转换为 Int

- parseInt()
  
```js
let num = 9.81
let numInt = parseInt(num)

console.log(numInt) // 9
```

🌕  你很厉害！你已经完成了第二天的挑战，现在我们来动手做些练习：


## 💻 Day 2: Exercises

### Exercise: Level 1

1. 声明一个变量名为challenge的变量，将**'30 Days Of JavaScript'**作为值赋值给它。
2. 使用 __console.log()__ 将string输出到浏览器终端
3. 使用 _console.log()_ 输出字符串的长度  __length__ 
4. 使用 __toUpperCase()__ 将某个字符串的所有字符转换为大写字符
5. 使用 __toLowerCase()__ 将某个字符串的所有字符转换为小写字符
6. 使用 __substr()__ 或者 __substring()__ 来截取字符的第一个word
7. 从*30 Days Of JavaScript*中截取 *Days Of JavaScript*
8. 使用 __includes()__ 方法判断某个字符串是否包含 __Script__ 这个词
9. 将某个字符串使用__split()__ 方法分割成数组
10. 使用 __split()__ 方法将 _30 Days Of JavaScript_ 这个字符串以空格作为分隔符进行分割。
11. 使用  __split__ 方法将 'Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon'以逗号作为分割符，将它转换为数组
12. 使用 __replace()__ 方法将 30 Days Of JavaScript 转换为 30 Days Of Python。
13. 通过 __charAt()__ 来查看'30 Days Of JavaScript'字符串的第15个字符。
14. 使用 __charCodeAt()__ 方法获得'30 Days Of JavaScript'字符串中的  J 的字符编码。
15. 使用 __indexOf__ 方法确定 30 Days Of JavaScript 字符串中第一个 a 字符的位置。
16. 使用 __lastIndexOf__ 方法确定 30 Days Of JavaScript 字符串中最后一个 a 字符的位置。
17. 使用 __indexOf__ 来查找 __'You cannot end a sentence with because because because is a conjunction'__ 这个句子中出现的第一个 __because__ 词的位置。

18. 使用 __lastIndexOf__ 来查找 __'You cannot end a sentence with because because because is a conjunction'__ 这个句子中出现的最后一个__because__ 词的位置。

19. 使用 __search__ 来查找 __'You cannot end a sentence with because because because is a conjunction'__ 这个句子中出现的第一个 __because__ 词的位置。
20. 使用 __trim()__ 来移除这个字符串中前后出现的空字符' 30 Days Of JavaScript '.

21. 使用 __startsWith()__ 方法作用于字符串 * 30 Days Of JavaScript * 使结果为true
22. 使用 __endsWith()__ 方法作用于字符串* 30 Days Of JavaScript *使结果为true
23. 使用 __match()__ 方法找出 30 Days Of JavaScript 字符中的所有 a 字符
24. 使用 __concat()__ 将 '30 Days of' 和 'JavaScript' 拼接为单个字符 - '30 Days Of JavaScript'
25. 使用 __repeat()__ 输出连续的两个 30 Days Of JavaScript

### Exercise: Level 2

1. Using console.log() print out the following statement.

    ```sh
    The quote 'There is no exercise better for the heart than reaching down and lifting people up.' by John Holmes teaches us to help one another.
    ```

1. Using console.log() print out the following quote by Mother Teresa.

    ```sh
    "Love is not patronizing and charity isn't about pity, it is about love. Charity and love are the same -- with charity you give love, so don't just give money but reach out your hand instead."
    ```

1. Check if typeof '10' is exactly equal to 10. If not make it exactly equal.
1. Check if parseFloat('9.8') is equal to 10 if not make it exactly equal with 10.
2. Check if 'on' is found in both python and jargon
3. _I hope this course is not full of jargon_. Check if _jargon_ is in the sentence.
4. Generate a random number between 0 and 100 inclusive.
5. Generate a random number between 50 and 100 inclusive.
6. Generate a random number between 0 and 255 inclusive.
7. Access the 'JavaScript' string characters using a random number.
8. Use console.log() and escape characters to print the following pattern.

    ```js
    1 1 1 1 1
    2 1 2 4 8
    3 1 3 9 27
    4 1 4 16 64
    5 1 5 25 125
    ```

9.  Use __substr__ to slice out the phrase __because because because__ in the following sentence:__'You cannot end a sentence with because because because is a conjunction'__

### Exercises: Level 3

1. 'Love is the best thing in this world. Some found their love and some are still looking for their love.' Count the number of word love in this sentence.
2. Use __match()__ to count the number all because's in the following sentence:__'You cannot end a sentence with because because because is a conjunction'__
3. Clean the following text and find the most frequent word (hint, use replace and regular express).

    ```js
        const sentence = '%I $am@% a %tea@cher%, &and& I lo%#ve %te@a@ching%;. The@re $is no@th@ing; &as& mo@re rewarding as educa@ting &and& @emp%o@weri@ng peo@ple. ;I found tea@ching m%o@re interesting tha@n any ot#her %jo@bs. %Do@es thi%s mo@tiv#ate yo@u to be a tea@cher!? %Th#is 30#Days&OfJavaScript &is al@so $the $resu@lt of &love& of tea&ching'
    ```

4. Calculate the total annual income of the person by extract the numbers from the following text. 'He earns 5000 euro from salary per month, 10000 euro annual bonus, 15000 euro online courses per month.'

🎉 CONGRATULATIONS ! 🎉

[<< Day 1](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/readMe.md) | [Day 3 >>](https://github.com/Asabeneh/30DaysOfJavaScript/blob/master/03_Day/03_booleans_operators_date.md)
