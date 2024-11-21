# Day 40 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 40** of my **100 Days of Code Challenge**! Today, I implemented a Java program to take input for an array and display its elements. This exercise helped me understand how to handle arrays and loops in Java.

## ✅ What I did today
- Wrote a Java program to input and display elements of an array.
- Practiced working with arrays and iterating through them using loops.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Loops, Input Handling

## 📖 Problem Description
- The task is to:
  1. Input the size of an array.
  2. Accept elements into the array.
  3. Display the array elements in the same order they were input.
  
For example:
  - Input: `3` (size of the array), `1 2 3` (elements)
  - Output: `1 2 3`

### Input/Output Example:
  - **Input**:
    ```
    Enter the number of elements you want to store: 3
    Enter the elements: 1 2 3
    ```
  - **Output**:
    ```
    Array of elements: 1 2 3
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;

public class pro_59 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        // Input the size of the array
        System.out.println("Enter the number of elements you want to store:");
        int num = input.nextInt();
        
        int[] array = new int[num];
        
        // Input the elements
        System.out.println("Enter the elements:");
        for (int i = 0; i < num; i++) {
            array[i] = input.nextInt();
        }
        
        // Display the elements
        System.out.println("Array of elements:");
        for (int i = 0; i < num; i++) {
            System.out.print(array[i] + " ");
        }
        
        input.close();
    }
}
🖥️ Program Output

Enter the number of elements you want to store:
3
Enter the elements:
1 2 3
Array of elements:
1 2 3
```
---
### 📚 Lessons Learned
Learned how to handle arrays in Java by using loops for input and output.
Improved understanding of managing array sizes dynamically based on user input.

---
### ⚡ Challenges
Ensuring the program handles valid input and does not exceed the allocated array size.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
