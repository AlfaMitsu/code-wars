Growing plant

    int growingPlant(int upSpeed, int downSpeed, int desiredHeight) {
      int currentHeight = 0;
      int days = 0;
      
      while (currentHeight < desiredHeight) {
        days++;
        currentHeight += upSpeed;
        if (currentHeight >= desiredHeight) {
          break;
        }
        currentHeight -= downSpeed;
      }
      
      return days;
    }
