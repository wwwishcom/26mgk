# 2회차. 26.07.21(화)
### Aoj - 이분탐색
방학동안 알고리즘 공부를 위해 Aoj에서 이분탐색 유형의 문제들을 우선 풀어보기로 했다.

### 1212. 정렬된 수 3
https://aoj.anacnu.kr/problems/1212

첫 번째 문제는 실버4 정도 수준의 이분탐색 문제였다.

```
import sys
from bisect import bisect_left, bisect_right

input = sys.stdin.readline

N, Q = map(int(input()).split())
A = list(map(int, input().split()))

result = []
for _ in range(Q):
    k = int(input())
    cnt = bisect_right(A, k) - bisect_left(A, k)
    result.append(cnt)

for r in result:
    print(r)
```

일단 문제부터가 런타임 에러 뜰 거 같은 문제여서

import sys, 이분탐색까지 신경써서 했는데

```
for r in result:
  print(r)
```
부분에서 런타임에러가 생긴 거 같다.
