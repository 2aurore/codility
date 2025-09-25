total score : 100%

Detected time complexity : O(N + M)


```C#
using System;

class Solution {
    public int[] solution(int N, int[] A) {
        // Implement your solution here
        int[] result = new int[N];
        int maximum = 0;
        int lastMaximum = 0;

        foreach(int num in A) {
            int index = num - 1;

            if(num <= N && num > 0) {

                if (result[index] < lastMaximum) {
                    result[index] = lastMaximum;
                }

                result[index]++;

                if (result[index] > maximum) {
                    maximum = result[index];
                }
            } else {
                lastMaximum = maximum;
            }
        }

        for(int i = 0; i < result.Length; i ++) {
            if (result[i] <  lastMaximum) {
                result[i] =  lastMaximum;   
            }
        }

        return result;
    }
}
```

total score : 88%

`반복문 내에서 Array.Fill 반복 수행하여 시간 복잡도 증가`

```C#
using System;

class Solution {
    public int[] solution(int N, int[] A) {
        // Implement your solution here
        int[] result = new int[N];
        int maxValue = 0;

        foreach(int num in A) {
            if(num <= N && num > 0) {
                result[num-1] += 1;
                maxValue = Math.Max(maxValue, result[num-1]);
            }
            else {
                Array.Fill(result, maxValue);
            }
        }

        return result;
    }
}
```
