Get the mean of an array

    int getAverage(List<int> marks) {
      int sum = marks.reduce((value, element) => value + element);
      return sum ~/ marks.length;
    }
