Steps in Primes

    List<int> step(int g, int start, int end) {
      bool isPrime(int n) {
        if (n <= 1) return false;
        if (n <= 3) return true;
        if (n % 2 == 0 || n % 3 == 0) return false;
        int i = 5;
        while (i * i <= n) {
          if (n % i == 0 || n % (i + 2) == 0) return false;
          i += 6;
        }
        return true;
      }
    
      for (int i = start; i <= end - g; i++) {
        if (isPrime(i) && isPrime(i + g)) {
          return [i, i + g];
        }
      }
      return [];
    }
