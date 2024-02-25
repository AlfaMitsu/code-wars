See you next happy year

    int nextHappyYear(int year) {
      while (true) {
        year++;
        String yearString = year.toString();
        Set<String> digits = yearString.split('').toSet();
        if (digits.length == yearString.length) {
          return int.parse(yearString);
        }
      }
    }
