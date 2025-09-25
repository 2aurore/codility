total score : 100%

Detected time complexity : O(N) or O(N * log(N))


```C#
using System;
using System.Collections.Generic;

class Solution {
    public int solution(int[] A) {
        HashSet<int> sets = new HashSet<int>();
        int result = 0;

        foreach(int num in A) {
            if(num <= A.Length) {
                sets.Add(num);
            }
        }

        if (A.Length == sets.Count){
            result = 1;
        }
        return result;
    } 
}
```
