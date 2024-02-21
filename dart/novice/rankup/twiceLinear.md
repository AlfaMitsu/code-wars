Twice Linear

    int dblLinear(int n) {
      List<int> u = [1];
      int xIndex = 0;
      int yIndex = 0;
      
      while (u.length <= n) {
        int nextX = 2 * u[xIndex] + 1;
        int nextY = 3 * u[yIndex] + 1;
        
        if (nextX <= nextY) {
          u.add(nextX);
          xIndex++;
          if (nextX == nextY) yIndex++;
        } else {
          u.add(nextY);
          yIndex++;
        }
      }
      
      return u[n];
    }
