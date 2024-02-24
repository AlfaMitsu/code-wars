Moduli Number System

    String fromNb2Str(int n, List<int> bases) {
      if (bases.reduce((a, b) => a * b) <= n || !areCoprime(bases)) {
        return "Not applicable";
      }
    
      return bases.map((base) => "-${n % base}-").join();
    }
    
    bool areCoprime(List<int> bases) {
      for (int i = 0; i < bases.length; i++) {
        for (int j = i + 1; j < bases.length; j++) {
          if (gcd(bases[i], bases[j]) != 1) {
            return false;
          }
        }
      }
      return true;
    }
    
    int gcd(int a, int b) {
      if (b == 0) {
        return a;
      } else {
        return gcd(b, a % b);
      }
    }
