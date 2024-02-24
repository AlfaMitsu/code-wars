Deodorant Evaporator

    int evaporator(double content, double evap_per_day, double threshold) {
      int day = 0;
      double remaining = 100.0;
      
      while (remaining > threshold) {
        remaining *= (1 - evap_per_day / 100);
        day++;
      }
      
      return day;
    }
