Total score : 100%

Detected time complexity : O(N * log(N))

```C#
using System;
using System.Linq;

class Solution {
    public int solution(int[] A) {
        Array.Sort(A);

        int leng = A.Length;
        int min = A[0] * A[1] * A[leng-1];
        int max = A[leng-3] * A[leng-2] * A[leng-1];

        return Math.Max(min, max);
    }
}
```
