# Day 48 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 48** of my **100 Days of Code Challenge**! Today, I implemented a Java program to remove **duplicate elements** from an array. This task improved my understanding of arrays, sorting, and frequency counting using `HashMap`.

## ✅ What I did today
- Wrote a Java program to:
  1. Input an array of integers.
  2. Identify and remove duplicate elements from the array.
  3. Display only the unique elements.
- Practiced using `HashMap` for counting element occurrences.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** Arrays, HashMap, Loops, Sorting

## 📖 Problem Description
- The task is to:
  1. Input an array of integers from the user.
  2. Remove all duplicate elements from the array.
  3. Display only the unique elements.

For example:
  - Input: `Array: [1, 2, 2, 3, 4, 4, 5]`
  - Output:
    ```
    Unique elements: [1, 3, 5]
    ```

---

### Input/Output Example:

- **Input**:
Enter the number of elements in the array: 7 Enter the elements: 1 2 2 3 4 4 5

markdown
Copy code
- **Output**:
Array elements: 1 2 2 3 4 4 5 Non-repeating elements: 1 3 5

java
Copy code

---

## 📝 Code Example

```java
package dsa;

import java.util.Scanner;
import java.util.Arrays;
import java.util.HashMap;

public class pro_68 {

  public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      System.out.println("Enter the number of elements in the array: ");
      int num = input.nextInt();

      int[] arrays = new int[num];
      HashMap<Integer, Integer> frequencyMap = new HashMap<>();

      System.out.println("Enter the array elements:");
      for (int i = 0; i < num; i++) {
          arrays[i] = input.nextInt();
          frequencyMap.put(arrays[i], frequencyMap.getOrDefault(arrays[i], 0) + 1);
      }

      Arrays.sort(arrays);

      System.out.println("Array elements:");
      for (int i = 0; i < num; i++) {
          System.out.println(arrays[i]);
      }

      System.out.println("Non-repeating elements:");
      for (Integer key : frequencyMap.keySet()) {
          if (frequencyMap.get(key) == 1) {
              System.out.println(key);
          }
      }

      input.close();
  }
}
🖥️ Program Output
Example 1: With Duplicates

Enter the number of elements in the array: 
7
Enter the array elements: 
1 2 2 3 4 4 5
Array elements:
1
2
2
3
4
4
5
Non-repeating elements:
1
3
5
Example 2: No Duplicates

Enter the number of elements in the array: 
5
Enter the array elements: 
10 20 30 40 50
Array elements:
10
20
30
40
50
Non-repeating elements:
10
20
30
40
50
```
---
## 📚 Lessons Learned
Practiced using HashMap for frequency counting.
Learned how to remove duplicate elements from an array efficiently.

---
## ⚡ Challenges
Handling cases where all elements are duplicates or no duplicates exist.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
