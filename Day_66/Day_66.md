
# Day 66 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 66** of my **100 Days of Code Challenge**! Today, I implemented a Java program to check if it is possible to create a palindromic string by concatenating substrings from two given strings. This program uses substring extraction and palindrome validation to solve the problem.

## ✅ What I did today
- Wrote a Java program to:
  1. Accept multiple test cases.
  2. For each test case:
     - Input two strings `A` and `B`.
     - Extract substrings `s1` from `A` and `s2` from `B`.
     - Check if the concatenation `s1 + s2` forms a palindromic string.
  3. Output `"yes"` if such substrings exist, otherwise output `"no"`.
- Practiced nested loops for substring generation and palindrome checking.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** String Manipulation, Substring Operations, Palindrome Checking

## 📖 Problem Description
- **Input**:
  - `T`: Number of test cases.
  - For each test case:
    - Two strings `A` and `B`, consisting of lowercase alphabets.
- **Output**:
  - Print `"yes"` if it is possible to find non-empty substrings `s1` from `A` and `s2` from `B` such that `s1 + s2` is a palindrome.
  - Print `"no"` otherwise.

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter a T number of test cases: 1 Enter a string1: abc Enter a string2: def


**Output**:
no


#### Example 2:
**Input**:
Enter a T number of test cases: 1 Enter a string1: race Enter a string2: car


**Output**:
yes


---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_66 {
    static boolean isPalindrome(String str) {
        int left = 0;
        int right = str.length() - 1;
        while (left <= right) {
            if (str.charAt(left) != str.charAt(right)) {
                return false;
            }
            left++;
            right--;
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Enter a T number of test cases: ");
        int T = input.nextInt();
        input.nextLine();

        for (int i = 0; i < T; i++) {
            System.out.println("Enter a string1: ");
            String A = input.nextLine();
            System.out.println("Enter a string2: ");
            String B = input.nextLine();

            boolean palindrome = false;

            // Generate substrings of A and B
            for (int j = 0; j < A.length(); j++) {
                for (int k = j + 1; k <= A.length(); k++) {
                    String s1 = A.substring(j, k);
                    for (int l = 0; l < B.length(); l++) {
                        for (int m = l + 1; m <= B.length(); m++) {
                            String s2 = B.substring(l, m);
                            if (isPalindrome(s1 + s2)) {
                                palindrome = true;
                                break;
                            }
                        }
                        if (palindrome) break;
                    }
                    if (palindrome) break;
                }
                if (palindrome) break;
            }

            if (palindrome) {
                System.out.println("yes");
            } else {
                System.out.println("no");
            }
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Enter a T number of test cases: 
1
Enter a string1: 
abc
Enter a string2: 
def
no
Example 2:

Enter a T number of test cases: 
1
Enter a string1: 
race
Enter a string2: 
car
yes
```
---
## 📚 Lessons Learned
Practiced generating substrings for palindrome validation.
Improved efficiency by using nested loops and breaking early when a valid condition is found.
Gained insights into optimizing string manipulation tasks in Java.

---
## ⚡ Challenges
Managing time complexity for large strings due to nested loops.
Ensuring proper substring boundaries to avoid StringIndexOutOfBoundsException.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

---
## 100 Days of Code is a challenge created by Ajinkya Kulakarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
