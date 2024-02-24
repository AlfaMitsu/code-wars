1/n-Cycle

    int cycle(int n) {
      if (n % 2 == 0 || n % 5 == 0) return -1; // n and 10 are not coprime
      
      var remainders = List<int>.filled(n, 0);
      var remainder = 1;
      var position = 0;
    
      while (remainders[remainder] == 0 && remainder != 0) {
        remainders[remainder] = position;
        remainder = (remainder * 10) % n;
        position++;
      }
    
      return remainder == 0 ? -1 : position - remainders[remainder];
    }
