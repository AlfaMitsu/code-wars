Strong Number

    String strong(int n) {
      int sum = 0;
      int originalNumber = n;
      while (n > 0) {
        int digit = n % 10;
        sum += factorial(digit);
        n ~/= 10;
      }
      return sum == originalNumber ? "STRONG!!!!" : "Not Strong !!";
    }
    
    int factorial(int n) {
      return n == 0 ? 1 : n * factorial(n - 1);
    }
