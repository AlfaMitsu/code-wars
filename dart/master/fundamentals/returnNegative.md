Return Negative

    num makeNegative(num n) {
      // If the number is greater than zero, multiply it by -1 to make it negative
      if (n > 0) {
        return -n;
      }
      // If the number is zero or already negative, return it as is
      return n;
    }
    
    void main() {
      print(makeNegative(1));    // Output: -1
      print(makeNegative(-5));   // Output: -5
      print(makeNegative(0));    // Output: 0
      print(makeNegative(0.12)); // Output: -0.12
    }
