Speed Control

    int gps(int s, List<double> x) {
      if (x.length <= 1) return 0;
    
      double maxSpeed = 0;
      for (int i = 1; i < x.length; i++) {
        double speed = (3600 * (x[i] - x[i - 1])) / s;
        if (speed > maxSpeed) {
          maxSpeed = speed;
        }
      }
    
      return maxSpeed.floor();
    }
