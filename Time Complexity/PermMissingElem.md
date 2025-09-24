total score : 100% 

Detected time complexity : O(N) or O(N * log(N))


```C#
using System;

class Solution {
    public int solution(int[] A) {
        long N = A.Length +1;

        long totalSum = N * (N+1) / 2;

        long arraySum = 0;
        foreach(int num in A) {
            arraySum += num;
        }

        return (int)(totalSum - arraySum);
    }
}
```


total score : 80%

`전체 합 계산 시 int 범위를 초과해서 lage_range failed `

```C#
using System;

class Solution {
    public int solution(int[] A) {
        int N = A.Length +1;

        int totalSum = N * (N+1) / 2;

        int arraySum = 0;
        foreach(int num in A) {
            arraySum += num;
        }

        int missingNum = totalSum - arraySum;
        return missingNum;
    }
}
```
