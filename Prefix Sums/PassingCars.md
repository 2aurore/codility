

total score : 70%

```C#
using System;

class Solution {
    public int solution(int[] A) {
        int left = 0;
        int count = 0;

        foreach(int i in A) {
            if (i == 0) {
                left++;
            } else {
                count = count + left;
            }
        }

        return count;
    }
}
```
