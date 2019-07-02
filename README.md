# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)
```swift
var number = ""
for i in 1...10 {
   let conv = String(i)
   number += conv
}
   print(number)
```
***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.
```swift
//var number = ""
//for i in 5...51 {
//
//    if i%2==0{
//    let conv = String(i)
//    number += conv + " "
//        }   }
//    print(number)
```
***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.
```swift
//var number = ""
//for i in 1...60 {
//
//    if i%10==4{
//    let conv = String(i)
//    number += conv + " "
//        }   }
//    print(number)
```
***
## Question 4

Print each character in the string `"Hello world!"`
```swift
//var word = "Hello world!"
//for character in word{
//    print(character)
//}
```
***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).
```swift
//var myString = "Hello world!"
//let myStringEnd = myString.endIndex
//let lastCharIndex = myString.index(before: myStringEnd)
//let lastChar = myString[lastCharIndex]
//print(lastChar)
```
***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.
``` swift
//var myString = "Hello world!111"
var i = 0
if myString.count % 2 != 0 {
for char in myString {
if i % 2 == 0{
print(char)
}
i+=1
}
} else {
print(myString)
}
```

***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.
```swift 
var notAChar:String = "c"
var charIs = Character(notAChar)
print(charIs)

```
***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.
``` swift
var aAcute = "\u{0061}\u{0301}"
var bAcute = "á"
aAcute == bAcute

var some = "\u{D55C}"
var another = "한"
some == another

var A = "\u{0041}"
var a = "A"
a == A

var B = "\u{004F}"
var b = "O"
B==b

var z = "\u{0053}"
var Z = "S"
z==Z

```
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`
print("\u{0048}\u{0045}\u{004C}\u{004C}\u{004F}\u{0020}\u{0057}\u{004F}\u{0052}\u{004C}\u{0044}\u{0021}")
***
## Question 10

**Using only Unicode**, print out your name.
print("\u{0041}\u{006C}\u{0062}\u{0065}\u{0072}\u{0074}")
***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.
```swift
print("\u{006F}\u{0069}\u{0020}\u{004D}\u{0075}\u{006E}\u{0064}\u{006F}")
***
```
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -

let rows = String(repeating: "  - ", count: 10)
print(rows)
for _ in 1...4{
let lols = String(repeating: "| \u{2698} ", count:10) + "|"
print(lols)
}
let dows = String(repeating: "  - ", count: 10)
print(dows)



```

***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜

print("\u{2656}\u{2658}\u{2657}\u{265B}\u{2655}\u{2654}\u{2657}\u{2658}\u{2656}")
print("\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}")
for _ in 1...2{
print("")
}
print("\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}")
print("\u{265C}\u{265E}\u{265D}\u{265B}\u{265C}\u{9821}\u{265D}\u{265E}\u{265C}")

```
***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with *"
let replacedString = aString.replacingOccurrences(of: "e", with: "*")
print(replacedString)

// Your code here
 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "Hello"`

// Your code here
var aString = "Hello"
var reverse = String(aString.reversed())
print(reverse)

```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"

// Your code here


let aString = "anutforajaroftuna"
var reverse = String(aString.reversed())
print(reverse)
if aString == reverse{
print(true)
}
else {
print(false)

}

```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
var problem = "split this string into words and print them on separate lines"
var solved = problem.components(separatedBy: " ")
print(solved)
```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```

***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

// Your code here
var problem = "find the longest word in the problem description"
var word = ""
var longest = ""
var array = [String] ()
for a in problem{
if a == " "{
array.append(word)
word = ""
continue
}
word += String(a)
}
array.append(word)
//print(array)
for a in array{
if longest.count <= a.count {
longest = a
}
}
print(longest)




```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"

var storev = 0
var storec = 0
for a in input.lowercased(){
for b in vowels {
if a == b {
storev += 1
}
}
for c in consonants {
if a == c{
storec += 1
}
}
}

var vowelsConsonants = (storev, storec)
print(vowelsConsonants)

```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`
```swift
var problem = "How are you doing this Monday? "
var word = ""
if problem == ""{
print("No last word")
} else {
for a in problem{
if a == " "{
word = ""
continue
}
word += String(a)
}
}
print(word.count)

```
***
