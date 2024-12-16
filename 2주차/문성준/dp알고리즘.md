## 🔥 DP 문제 연습 <br>
### 🌟 쉬운 단계
피보나치 수열 (기본 DP 문제)<br>
1로 만들기 (백준 1463)<br>
계단 오르기 (백준 2579)<br><hr>
### 🌟 중간 단계
이친수 (백준 2193)<br>
2×n 타일링 (백준 11726)<br>
2×n 타일링 2 (백준 11727)<br><hr>
### 🌟 어려운 단계
LCS (최장 공통 부분 수열) (백준 9251)<br>
가장 긴 증가하는 부분 수열 (LIS) (백준 11053)<br>
RGB 거리 (백준 1149)
<br><hr>
### 😎 추천 학습 루트
피보나치 문제로 시작합니다 (점화식: dp[i] = dp[i-1] + dp[i-2])<br>
2×n 타일링 문제를 풀어봅니다 (점화식이 피보나치와 유사합니다)<br>
그다음, 계단 오르기 문제로 DP 개념을 확장합니다.<br>
<br><hr>

### code
```
// DP 자료구조의 예시 구현 (피보나치 수열 예시)
    public static int fibonacci(int n) {
        if (n <= 1) {
            return n;
        }
        int[] dp = new int[n + 1]; // n까지의 피보나치 수를 저장하는 DP 배열
        dp[0] = 0; // 피보나치 수열의 첫 번째 값
        dp[1] = 1; // 피보나치 수열의 두 번째 값
        
        for (int i = 2; i <= n; i++) {
            dp[i] = dp[i - 1] + dp[i - 2]; // 점화식: F(n) = F(n-1) + F(n-2)
        }
        
        return dp[n];
    }
    
    // DP 자료구조의 메모리 최적화 버전 (변수 2개만 사용하는 피보나치 수열 예시)
    public static int fibonacciOptimized(int n) {
        if (n <= 1) {
            return n;
        }
        int prev2 = 0; // F(n-2)
        int prev1 = 1; // F(n-1)
        int current = 0; // F(n)
        
        for (int i = 2; i <= n; i++) {
            current = prev1 + prev2; // 점화식: F(n) = F(n-1) + F(n-2)
            prev2 = prev1; // 이전 값 갱신
            prev1 = current; // 현재 값 갱신
        }
        
        return current;
    }
```



