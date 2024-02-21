Primes in Numbers

    String primeFactors(int n) {
      var factors = <int>[];
      var remaining = n;
      
      for (var i = 2; i * i <= n; i++) {
        while (remaining % i == 0) {
          factors.add(i);
          remaining ~/= i;
        }
      }
      
      if (remaining > 1) {
        factors.add(remaining);
      }
    
      var result = '';
      var currentFactor = factors.first;
      var count = 0;
    
      for (var factor in factors) {
        if (factor == currentFactor) {
          count++;
        } else {
          result += '(${currentFactor}${count > 1 ? '**$count' : ''})';
          currentFactor = factor;
          count = 1;
        }
      }
    
      result += '(${currentFactor}${count > 1 ? '**$count' : ''})';
    
      return result;
    }
