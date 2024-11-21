# Min Height Triangle

Given integers `b` and `a`, find the smallest integer `h` such that there exists a triangle of height `h`, base `b`, having an area of at least `a`.

### Input Format

The first line contains integers `b` and `a`.

### Constraints

1 ≤ `a`, `b` ≤ 10⁶

### Output Format

Print the minimum integer height to form a triangle with an area of at least `a`.

### Sample Input 1

```
2 2
```

### Sample Output 1

```
2
```

### Sample Input 2

```
17 100
```

### Sample Output 2

```
12
```

### Explanation

The task is to find the smallest integer height of the triangle with base `2` and area at least `2`. It turns out, that there are triangles with height `2`, base `2`, and area `2`, for example, a triangle with corners in the following points: `(1,1)`, `(3,1)`, `(1,3)`.

It can be proved that there is no triangle with integer height smaller than `2`, base `2`, and area at least `2`.

### Solution

```c
#include <stdio.h>

int main() {
    int b, a, h;
    scanf("%d %d", &b, &a);
    // normal integer division
    h = 2 * a / b;
    // if 2*a is not perfectly divisible by b, this means there is some height left in the integer division, hence round up h by 1
    if (2 * a % b != 0) {
        h++;
    }
    printf("%d", h);
}
