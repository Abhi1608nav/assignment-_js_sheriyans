# JavaScript Practice Problems

This repository contains a collection of beginner-friendly JavaScript problems to practice basic programming concepts.

## Table of Contents
1. [Age Category Message](#age-category-message)
2. [Even or Odd Sum](#even-or-odd-sum)
3. [Character Case Checker](#character-case-checker)
4. [Largest of Three Numbers](#largest-of-three-numbers)
5. [Leap Year Checker](#leap-year-checker)
6. [Simple Calculator](#simple-calculator)
7. [Positive, Negative, or Zero](#positive-negative-or-zero)
8. [User Greeting](#user-greeting)
9. [Traffic Light System](#traffic-light-system)
10. [Multiplication Table](#multiplication-table)
11. [Grade Calculator](#grade-calculator)
12. [Simple Login System](#simple-login-system)
13. [Swapping Without Third Variable](#swapping-without-third-variable)
14. [FizzBuzz](#fizzbuzz)
15. [Number Reversal](#number-reversal)
16. [Sum of Digits](#sum-of-digits)
17. [Palindrome Checker](#palindrome-checker)
18. [Reverse Without String Methods](#reverse-without-string-methods)
19. [Find Second Largest](#find-second-largest)
20. [Find First Non-Repeating Character](#find-first-non-repeating-character)
21. [Even Digit Counter](#even-digit-counter)
22. [Nested Condition Challenge](#nested-condition-challenge)
23. [Toggle Case](#toggle-case)
24. [Find the Missing Number in a Sequence](#find-the-missing-number-in-a-sequence)
25. [Convert Number to Words](#convert-number-to-words)

---

---

## Problems and Solutions

### 1. Age Category Message
**Description:** Ask the user for their age and classify them into categories:
- Under 18 → Minor
- 18-60 → Adult
- Above 60 → Senior Citizen

**Solution:**
```javascript
let age = Number(prompt("Enter your age"));
if (age < 18) {
    console.log('You are a minor');
} else if (age >= 18 && age < 60) {
    console.log("You are an adult");
} else {
    console.log("You are a senior citizen");
}
```

### 2. Even or Odd Sum
**Description:** Take two numbers as input and check if their sum is even or odd.

**Solution:**
```javascript
let num1 = Number(prompt("Enter first number"));
let num2 = Number(prompt("Enter second number"));
let sum = num1 + num2;
console.log(sum % 2 === 0 ? "Even Sum" : "Odd Sum");
```

### 3. Character Case Checker
**Description:** Ask the user for a character and check if it is uppercase or lowercase.

**Solution:**
```javascript
let char = prompt("Enter a character");
if (char >= 'A' && char <= 'Z') {
    console.log("Uppercase");
} else if (char >= 'a' && char <= 'z') {
    console.log("Lowercase");
} else {
    console.log("Not an alphabet character");
}
```

### 4. Largest of Three Numbers
**Description:** Take three numbers as input and find the largest among them.

**Solution:**
```javascript
let a = Number(prompt("Enter first number"));
let b = Number(prompt("Enter second number"));
let c = Number(prompt("Enter third number"));
console.log(Math.max(a, b, c) + " is the largest number");
```

### 5. Leap Year Checker
**Description:** Check if a given year is a leap year.

**Solution:**
```javascript
let year = Number(prompt("Enter a year"));
if ((year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0)) {
    console.log("Leap Year");
} else {
    console.log("Not a Leap Year");
}
```

### 6. Simple Calculator
**Description:** Perform basic arithmetic operations based on user input.

**Solution:**
```javascript
let num1 = Number(prompt("Enter first number"));
let operator = prompt("Enter operator (+, -, *, /)");
let num2 = Number(prompt("Enter second number"));
let result;
switch (operator) {
    case '+': result = num1 + num2; break;
    case '-': result = num1 - num2; break;
    case '*': result = num1 * num2; break;
    case '/': result = num2 !== 0 ? num1 / num2 : "Cannot divide by zero"; break;
    default: result = "Invalid operator";
}
console.log("Result: " + result);
```

### 7. Positive, Negative, or Zero
**Description:** Check if a number is positive, negative, or zero.

**Solution:**
```javascript
let num = Number(prompt("Enter a number"));
if (num > 0) {
    console.log("Positive");
} else if (num < 0) {
    console.log("Negative");
} else {
    console.log("Zero");
}
```

### 8. User Greeting
**Description:** Greet the user based on their name.

**Solution:**
```javascript
let name = prompt("Enter your name");
console.log("Hello, " + name + "!");
```

### 9. Traffic Light System
**Description:** Simulate a traffic light system with three colors: Red, Yellow, Green.

**Solution:**
```javascript
let color = prompt("Enter traffic light color").toLowerCase();
switch (color) {
    case 'red': console.log("Stop"); break;
    case 'yellow': console.log("Ready"); break;
    case 'green': console.log("Go"); break;
    default: console.log("Invalid color");
}
```

### 10. Multiplication Table
**Description:** Print the multiplication table of a given number.

**Solution:**
```javascript
let num = Number(prompt("Enter a number"));
for (let i = 1; i <= 10; i++) {
    console.log(`${num} x ${i} = ${num * i}`);
}
```

### 11. Grade Calculator
**Description:** Take marks as input and assign a grade based on standard grading criteria.

**Solution:**
```javascript
let marks = Number(prompt("Enter your marks"));
if (marks >= 90) {
    console.log("Grade: A");
} else if (marks >= 80) {
    console.log("Grade: B");
} else if (marks >= 70) {
    console.log("Grade: C");
} else if (marks >= 60) {
    console.log("Grade: D");
} else {
    console.log("Fail");
}
```

---


### 12. Simple Login System
**Description:** Create a simple login system that checks if the entered username and password match predefined values.

**Code Snippet:**
```javascript
const username = "user";
const password = "pass123";

let inputUsername = prompt("Enter username:");
let inputPassword = prompt("Enter password:");

if (inputUsername === username && inputPassword === password) {
    console.log("Login successful");
} else {
    console.log("Invalid credentials");
}
```

---

### 13. Swapping Without Third Variable
**Description:** Swap two numbers without using a third variable.

**Code Snippet:**
```javascript
let a = 5, b = 10;

a = a + b;
b = a - b;
a = a - b;

console.log(`After swapping: a = ${a}, b = ${b}`);
```

---

### 14. FizzBuzz
**Description:** Print numbers from 1 to 100.  
- If divisible by 3, print "Fizz".  
- If divisible by 5, print "Buzz".  
- If divisible by both 3 and 5, print "FizzBuzz".  

**Code Snippet:**
```javascript
for (let i = 1; i <= 100; i++) {
    if (i % 3 === 0 && i % 5 === 0) {
        console.log("FizzBuzz");
    } else if (i % 3 === 0) {
        console.log("Fizz");
    } else if (i % 5 === 0) {
        console.log("Buzz");
    } else {
        console.log(i);
    }
}
```

---

### 15. Number Reversal
**Description:** Reverse a given number.

**Code Snippet:**
```javascript
let word = prompt("Enter a number");
let reverseWord = '';
for(let i = word.length - 1; i>=0 ;i--) {
    reverseWord +=word[i];
}
console.log(word, reverseWord);
```

---

### 16. Sum of Digits
**Description:** Find the sum of the digits of a given number.

**Code Snippet:**
```javascript
function sumOfDigits(num) {
    return num.toString().split('').reduce((acc, digit) => acc + parseInt(digit), 0);
}
console.log(sumOfDigits(1234));
```

---

### 17. Palindrome Checker
**Description:** Check if a given string is a palindrome.

**Code Snippet:**
```javascript
function isPalindrome(str) {
    let reversed = str.split('').reverse().join('');
    return str === reversed;
}
console.log(isPalindrome("racecar")); // true
console.log(isPalindrome("hello"));   // false
```

---

### 18. Reverse Without String Methods
```javascript
let word = prompt("Enter a number");
let reverseWord = '';
for(let i = word.length - 1; i>=0 ;i--) {
    reverseWord +=word[i];
}
console.log(word, reverseWord);
```

### 19. Find Second Largest
```javascript
let num1 = Number(prompt("Enter first number"));
let num2 = Number(prompt("Enter second number"));
let num3 = Number(prompt("Enter third number"));

if(num1>num2 && num2>num3) {
    console.log("The second largest number is ", num2);
} else if(num2>num3) {
    console.log("The second largest number is ", num1 > num3 ? num1 : num3);
} else {
    console.log("The second largest number is ", num2 > num1 ? num2 : num1);
}
```

### 20. Find First Non-Repeating Character
```javascript
let word = prompt("Enter a word");
let charMap = new Map();
for(let i = 0; i < word.length; i++) {
    charMap.set(word[i], (charMap.get(word[i]) || 0) + 1);
}
for(let i = 0; i < word.length; i++) {
    if(charMap.get(word[i]) === 1) {
        console.log("The first non-repeating character in word is ", word[i]);
        break;
    }
}
```

### 21. Even Digit Counter
```javascript
let number = Number(prompt('Enter a number'));
let evenDigitCounter = 0;
while(number>0) {
    let rem = number % 10;
    number = Math.floor(number / 10);
    if(rem % 2 === 0) evenDigitCounter++;
}
console.log(`Number of even digit count: `, evenDigitCounter);
```
## 22. Nested Condition Challenge
**Description:** Write a program that categorizes a number based on multiple conditions.

**Code Snippet:**
```javascript
let num = Number(prompt("Enter a number"));
if (num > 0) {
    if (num % 2 === 0) {
        console.log("Positive Even Number");
    } else {
        console.log("Positive Odd Number");
    }
} else if (num < 0) {
    console.log("Negative Number");
} else {
    console.log("Zero");
}
```

---

## 23. Toggle Case
**Description:** Convert uppercase letters to lowercase and vice versa in a given string.

**Code Snippet:**
```javascript
function toggleCase(str) {
    return str.split('').map(char =>
        char === char.toUpperCase() ? char.toLowerCase() : char.toUpperCase()
    ).join('');
}
console.log(toggleCase("Hello World"));
```

---

## 24. Find the Missing Number in a Sequence
**Description:** Given an array containing numbers from 1 to n with one missing, find the missing number.

**Code Snippet:**
```javascript
function findMissingNumber(arr, n) {
    let expectedSum = (n * (n + 1)) / 2;
    let actualSum = arr.reduce((sum, num) => sum + num, 0);
    return expectedSum - actualSum;
}
console.log(findMissingNumber([1, 2, 4, 5, 6], 6));
```

---

## 25. Convert Number to Words
**Description:** Convert a given number into words (e.g., 123 → "One Hundred Twenty-Three").

**Code Snippet:**
```javascript
function numberToWords(num) {
    let words = ["Zero", "One", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine"];
    return num.toString().split('').map(digit => words[digit]).join(' ');
}
console.log(numberToWords(123));
```
