Factorial Decomposition

    String decomp(int n) {
      List<int> primes = sieveOfEratosthenes(n);
      List<int> counts = List<int>.filled(primes.length, 0);
    
      for (int i = 0; i < primes.length; i++) {
        int p = primes[i];
        int k = p;
        while (k <= n) {
          counts[i] += n ~/ k;
          k *= p;
        }
      }
    
      String result = '';
      for (int i = 0; i < primes.length; i++) {
        if (counts[i] > 0) {
          if (result.isNotEmpty) {
            result += ' * ';
          }
          result += '${primes[i]}';
          if (counts[i] > 1) {
            result += '^${counts[i]}';
          }
        }
      }
    
      return result;
    }
    
    List<int> sieveOfEratosthenes(int n) {
      List<bool> isPrime = List<bool>.filled(n + 1, true);
      isPrime[0] = isPrime[1] = false;
      for (int i = 2; i <= n; i++) {
        if (isPrime[i]) {
          for (int j = i * i; j <= n; j += i) {
            isPrime[j] = false;
          }
        }
      }
      return List.generate(n + 1, (index) => index).where((element) => isPrime[element]).toList();
    }
