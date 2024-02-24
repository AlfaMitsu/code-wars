Primorial of a Number

    int numPrimorial(int n) {
      int result = 1;
      int count = 0;
      int currentNumber = 2;
    
      while (count < n) {
        if (isPrime(currentNumber)) {
          result *= currentNumber;
          count++;
        }
        currentNumber++;
      }
    
      return result;
    }
    
    bool isPrime(int number) {
      if (number < 2) return false;
      for (int i = 2; i <= number / 2; i++) {
        if (number % i == 0) return false;
      }
      return true;
    }
