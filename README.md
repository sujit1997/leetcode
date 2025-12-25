# LeetCode Solutions (Java)

A personal repository for solving LeetCode problems in Java. This repo contains clean, well-documented Java solutions organized for easy lookup, testing, and reuse.

## Table of contents
- [About](#about)
- [Repository structure](#repository-structure)
- [Conventions](#conventions)
- [Java version & build tools](#java-version--build-tools)
- [How to run a solution](#how-to-run-a-solution)
- [Template / Example](#template--example)
- [Adding a new solution](#adding-a-new-solution)
- [Testing](#testing)
- [Tips & utilities](#tips--utilities)
- [Contributing](#contributing)
- [License](#license)

## About
This repository stores my LeetCode problem solutions implemented in Java. Each solution focuses on clarity and correctness, with references to the problem number, title, difficulty, and relevant tags (e.g., `tree`, `dp`, `graph`, `two-pointers`).

## Repository structure
A suggested structure — feel free to adapt:

- /problems
  - /0001_Two_Sum
    - Solution.java
    - README.md (optional: explanation + complexity)
    - input.txt (optional: sample input)
  - /0002_Add_Two_Numbers
- /common (shared helper classes, e.g., ListNode, TreeNode, Utils)
- /tests (JUnit tests or sample runners)
- README.md

Alternative (single-package structure):
- src/main/java/com/yourname/leetcode/... (organized by problem id or topic)
- src/test/java/... (unit tests)

## Conventions
- Directory name format: {zero-padded-id}_{Problem_Title_With_Underscores}
  - Example: `0001_Two_Sum`
- Class / File name: `Solution.java` inside each problem folder (or `Problem0001_TwoSum.java` if you prefer unique filenames)
- Package: use a consistent package like `com.sujit1997.leetcode.problems.id0001`
- Include problem metadata at the top of each file in a comment:
  - LeetCode link, problem id, title, difficulty, tags
  - Time & space complexity
- Use Java 11+ (adjust if you use a different LTS)

## Java version & build tools
Recommended:
- JDK 11 or later
- Build tools (optional):
  - Maven:
    - Add standard Maven layout and dependencies (JUnit 5)
  - Gradle:
    - Use Gradle Kotlin/Groovy DSL with JUnit 5

If you don't use a build tool, plain `javac` / `java` is fine for single-file runs.

## How to run a solution

1. Using javac/java (single file):
   - Compile: javac Solution.java
   - Run: java Solution

   If your solution contains a `main` method that reads from standard input or runs sample test calls.

2. Using Maven:
   - mvn test (for running tests)
   - mvn compile && mvn exec:java -Dexec.mainClass="com.sujit1997.leetcode.problems._0001.Solution"

3. Using an IDE:
   - Import as a Maven/Gradle project or simple Java project and run the `main` method or unit tests.

## Template / Example
Here is a minimal file header and class template to copy into each solution:

```java
/*
 LeetCode Problem: #0001 Two Sum
 Link: https://leetcode.com/problems/two-sum/
 Difficulty: Easy
 Tags: array, hash-table
 Time: O(n)
 Space: O(n)
*/

public class Solution {
    public int[] twoSum(int[] nums, int target) {
        // Implementation
    }

    // Optional main for quick manual testing
    public static void main(String[] args) {
        Solution s = new Solution();
        int[] res = s.twoSum(new int[]{2,7,11,15}, 9);
        System.out.println(Arrays.toString(res)); // [0,1]
    }
}
```

## Adding a new solution
1. Create a new folder under `problems/` named with the problem id and title: `0123_Best_Time_to_Buy_and_Sell_Stock_III`.
2. Add `Solution.java` containing the solution and a brief explanation in comments.
3. Optionally add `README.md` in that folder with:
   - Short explanation of the approach
   - Complexity analysis
   - Links to references
4. Add unit tests (recommended) under `/tests` or `src/test/java`.

## Testing
- Use JUnit 5 for unit tests:
  - Example test class: `Problem0001Test`
  - Run with `mvn test` or from your IDE.
- For quick checks, include a `main` method in `Solution.java` that runs a few examples and prints results.

## Tips & utilities
- Keep common data-structure helpers in `/common`:
  - `ListNode.java`, `TreeNode.java`, `Utils.java` (print helpers, converters)
- Tag problems by difficulty and topics in the folder README or in a master index file (e.g., `INDEX.md`)
- Consider adding a cumulative progress/scoreboard (CSV or markdown) to track solved problems and dates.

## Contributing
This is a personal repository, but if you want to contribute:
- Fork and create a PR
- Follow the repository conventions (naming, metadata)
- Include tests and a short explanation
- Keep implementations idiomatic and well-commented

## License
Choose a license (e.g., MIT) and add a LICENSE file if you want to make this repo open-source.

---

Happy coding — and good luck on your LeetCode journey! If you want, I can:
- Generate a starter project with Maven/Gradle,
- Produce a `Solution.java` template you can paste,
- Create an `INDEX.md` to track progress. Tell me which you'd like next.
