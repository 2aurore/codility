total score : 100%

Detected time complexity : O(N + M)


```C#
using System;

class Solution {
    public int[] solution(int N, int[] A) {
        int[] result = new int[N];
        int maximum = 0;
        int lastMaximum = 0;

        foreach(int num in A) {
            if(num <= N && num > 0) {
                int index = num - 1;

                // 카운트 증가 전에 마지막 maximum 값이 업데이트 되었다면 추가 반영
                if (result[index] < lastMaximum) {
                    result[index] = lastMaximum;
                }
                // +1 증가
                result[index]++;

                // 현재 인덱스가 maximum 보다 크다면 업데이트
                if (result[index] > maximum) {
                    maximum = result[index];
                }
            } else {
                // num 이 N 보다 클때 maximum 값으로 업데이트
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
