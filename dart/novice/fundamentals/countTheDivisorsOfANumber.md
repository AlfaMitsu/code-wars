Count the divisors of a number

    int divisors(n) {
      int count = 0;
      for (int i = 1; i <= n; i++) {
        if (n % i == 0) {
          count++;
        }
      }
      return count;
    }
