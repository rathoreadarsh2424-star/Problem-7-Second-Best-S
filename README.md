# Problem 7: Second-Best Score

Java solution for the attached Category C coding assignment.

## Approach
- Traverse the scores once; do not sort the array.
- Keep `highest` and `second` distinct scores.
- If a score is greater than `highest`, shift the old `highest` into `second`.
- Otherwise, update `second` only if the score is less than `highest` and greater than `second`.
- Return `-1` when no second-highest distinct score exists.

## Complexity
- Time: **O(n)** — each score is visited once.
- Auxiliary space: **O(1)** — only two tracking variables are used by the function.
- Sorting first would generally take **O(n log n)** time and may need extra space depending on the sorting algorithm.

## Sample checks
- `[45, 78, 92, 78, 60]` → `78`
- `[50, 50, 50]` → `-1`

## Compile and run
From the `src` directory:

```bash
javac Problem7SecondBestScore.java
java Problem7SecondBestScore
```
