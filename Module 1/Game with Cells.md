# Game with cells

Arty is daydreaming in DSA class. He has a sheet of graph paper with `n` rows and `m` columns, and he imagines that there is an army base in each cell for a total of `n * m` bases. He wants to drop supplies at strategic points on the sheet, marking each drop point with a red dot. If a base contains at least one package inside or on top of its border fence, then it is considered to be supplied.

### Problem Statement

Given `n` and `m`, what is the minimum number of packages that Arty must drop to supply all of his bases?

### Input Format

The first line contains integers `n` and `m`.

### Constraints

1 ≤ `n`, `m` ≤ 1000

### Output Format

Print the minimum number of packages required.

### Sample Input 1

```
2 2
```

### Sample Output 1

```
1
```

### Explanation

Arty has four bases in a grid. If he drops a single package where the walls of all four bases intersect, then those four cells can access the package. Because he managed to supply all four bases with a single supply drop, we print `1` as the answer.

### Solution

```c
#include <stdio.h>
int main(void) 
{
    int n, m, int_pts;
    scanf("%d %d", &n, &m);
    // The mistake I made was not considering the 
    // orientation of the remaining cells instead 
    // calculated totalcells
    // note - 5x5 - 4x4 + 1x4 + 4x1
    // checking parity of n and m
    if (n == 1 && m == 1)
    {
        printf("%d", 1);
    }
    else if (n % 2 != 0 && m % 2 != 0) 
    {
        int_pts = ((n - 1) * (m - 1)) / 4;
        int_pts = int_pts + (n / 2) + (m / 2);
        printf("%d", int_pts + 1);        
    }
    else if (n % 2 != 0 && m % 2 == 0)
    {
        int_pts = (n - 1) * (m) / 4;
        int_pts = int_pts + (m / 2);
        printf("%d", int_pts);
    }
    else if (n % 2 == 0 && m % 2 != 0)
    {
        int_pts = (n) * (m - 1) / 4;
        int_pts = int_pts + (n / 2);
        printf("%d", int_pts);        
    }
    else {    
        printf("%d", (n * m) / 4);
    }
}
