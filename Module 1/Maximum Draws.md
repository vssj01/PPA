Maximum Draws


A student from Programming Pathshala is ready to leave for an interview and needs a matching pair of socks immediately. 
If there are `n` colors of socks in the drawer, how many socks need to be removed to be certain of having a matching pair?

### Input Format:
The first line of input contains `n`.

### Constraints:
1 ≤ n < 10^6

### Output Format:
Print the total number of socks that need to be removed to be certain of having a matching pair.


### Sample Input 1:
1

### Sample Output 1:
2

### Sample Input 2:
2

### Sample Output 2:
3


### Explanation:
- Case 1: Only 1 color of sock is in the drawer. Any will match.
- Case 2: 2 colors of socks are in the drawer. The first two removed may not match. At least 3 socks need to be removed to guarantee success.

### Example:
Input:<br>
2<br>
Output:<br>
3


### Solution
```c
#include <stdio.h>

int main(){
    int n;
    scanf("%d", &n);
    printf("%d", n+1);
    return 0;
}
