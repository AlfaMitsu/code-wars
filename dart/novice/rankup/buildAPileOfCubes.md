Build a pile of Cubes

    int findNb(int m) {
      var totalVolume = 0;
      var n = 1;
      
      while (totalVolume < m) {
        totalVolume += n * n * n;
        if (totalVolume == m) {
          return n;
        }
        n++;
      }
      
      return -1;
    }
