Consecutive digits to form sum

    bool consecutiveDucks(int n) {
      for (int k = 1; k < n; k++) {
        double x = (n - k * (k + 1) / 2) / (k + 1);
        if (x <= 0) {
          return false;
        }
        if (x == x.toInt()) {
          return true;
        }
      }
      return false;
    }
