Steps in K-Primes

    List<List<int>> kprimesStep(int k, int step, int start, int end) {
      List<List<int>> result = [];
    
      // Helper function to check if a number is k-prime
      bool isKPrime(int n) {
        int count = 0;
        for (int i = 2; i * i <= n; i++) {
          while (n % i == 0) {
            count++;
            n ~/= i;
          }
        }
        if (n > 1) {
          count++;
        }
        return count == k;
      }
    
      // Find pairs of k-prime numbers with the specified step
      for (int i = start; i <= end - step; i++) {
        if (isKPrime(i) && isKPrime(i + step)) {
          result.add([i, i + step]);
        }
      }
    
      return result;
    }
