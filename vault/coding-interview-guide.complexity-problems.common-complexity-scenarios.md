---
id: QmDtWkYsxMok1tUomni7Z
title: Common Complexity Scenarios
desc: ''
updated: 1638329112730
created: 1637637110142
---

### List of Important Complexities

#### Simple for-loop with an increment of size 1

```java
for (int x = 0; x < n; x++) {
    // statement(s) that take constant time
}
```
Running time Complexity = T(n) = (2n+2) + cn + 2. Dropping the leading constants => n + 2. Dropping lower order terms => O(n).

#### For-loop with increments of size k

```java
for (x = 0; x < n; x+=k) {
    // statement(s) that take constant time
}
```
Running time Complexity = 2 + n((2+c)/k) = O(n)

**Explanation:**
- `x = 0`: 1
- `x < n`: 1 + (n/k) 
    - This is because we have to do one final comparison
- `x+=k`: n/k
- `inside loop`: c * (n/k)
- T(n) = 2 + 2n/k + cn/k = 2 + n(2/k + c/k) = 2 + n((2+c)/k) => O(n)

#### Simple nexted for-loop
