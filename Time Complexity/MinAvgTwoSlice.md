Total score : 100%

Detected time complexity : O(N)

```C#
using System;

class Solution {
    public int solution(int[] A) {
        float minAvg = (A[0] + A[1]) / 2f;
        int minIdx = 0;
        float avg = 0;

        for(int i = 2; i < A.Length; i++) {
            avg = (A[i-2] + A[i-1] + A[i]) / 3f;
            if(minAvg > avg) {
                minAvg = avg;
                minIdx = i-2;
            }

            avg = (A[i-1] + A[i]) / 2f;
            if(minAvg > avg) {
                minAvg = avg;
                minIdx = i-1;
            }
        }
        return minIdx;
    }
}

```
