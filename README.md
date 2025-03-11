<h1 id="my-title"> Kotlin Guidebook </h1>
This Kotlin guide provides a concise and efficient summary of most of the Kotlin syntax and know-hows of the language. This guide is a by product of the official <a href="https://kotlinlang.org/docs/home.html"> Kotlin Documentation</a> and does not aim to provide a tutorial for the language but only serve as an instant helpbook for programmers.

<br>Please let me know about any errors in this guide and feel free to help out in it's expansion.</br>

# Table of Contents
- [Introduction](#introduction)
  - [Hello world Kotlin program](#hello-world-kotlin-program)
  - [Input code](#input-code)
  - [Comments](#comments)

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
