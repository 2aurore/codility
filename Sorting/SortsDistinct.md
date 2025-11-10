Total score : 100%

Detected time complexity : O(N*log(N)) or O(N)

```C#
using System;
using System.Collections.Generic;

class Solution {
    public int solution(int[] A) {
        if (A == null || A.Length == 0) {
            return 0;
        }

        HashSet<int> hashSet = new HashSet<int>(A);

        return hashSet.Count;
    }
}
```
