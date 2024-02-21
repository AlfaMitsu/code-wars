Memorized Log Cutting

    import "dart:math";
        
    int cutLog(List<int> p, int n) {
      List<int> dp = List.filled(n + 1, 0);
    
      for (int i = 1; i <= n; i++) {
        int q = -1;
        for (int j = 1; j <= i; j++) {
          q = max(q, p[j] + dp[i - j]);
        }
        dp[i] = q;
      }
    
      return dp[n];
    }
