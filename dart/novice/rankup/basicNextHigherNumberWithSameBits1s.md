Find next higher number with same Bits (1's)

    int nextHigher(int n) {
      int c = n, c0 = 0, c1 = 0;
    
      // Count trailing zeros
      while ((c & 1) == 0 && c != 0) {
        c0++;
        c >>= 1;
      }
    
      // Count consecutive 1s after trailing zeros
      while ((c & 1) == 1) {
        c1++;
        c >>= 1;
      }
    
      // Error case: no higher number with same number of 1 bits
      if (c0 + c1 == 31 || c0 + c1 == 0) {
        return -1;
      }
    
      // Position of rightmost non-trailing zero
      int p = c0 + c1;
    
      // Flip rightmost non-trailing zero
      n |= (1 << p);
    
      // Clear all bits to the right of p
      n &= ~((1 << p) - 1);
    
      // Insert (c1-1) ones on the right
      n |= (1 << (c1 - 1)) - 1;
    
      return n;
    }
