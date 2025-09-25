total score : 100%

Detected time complexity : O(N)


```C#
using System;
using System.Collections.Generic;

class Solution {
    public int solution(int X, int[] A) {
        HashSet<int> steps = new HashSet<int>();
        int result = -1; 

        for(int i = 0; i < A.Length; i++) {
            if (A[i] <= X) {
                steps.Add(A[i]);
            }
            if (steps.Count == X) {
                result = i;
                break;
            }
        }
        return result;
    }
}
```
