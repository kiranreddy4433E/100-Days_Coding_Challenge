# Day 14 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 14** of my **100 Days of Code Challenge**! Today, I implemented a Java program to **reverse a given number**. This problem allowed me to practice working with loops and basic arithmetic operations to manipulate digits.

## ✅ What I did today
- Wrote a Java program that reverses a given integer.
- Practiced extracting and manipulating individual digits in a number.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Modulus Operator, Integer Division

## 🔗 Links to Code
- [Day 14 Code Repository](#link-to-repository): This repository contains the code solution for reversing a given number.

## 📖 Problem Description
- The task is to take an integer as input and reverse its digits.
- For example:
  - Input: `1234`
    - Output: `4321`
  - Input: `-567`
    - Output: `-765`

### Input/Output Example:
  - Input: `12345`
    - Output: `54321`
  
  - Input: `-987`
    - Output: `-789`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_25 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Input number from the user
        System.out.print("Enter a number: ");
        int num = input.nextInt();
        int reverse = 0;

        // Calculate the reverse of the number
        while (num != 0) {
            reverse = 10 * reverse + num % 10;
            num /= 10;
        }

        // Output the reversed number
        System.out.println("Reversed Number: " + reverse);

        input.close();
    }
}
```
---

### 🖥️ Program Output

- Enter a number: 
- 12345
- Reversed Number: 54321

- Enter a number: 
- -987
- Reversed Number: -789

---

### 📚 Lessons Learned
Practiced using the modulus operator (%) to extract individual digits from a number.
Reinforced the use of integer division (/) to remove digits one at a time from a number.
Learned how to construct a number in reverse by manipulating the order of digits.

---

### ⚡ Challenges
Handling negative numbers correctly was important to ensure the negative sign is maintained when reversing the digits.

---

### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---

### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
