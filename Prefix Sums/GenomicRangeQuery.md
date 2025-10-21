Total score : 100%

Detected time complexity : O(N + M)

```C#
using System;

class Solution {
    public int[] solution(string S, int[] P, int[] Q) {
        int N = S.Length;
        int M = P.Length;

        int[] prefixA = new int[N+1];
        int[] prefixC = new int[N+1];
        int[] prefixG = new int[N+1];

        int[] results = new int[M];

        for(int i = 0; i < N; i++){
            prefixA[i+1] = prefixA[i];
            prefixC[i+1] = prefixC[i];
            prefixG[i+1] = prefixG[i];

            switch(S[i]) {
                case 'A':
                    prefixA[i+1]++;
                    break;
                case 'C':
                    prefixC[i+1]++;
                    break;
                case 'G':
                    prefixG[i+1]++;
                    break;
            }
        }

        for(int i = 0; i < M; i++) {
            int startIndex = P[i];
            int endIndex = Q[i];

            if (prefixA[endIndex + 1] - prefixA[startIndex] > 0)
            {
                results[i] = 1;
            }
            else if (prefixC[endIndex + 1] - prefixC[startIndex] > 0)
            {
                results[i] = 2;
            }
            else if (prefixG[endIndex + 1] - prefixG[startIndex] > 0)
            {
                results[i] = 3;
            }
            else
            {
                results[i] = 4;
            }
        }

        return results;

    }
}
```
