How many stairs will Suzuki climb in 20 years?

    int stairsIn20(List<List<int>> arr) {
      int oneYearTotal = arr.expand((day) => day).reduce((value, element) => value + element);
      return oneYearTotal * 20;
    }
