# Day 12 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 12** of my **100 Days of Code Challenge**! Today, I implemented a Java program to find the **sum of digits** of a given number. This problem helped me improve my understanding of **modulus operations** and **integer division** for manipulating individual digits of a number.

## ✅ What I did today
- Wrote a Java program to calculate the **sum of digits** of a number.
- Practiced using **loops**, **modulus** (`%`), and **integer division** (`/`) to extract and sum each digit.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Loops, Modulus Operator, Integer Division

## 🔗 Links to Code
- [Day 12 Code Repository](https://github.com/kiranreddy4433E/Day_12/blob/main/pro_24.java): This repository contains the code solution for finding the sum of digits of a number.

## 📖 Problem Description
- The task is to take an integer input and calculate the sum of its digits. This is done by repeatedly extracting the last digit of the number using the **modulus operator** (`%`) and reducing the number by dividing it by 10.
  
### Input/Output Example:
  - Input: `12345`
    - Output: `The sum of digits is 15`
  
  - Input: `987`
    - Output: `The sum of digits is 24`

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_24 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        // Input from user
        System.out.println("Enter a number: ");
        int num = input.nextInt();
        int sum = 0;
        
        // Calculate the sum of digits
        while (num != 0) {
            int digit = num % 10;  // Get the last digit
            sum += digit;  // Add digit to sum
            num /= 10;  // Remove the last digit from the number
        }
        
        // Output the result
        System.out.println("Sum of the digits: " + sum);
        
        input.close();
    }
}
```
---

### 🖥️ Program Output

Enter a number: 
12345
Sum of the digits: 15

Enter a number: 
987
Sum of the digits: 24

---

### 📚 Lessons Learned
Learned how to extract individual digits from a number using the modulus operator (%).
Practiced using integer division (/) to remove digits from a number one by one.
Reinforced my understanding of loops to iteratively calculate the sum of digits.

---

### ⚡ Challenges
The main challenge was handling negative numbers. This was solved by using the absolute value of the input, ensuring that the program works correctly regardless of sign.

---

### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---

100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms
