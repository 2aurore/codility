
total score : 100% 


```C#C#
using System;

class Solution
{
    public int[] solution(int[] A, int K)
    {
        int N = A.Length;

        // rotation이 필요하지 않은 경우
        if (N == 0 || K == 0)
        {
            return A;
        }

        // K 가 N 보다 큰 경우를 처리하기 위해 필요 횟수만 연산할 수 있도록 함
        K %= N;

        // K = 0 으로 rotation이 불필요한 경우
        if (K == 0)
        {
            return A;
        }

        int[] result = new int[N];

        Array.Copy(A, N - K, result, 0 , K);
        Array.Copy(A, 0, result, K, N - K);
        return rotatedArray;
    }
}
```
