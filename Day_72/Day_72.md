# Day 72 of 100 - 100 Days of Code Challenge

## 📝 Overview
Welcome to **Day 72** of my **100 Days of Code Challenge**! Today, I implemented a simple editor using Java, which supports two primary operations:
1. Insert a string at a specified position.
2. Query and print a substring of a specified length starting from a given position.

This problem required efficient string manipulation and query processing.

## ✅ What I did today
- Built a text editor using a `StringBuilder` to handle dynamic string modifications efficiently.
- Implemented two operations:
  1. **Insert Operation**: Adds a substring at a given position.
  2. **Query Operation**: Retrieves and prints a specific substring.

## 💻 Technologies Used
- **Programming Language:** Java
- **Concepts:** StringBuilder, String Manipulation, Query Processing

## 📖 Problem Description
- **Input**:
  - `Q`: Number of queries.
  - For each query:
    - `+ i x`: Insert string `x` after the `i`-th character (1-indexed) of the current string.
    - `? i len`: Print the substring of length `len` starting from the `i`-th character (1-indexed).
- **Output**:
  - For each query of type `?`, print the required substring.

---

### Input/Output Example:

#### Example 1:
**Input**:
Enter the Q queries: 5

0 Hello
5 World ? 1 5
5 Amazing ? 6 6


**Output**:
Hello WorldA


---

## 📝 Code Example

```java
package coading_Challange;

import java.util.Scanner;

public class Day_72 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.println("Enter the Q queries: ");
        int Q = input.nextInt();
        input.nextLine(); // Consume the newline character

        // Use StringBuilder for efficient string manipulation
        StringBuilder string = new StringBuilder();

        for (int i = 0; i < Q; i++) {
            System.out.println("Enter a query " + (i + 1) + ": ");
            String query = input.nextLine();

            if (query.startsWith("+")) {
                // Parse the insert operation
                String[] parts = query.split(" ");
                int start = Integer.parseInt(parts[1]);
                String end = parts[2];
                string.insert(start, end); // Insert the string at the specified position
            } else if (query.startsWith("?")) {
                // Parse the query operation
                String[] parts = query.split(" ");
                int start = Integer.parseInt(parts[1]) - 1; // Convert to 0-indexed
                int len = Integer.parseInt(parts[2]);

                // Print the substring
                System.out.println(string.substring(start, start + len));
            }
        }

        input.close();
    }
}
🖥️ Program Output
Example 1:

Enter the Q queries:
5
Enter a query 1: 
+ 0 Hello
Enter a query 2: 
+ 5 World
Enter a query 3: 
? 1 5
Hello
Enter a query 4: 
+ 5 Amazing
Enter a query 5: 
? 6 6
WorldA
```
---
## 📚 Lessons Learned
Learned how to use StringBuilder for efficient string manipulation, especially for insertion and query operations.
Practiced processing string-based queries using split and string indexing techniques.
Improved problem-solving skills for managing dynamic data with minimal performance overhead.

---
## ⚡ Challenges
Handling edge cases such as invalid indices or empty strings during insertions and queries.
Ensuring that all operations are processed in the correct sequence and indices are 1-indexed as per the problem requirements.

---
## 📬 Connect with me
- Email: kiranreddy4746@gmail.com
- LinkedIn: [Chandra Kiran Reddy Reddycharla](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)
- Twitter: @kiran4746

--- 
## 100 Days of Code is a challenge created by Ajinkya Kulkarni, Amit Prabhu. Join the community using the hashtag #100DaysOfCode on LinkedIn and other social platforms.
