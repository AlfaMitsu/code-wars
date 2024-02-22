Count the Digit

    int nbDig(int n, int d) {
      int count = 0;
      for (int i = 0; i <= n; i++) {
        int square = i * i;
        do {
          if (square % 10 == d) {
            count++;
          }
          square ~/= 10;
        } while (square > 0);
      }
      return count;
    }
