How good are you really?

    bool betterThanAverage(List<int> classPoints, int yourPoints) {
      double classAverage = (classPoints.reduce((a, b) => a + b) + yourPoints) / (classPoints.length + 1);
      return yourPoints > classAverage;
    }
