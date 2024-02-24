Ball Upwards

    int maxBall(int v0) {
      double g = 9.81; // Acceleration due to gravity in m/s^2
      double vms = v0 * 1000 / 3600; // Convert velocity from km/h to m/s
      double tMax = vms / g; // Time to reach max height in seconds
      return (tMax * 10).round(); // Convert time to tenths of a second
    }
