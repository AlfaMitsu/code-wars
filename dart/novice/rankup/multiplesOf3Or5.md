Multiples of 3 or 5

    int solution(int n) {
      if (n < 0) return 0;
      
      int sum = 0;
      for (int i = 1; i < n; i++) {
        if (i % 3 == 0 || i % 5 == 0) {
          sum += i;
        }
      }
      return sum;
    }
