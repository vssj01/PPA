# Handshakes

**Problem Statement:**

Programming Pathshala is organizing a meet. There will be **N** people present at the meet. Your task is to find out the total number of handshakes if every attendant shakes hands with the others exactly one time.

---

## Input Format

The first line of input contains **n**.

---

## Constraints

1 ≤ n < 10⁶

---

## Output Format

Print the total number of handshakes.

---

## Sample Input 1

```
3
```

## Sample Output 1

```
3
```

---

## Sample Input 2

```
5
```

## Sample Output 2

```
10
```

---

## Explanation

### Case 1:
There are **3** people, so **3** handshakes take place. 

- **P1** shakes hands with **P2** and **P3**, and 
- **P2** shakes hands with **P3**.

### Example:

#### Input:
```
5
```

#### Output:
```
10
```

---

## Solution (C Code):

```c
#include <stdio.h>
int main(void) {
    int n;
    scanf("%d",&n);
    // considering n to be 1000000 then n*(n-1) will cause integer overflow.
    // I have correctly used format specifier as ld but need to use explicit type casting for product
    // printf("%ld",(n - 1) * n / 2)
    printf("%ld",(long)(n - 1) * n / 2);
    return 0;
}
```
