# Day 31 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 31** of my **100 Days of Code Challenge**! Today, I implemented a Java program to find the **kth smallest number in an array** by sorting the array first. This exercise helped me improve my understanding of sorting algorithms and indexing.

## ✅ What I did today
- Created a Java program to identify the kth smallest number in a predefined array.
- Practiced sorting arrays and using indices to retrieve specific elements.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, Sorting, Indexing

## 📖 Problem Description
- The task is to identify the kth smallest number in an array by sorting it first and then accessing the kth element. For example:
  - Given array: `{123, 4, 33, 36, 7, 456, 2, 7, 6, 0}`
  - For `k = 3`, the 3rd smallest element is `4`.

### Input/Output Example:
  - **Input**:
    ```
    Enter a number between 1 - 10: 3
    ```
  - **Output**:
    ```
    Sorted Array: [0, 2, 4, 6, 7, 7, 33, 36, 123, 456]
    3rd Smallest number: 4
    ```

---

## 📝 Code Example

```java
package dsa;

import java.util.Arrays;
import java.util.Scanner;

public class pro_44 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a number between 1 - 10: ");
        
        int kth = input.nextInt();
        int[] arr = {123, 4, 33, 36, 7, 456, 2, 7, 6, 0};
        
        // Sort the array
        Arrays.sort(arr);
        System.out.println("Sorted Array: " + Arrays.toString(arr));
        
        // Print the kth smallest element
        System.out.println(kth + "th Smallest number: " + arr[kth - 1]);
        
        input.close();
    }
}

🖥️ Program Output

Enter a number between 1 - 10: 
3
Sorted Array: [0, 2, 4, 6, 7, 7, 33, 36, 123, 456]
3rd Smallest number: 4
```
---
### 📚 Lessons Learned
- Practiced array sorting with Arrays.sort() and accessing elements by index.
- Reinforced the process of finding specific elements in a sorted array.

---
### ⚡ Challenges
Ensuring the kth index was valid within the bounds of the array to avoid errors.

---
### 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: Chandra Kiran Reddy Reddycharla
- Twitter: @kiran4746

---
### 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
