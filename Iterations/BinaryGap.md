
total score : 100%

```C#
using System;

class Solution {
    public int solution(int N) {
        // N을 이진수 문자열로 변환
        string binary = Convert.ToString(N, 2);

        int maxGap = 0;          // 최대 gap 저장 변수
        int currentGap = 0;      // 현재 gap 저장 변수
        bool countFlag = false;  // max gap 업데이트 플래그

        foreach(char num in binary) {
            if(num == '1') {
                // 플래그 true 인 상태에서 다음 1을 만났을때 max 값을 업데이트
                if(countFlag){
                    // 현재 카운트된 gap 과 max gap 중 더 큰 값으로 적용
                    maxGap = Math.Max(maxGap, currentGap);
                    currentGap = 0;
                }
                // 최초에 1을 만났을 때 플래그 on
                countFlag = true;
            } else if (countFlag) {
                // 1을 만난 다음부터 0의 갯수 카운트
                currentGap += 1;
            }
        }

        return maxGap;
    }
}
```
