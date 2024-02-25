String prefix and suffix

    int solve(String s) {
      int len = s.length;
      for (int i = len ~/ 2; i > 0; i--) {
        if (s.substring(0, i) == s.substring(len - i)) {
          return i;
        }
      }
      return 0;
    }
