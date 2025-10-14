total score : 100%

Detected time complexity : O(N)


```C#
using System;

class Solution {
    public int solution(int[] A) {
        int left = 0;
        int count = 0;

        foreach(int i in A) {
            if (i == 0) {
                left++;
            } else {
                count = count + left;
            }

            if (count > 1000000000) {
                return -1;
            }
        }

        return count;
    }
}
```



total score : 70%

```C#
using System;

class Solution {
    public int solution(int[] A) {
        int left = 0;
        int count = 0;

        foreach(int i in A) {
            if (i == 0) {
                left++;
            } else {
                count = count + left;
            }
        }

        return count;
    }
}
```
