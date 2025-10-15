total score : 100%

Detected time complexity : O(1)

```C#
using System;
class Solution {
    public int solution(int A, int B, int K) {
        int count = (B / K) - (A / K);
        if (A % K == 0) count++;
        return count;
    }
}
```


total score : 50%
- TIMEOUT ERROR
- Detected time complexity : O(B-A)

```C#
using System;

class Solution {
    public int solution(int A, int B, int K) {
        int count = 0;

        for(int i = A; i <= B; i++) {
            if (i % K == 0) {
                count++;
            }
        }
        return count;
    }
}
```
