total score : 100%

```C#
using System;

class Solution {
    public int solution(int X, int Y, int D) {
               
        int distance = Y - X;

        if(distance == 0) {
            return 0;
        }

        int jumps = (distance / D) + (distance % D > 0 ? 1 : 0);
        return jumps;
    }
}
```
