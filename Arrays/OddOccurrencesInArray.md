
total score : 100% 

```C#
using System;

class Solution
{
    public int solution(int[] A)
    {
        int unpairedElement = 0;

        foreach (int number in A)
        {
            // XOR 연산으로 pair가 되는 수를 검증
            unpairedElement ^= number;
        }

        return unpairedElement;
    }
}
```
