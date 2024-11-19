**Find Point**

Given two points, p = (px, py) and q = (qx, qy). We consider reflection or image r = (rx, ry), of point p across point q to be a 180° rotation of point p around q.

Given points p and q, find point r and print two space-separated integers denoting the respective values of rx and ry on a new line.

### Input Format

The first line of input contains 4 integers:  
px, py, qx, qy

### Constraints

- The values of px, py, qx, qy are between -100 and 100 inclusive.

### Output Format

Print the reflection or image point.

### Sample Input 1
```
0 0 1 1
```

### Sample Output 1
```
2 2
```

### Explanation

For case 1,  
p = (0, 0) and q = (1, 1).  
Therefore,  
r = (2, 2).

```c
#include <stdio.h>
int main(void) 
{
    int px, py, qx, qy;
    scanf("%d %d %d %d", &px, &py, &qx, &qy);
    printf("%d %d", 2*qx - px, 2*qy - py);
    return 0;
}
```
