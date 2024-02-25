Late ride

    int lateRide(int n) {
      int hours = n ~/ 60;
      int minutes = n % 60;
      int sum = 0;
      sum += hours ~/ 10 + hours % 10;
      sum += minutes ~/ 10 + minutes % 10;
      return sum;
    }
