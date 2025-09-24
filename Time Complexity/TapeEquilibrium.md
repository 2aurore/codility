total score : 100%

Detected time complexity : O(N)


```C#
using System;

class Solution {
    public int solution(int[] A) {
        int total = 0;
        int minDiff = 0;
        int currentDiff = 0;
        int left = 0;

        foreach(int num in A) {
            total += num;
        }

        for(int i = 0; i < A.Length -1; i++) {
            left += A[i];
            int right = total - left;
            currentDiff = Math.Abs(left - right);

            if(i == 0) {
                minDiff = currentDiff;
            } else {
                minDiff = Math.Min(minDiff, currentDiff);
            }
        }

        return minDiff;
    }
}
```
