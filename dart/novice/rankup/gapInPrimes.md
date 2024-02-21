Gap in Primes

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
    
    List<int> gap(int g, int m, int n) {
      int? prevPrime = null;
    
      for (int i = m; i <= n; i++) {
        if (isPrime(i)) {
          if (prevPrime != null && i - prevPrime == g) {
            return [prevPrime, i];
          }
          prevPrime = i;
        }
      }
    
      return [];
    }
