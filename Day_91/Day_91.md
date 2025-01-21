# Day 91 of 100 - 100 Days of Code Challenge

## 📝 Problem: Reconstruct Travel Itinerary and Total Cost

Sridhar is a seasoned traveler and a meticulous planner. He writes down his travel itinerary as cards with the format:
A B C


Where:
- `A` is the starting city.
- `B` is the destination city.
- `C` is the cost to travel from `A` to `B`.

Due to an unfortunate incident, the cards got shuffled. Sridhar needs help to:
1. Reconstruct the original order of the journey.
2. Calculate the total cost of the journey.

---

## 🔗 Input and Output Format

### Input:
1. The first line contains \( T \), the number of test cases.
2. For each test case:
   - The first line contains \( N \), the number of cities (or \( N-1 \) cards).
   - The next \( N-1 \) lines contain the shuffled cards in the format: `A B C`.

### Output:
For each test case:
1. Output the reconstructed journey, one card per line in the correct order.
2. Output the total cost of the journey on a new line.

---

## 💡 Approach

1. **Data Structures**:
   - Use a **HashMap** to store the direct mapping of `A -> B`.
   - Use another **HashMap** to store the reverse mapping `B -> A`.
   - Use a third **HashMap** to store the travel costs for each card.

2. **Find the Starting City**:
   - The starting city will be the one that doesn't appear as a destination in the `B` column.

3. **Reconstruct the Journey**:
   - Start from the identified starting city and traverse using the `A -> B` map until no further cities are found.

4. **Calculate Total Cost**:
   - Sum the travel costs during the reconstruction of the journey.

---

## 🚀 Code Implementation

```java
package coading_Challange;

import java.util.*;

public class Day_91 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Enter number of test cases:");
        int T = input.nextInt();
        input.nextLine(); // Consume the newline character

        for (int t = 0; t < T; t++) {
            System.out.println("Enter number of cities (N):");
            int N = input.nextInt();
            input.nextLine(); // Consume the newline character

            // Read travel cards
            Map<String, String> nextCityMap = new HashMap<>(); // A -> B mapping
            Map<String, String> prevCityMap = new HashMap<>(); // B -> A mapping
            Map<String, Integer> costMap = new HashMap<>();    // "A->B" -> Cost
            Set<String> cities = new HashSet<>();

            for (int i = 0; i < N - 1; i++) {
                String line = input.nextLine();
                String[] parts = line.split(" ");
                String A = parts[0];
                String B = parts[1];
                int C = Integer.parseInt(parts[2]);

                nextCityMap.put(A, B);
                prevCityMap.put(B, A);
                costMap.put(A + "->" + B, C);

                cities.add(A);
                cities.add(B);
            }

            // Find the starting city
            String startCity = null;
            for (String city : cities) {
                if (!prevCityMap.containsKey(city)) {
                    startCity = city;
                    break;
                }
            }

            // Reconstruct the journey
            String currentCity = startCity;
            List<String> orderedCards = new ArrayList<>();
            int totalCost = 0;

            while (nextCityMap.containsKey(currentCity)) {
                String nextCity = nextCityMap.get(currentCity);
                int cost = costMap.get(currentCity + "->" + nextCity);
                orderedCards.add(currentCity + " " + nextCity + " " + cost);
                totalCost += cost;
                currentCity = nextCity;
            }

            // Output the result
            for (String card : orderedCards) {
                System.out.println(card);
            }
            System.out.println(totalCost);
        }

        input.close();
    }
}
📊 Sample Input and Output
Input:

1
5
Madrid Paris 100
Paris Munich 200
Munich Warsaw 150
Warsaw Kiev 120
Output:

Madrid Paris 100
Paris Munich 200
Munich Warsaw 150
Warsaw Kiev 120
570
```
---
## 🛠️ Technologies Used
- Language: Java
- Concepts: HashMaps, Iteration, Graph Traversal, Adjacency Mapping

---
## 🤝 Connect with Me
- GitHub: kiranreddy4433E
- LinkedIn: [Chandra Kiran Reddy](https://www.linkedin.com/in/chandra-kiran-reddy-reddycharla-a9a746230/)

--- 
## 🌟 Acknowledgments
This problem is part of my 100 Days of Code Challenge, where I aim to solve coding problems daily and enhance my problem-solving skills.
