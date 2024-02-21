Sum by Factors

    bool isPrime(int n) {
      if (n <= 1) return false;
      if (n == 2) return true;
      if (n % 2 == 0) return false;
      for (int i = 3; i <= n ~/ 2; i += 2) {
        if (n % i == 0) return false;
      }
      return true;
    }
    
    String sumOfDivided(List<int> l) {
      if (l.isEmpty) return '';
    
      Set<int> primes = {};
      for (int num in l) {
        for (int i = 2; i <= num.abs(); i++) {
          if (isPrime(i) && num % i == 0) {
            primes.add(i);
          }
        }
      }
    
      Map<int, int> sumMap = {};
      for (int prime in primes) {
        int sum = 0;
        for (int num in l) {
          if (num % prime == 0) sum += num;
        }
        sumMap[prime] = sum;
      }
    
      List<List<int>> result = sumMap.entries.map((entry) => [entry.key, entry.value]).toList();
      result.sort((a, b) => a[0].compareTo(b[0]));
    
      return result.map((pair) => '(${pair[0]} ${pair[1]})').join();
    }
