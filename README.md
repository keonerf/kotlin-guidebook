<h1 id="my-title"> Kotlin Guidebook </h1>
This Kotlin guide provides a concise and efficient summary of most of the Kotlin syntax and know-hows of the language. This guide is a by product of the official <a href="https://kotlinlang.org/docs/home.html"> Kotlin Documentation</a> and does not aim to provide a tutorial for the language but only serve as an instant helpbook for programmers.

<br>Please let me know about any errors in this guide and feel free to help out in it's expansion.</br>

# Table of Contents
- [Introduction](#introduction)
  - [Hello world Kotlin program](#hello-world-kotlin-program)
  - [Input code](#input-code)
  - [Comments](#comments)
  - [Variables](#variables)
  - [Data types](#data-types)
  - [Type Inference](#type-inference)
  - [Type Conversion](#type-conversion)
  - [String templates](#string-templates)
  - [Character escape](#character-escape)
  - [Operators](#operators)
- [Control Flow](#control-flow)
  - [If-else](#if-else)
  - [When](#when)
  - [Conditional Expression](#conditional-expression)
  - [For loop](#for-loop)

- <a href="https://kotlinlang.org/docs/keyword-reference.html">Official kotlin Keywords and operators</a>

## Introduction <a name="introduction"></a>
Kotlin is a statically typed, general-purpose programming language developed by JetBrains, that has built world-class IDEs like IntelliJ IDEA, PhpStorm, Appcode, etc. It was first introduced by JetBrains in 2011 and a new language for the JVM. Kotlin is object-oriented language, and a “better language” than Java, but still be fully interoperable with Java code. Kotlin is sponsored by Google, announced as one of the official languages for Android Development in 2017 (Geeksforgeeks). It is well known amongst developers due to its features like lambda expressions, inline functions, null safety, coroutines and many others. This guide will cover these features amongst other key concepts.

### Hello world Kotlin program <a name="hello-world-kotlin-program"></a>
The most basic form of code, the "Hello world" program in Kotlin:
```kotlin
fun main() {
    println("Hello world")
}
```
### Input code <a name="input-code"></a>
The readLine function is used to gather input from the user:
```kotlin
fun main() {
    print("Enter your name: ")
    val name = readLine()
    println("Hello, $name!")
}
```
### Comments<a name="comments"></a>
```kotlin
// End-of-line comment

/* Block comment
   across multiple lines. */
```
Block comments in Kotlin can also be nested.
```kotlin
/* The comment starts here
/* but contains a nested comment here *⁠/
and ends here. */
```
### Variables <a name="variables"></a>
The var and val keywords are used to declare variables. The difference between these two is the factor of mutability which means whether or not the declared variable can be manipulated further down the code. 
var variables are mutable, and thus their values can be changed after they are initialized. val variables on the other hand are immutable meaning their value cannot be changed after they are initialized. 
```kotlin
var x = 5
x = 10
```
```kotlin
val y = 5
y = 10 // This will result in a compilation error
```
### Data types <a name="data-types"></a>
The following code contains some of the most important data types of the language:
```kotlin
    val booleanVar: Boolean = true
    val byteVar: Byte = 127
    val shortVar: Short = 32767
    val intVar: Int = 2147483647
    val longVar: Long = 9223372036854775807L
    val floatVar: Float = 3.14f
    val doubleVar: Double = 3.14159265358979323846
    val charVar: Char = 'A'
    val stringVar: String = "Hello, world!"
```
### Type Inference <a name="type-inference"></a>
Kotlin has the native capability of interpreting the data type of a declared variable. Note that this interpretation only works when the variable has been initialised that is a value has been alloted to it. If we declare a variable without an initial value then we must make sure to specify it's data type.
```kotlin
val a = 1 // data type = int
val b = "name" // data type = string
```
```kotlin
var z: Double // Valid, z has no initial value
// println(z) // Invalid, z is not initialized and has no value yet
z = 3.14 // Valid, z is initialized with a value
```
### Type Conversion <a name="type-conversion"></a>
Kotlin provides several methods for converting between data types. Here's an example in Kotlin that demonstrates various methods of type conversion.
```kotlin
    val str: String = "123"
    val num: Int = str.toInt() // Convert String to Int

    val dbl: Double = 123.45
    val int: Int = dbl.toInt() // Convert Double to Int

    val lng: Long = 9876543210
    val flt: Float = lng.toFloat() // Convert Long to Float

    val bol: Boolean = true
    val strBol: String = bol.toString() // Convert Boolean to String

    val char: Char = 'A'
    val intChar: Int = char.toInt() // Convert Char to Int // Conversion of Char to Number is deprecated. Use Char.code property instead.

    val byte: Byte = 127
    val short: Short = byte.toShort() // Convert Byte to Short
```
### String templates <a name="string-templates"></a>
The '$' operator is used to recall a variable.
```kotlin
val name= "Ali"
val result= "My name is $name" 
```
### Character escape <a name="character-escape"></a>
Special characters start from an escaping backslash \. The following escape sequences are supported:
```kotlin
    \t – insert tab
    \b – backspace
    \n – new line (LF)
    \r – carriage return (CR)
    \' – single quotation mark
    \" – double quotation mark
    \\ – backslash
    \$ – dollar sign
```
### Operators <a name="operators"></a>
Arithmetic operators:
```kotlin
  val a = 10
  val b = 5
  println(a + b) // 15
  println(a - b) // 5
  println(a * b) // 50
  println(a / b) // 2
  println(a % b) // 0
 ```
 Comparison operators:
```kotlin
  val c = 10
  val d = 5
  println(c > d) // true
  println(c >= d) // true
  println(c < d) // false
  println(c <= d) // false
  println(c == d) // false
  println(c != d) // true
 ```
Assignment operators:
 ```kotlin
  var h = 10
  h += 5
  println(h) // 15
  h -= 5
  println(h) // 10
  h *= 2
  println(h) // 20
  h /= 4
  println(h) // 5
  h %= 3
  println(h) // 1
 ```
Logical operators:
```kotlin  
  val i = true
  val j = false
  println(i && j) // false
  println(i || j) // true
  println(!i) // false
 ```
Bitwise operators:
```kotlin
  val k = 0b1010
  val l = 0b1100
  println(k and l) // Prints "8" (0b1000)
  println(k or l) // Prints "14" (0b1110)
  println(k xor l) // Prints "6" (0b0110)
 ```
Range operator:
```kotlin
  val o = 1..10
  println(o.contains(5)) // Prints "true"
  println(o.contains(11)) // Prints "false"
```
## Control flow  <a name="control-flow"></a>
### If-else <a name="if-else"></a>
```kotlin
if (condition) {
    // Code to execute if condition is true
} else {
    // Code to execute if condition is false
}
```
### When <a name="when"></a>
```kotlin
when (value) {
    condition1 -> // Code to execute if value matches condition1
    condition2 -> // Code to execute if value matches condition2
    else -> // Code to execute if value does not match any condition
}
```
### Conditional Expression <a name="conditional-expression"></a>
Given if and when are expressions, we can directly assign them to variables.
```kotlin
val seasonFirstMonth = when(season) {
    "summer" -> 6,
    "winter" -> 12,
    "automn" -> 9,
    "spring" -> 3,
    else -> error("There is only 4 seasons")
}
```
Thus, it allows a similar ternary operator using a regular if.
```kotlin
val max = if (a > b) a else b         
```
### For loop <a name="for-loop"></a>
```kotlin
for (item in collection) {
    // Code to execute for each item in collection
}
```
