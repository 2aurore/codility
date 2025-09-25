total score : 100%

Detected time complexity : O(N) or O(N * log(N))


```C#
using System;
using System.Collections.Generic;

class Solution {
    public int solution(int[] A) {
        HashSet<int> hashset = new HashSet<int>();

        foreach(int num in A) {
            if(num > 0) {
                hashset.Add(num);
            }
        }

        int result = 1;
        while(hashset.Contains(result)) {
            result++;
        }
        
        return result;
    }
}
```
