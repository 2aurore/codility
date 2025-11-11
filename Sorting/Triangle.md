Total score : 93%

Detected time complexity : O(N*log(N))

불필요한 반복 루프 제거
좌측 비교항의 int.MaxValue overflow 해결


```C#
using System;
using System.Linq;

class Solution {
    public int solution(int[] A) {
        if(A == null || A.Length == 0) {
            return 0;
        }

        Array.Sort(A);

        for(int i = 2; i < A.Length; i++) {
            if((long)A[i-2] + A[i-1] > A[i]) {
                return 1;
            } 
        }
        return 0;
    }
}
```

Total score : 93%

Detected time complexity : O(N*log(N))

```C#
using System;
using System.Linq;

class Solution {
    public int solution(int[] A) {
        int count = 0;

        if(A == null || A.Length == 0) {
            return count;
        }

        Array.Sort(A);

        for(int i = 2; i < A.Length; i++) {
            if(A[i-2] + A[i-1] > A[i]){
                count++;
            } 
        }
        return count > 0 ? 1 : 0;
    }
}
```
